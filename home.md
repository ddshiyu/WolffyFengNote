---
banner: "![[IMG-20240910225959113.jpeg]]"
banner_y: 0.42057
---
# 🏠 Homepage

- [👤 Personal](app://obsidian.md/%F0%9F%91%A4%20Personal)
- [💼 Productivity](app://obsidian.md/%F0%9F%92%BC%20Productivity)
- [📥 Inputs](app://obsidian.md/%F0%9F%93%A5%20Inputs)
- [🧰 Utilities](app://obsidian.md/%F0%9F%A7%B0%20Utilities)

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
# ⌛今日代办

```dataview
task from "record"
where !completed
```


# 🎠天马行空
```dataviewjs
dv.current()
```
```dataview
TASK
FROM "任务看板"
WHERE meta(section).subpath = "todo"
```

```ActivityHistory
/
```


