
```dataviewjs
dv.taskList(dv.pages('"record/"').sort((a, b) => { return new Date(a.file.name) - new Date(b.file.name); }).file.tasks)
```

```dataviewjs
dv.paragraph(dv.pages('"record/diary"').sort())
```

