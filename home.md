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

let ftMd = dv.pages('"home"').file.sort(t => t.cday)[0]
let total = parseInt([new Date() - ftMd.ctime] / (60*60*24*1000))
let totalDays = "您已使用 *Obsidian* "+total+" 天，"

let inputFile = dv.pages('"lifeStyle"').file
let inputMd = "共输入 "+
	inputFile.length+" 篇笔记，"

let outputFile = dv.pages('"record/diary"').file.tasks
let outputComMd = "共完成 "+
	outputFile.where(t => t.completed).length+" 项待办，"
let ouputUncomMd = "未完成 " + outputFile.where(t => !t.completed).length+" 项待办，"

let horse = dv.pages('"task"').file.tasks
let horseComMd = "共完成 "+
	horse.where(t => t.completed).length+" 项计划，"
let horseUmComMd = "未完成 "+
	horse.where(t => !t.completed).length+" 项计划，"

dv.paragraph(totalDays+inputMd+outputComMd+ouputUncomMd+horseComMd+horseUmComMd)

```
# ⌛ 今日待办

```dataview
task from "record/diary"
where !completed and date(file.name) = date(today)
```
# 📅 近七日待办

```dataview
task from "record/diary"
where !completed
```

# 🎠 计划
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


