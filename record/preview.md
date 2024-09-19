
```dataviewjs
const a = dv.pages('"record/diary"').sort(a=> new Date(a.file.name).getTime(), 'desc')
a.forEach(v => {
	dv.header(2, v.file.name)
	dv.taskList(v.file.tasks, false)
})
```

