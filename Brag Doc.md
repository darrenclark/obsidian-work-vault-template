# Brag Doc
### `#brag` items

```dataview
LIST item.text
FROM #brag 
FLATTEN file.lists as item
WHERE contains(item.text, "#brag")
SORT file.day DESC
```
