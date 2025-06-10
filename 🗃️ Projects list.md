# 🗃️ Projects list

```dataview
TABLE WITHOUT ID 
file.link AS "Project",
choice(length(filter(file.tasks, (x) => all(x.text, !x.completed))), "–", "Yes") AS "Needs tasks"
FROM #project AND !"Utility" AND !#exclude-master-tasklist AND !#completed AND !"Resources"
WHERE !completed
SORT file.name
```
