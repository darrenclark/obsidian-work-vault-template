---
date: 2024-11-20
tags: [meeting/one-on-one, people/john-appleseed, ]
---
# 2024-11-20 John Appleseed

#### 🗒️ Notes

- Chatted about more Github Copilot use cases:
	- Code review
	- Optimizing code

#### 📝 Action Items


#### ℹ️ Pending Action Items

```dataviewjs
let person = dv.current().tags.find((t) => t.startsWith("people/"));

if (person) {
  let oneOnOnes = dv.pages("#meeting/one-on-one and #" + person).file.tasks
  let tags = dv.pages().file.tasks.where(t => t.text.includes("#" + person))
  
  let query = oneOnOnes.concat(tags).where((t) => !t.fullyCompleted && !t.text.includes("❌"))
  dv.taskList(query)
} else {
  dv.paragraph("")
  dv.el("i", "Add a `#people/xyz` tag to view previous one on ones")
}
```

#### 🔗 Previous
```dataviewjs
let person = dv.current().tags.find((t) => t.startsWith("people/"));
let date = dv.current().date;

if (person) {
  let query = dv.pages("#meeting/one-on-one and #" + person).filter((p) => p.date < date).sort((p) => p.date, 'desc')
  dv.list(query.file.link)
} else {
  dv.paragraph("")
  dv.el("i", "Add a `#people/xyz` tag to view previous one on ones")
}
```
