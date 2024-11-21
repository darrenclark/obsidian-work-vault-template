# Noteworthy

### `#noteworthy` items

```dataview
LIST item.text
FROM #noteworthy 
FLATTEN file.lists as item
WHERE contains(item.text, "#noteworthy")
SORT file.day DESC
```
