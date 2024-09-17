---
banner: "![[wallhaven-2yxp16.jpg]]"
banner_y: 0.66
---


# 🏠 Homepage

- [[小狗钱钱]]
- [[国外新闻网]]
- [[定语从句]]
- [[夏沫的海]]
- [obsidian咖啡](https://obsidian.vip/)
- [个人知识库](https://pkmer.cn/)
- [obsidian中文论坛](https://forum-zh.obsidian.md/)
- [dataview](https://blacksmithgu.github.io/obsidian-dataview/)

```dataviewjs

let ftMd = dv.pages("").file.sort(t => t.cday)[0]
let total = parseInt([new Date() - ftMd.ctime] / (60*60*24*1000))
let totalDays = "您已使用 *Obsidian* "+total+" 天，"

let inputFile = dv.pages('"阅读"').file
let inputMd = "共输入 "+
	inputFile.length+" 篇笔记，"

let outputFile = dv.pages('"Outputs"').file
let outputMd = "共输出 "+
	outputFile.length+" 篇笔记，"

let paperFile = dv.pages("#paper").file
let paperMd = "共读了 "+
	paperFile.length+" 篇文献。"

dv.paragraph(totalDays+inputMd+outputMd+paperMd)

```
# ⌛ 今日代办

```dataview
task from "record/diary"
where !completed and date(file.name) = date(today)
```
# 📅 七日代办

```dataview
task from "record/diary"
where !completed and date(file.name) <= (date(today) + dur(7 days))
```

# 🎠 天马行空
```dataviewjs
dv.current()
```
```dataview
TASK
FROM "task"
WHERE meta(section).subpath = "todo"
```

```ActivityHistory
/
```


