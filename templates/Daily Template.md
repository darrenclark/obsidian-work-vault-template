---
date: {{date}}
---
# {{title}}

#### _{{date:dddd, MMMM DD, YYYY}}_

#### 📝 Tasks



#### 📅 Meetings

```dataview
LIST
FROM #meeting
WHERE file.day = this.file.day
```

#### 🗒️ Notes


#### ✅ Completed Tasks

```tasks
done on "{{date}}"
```