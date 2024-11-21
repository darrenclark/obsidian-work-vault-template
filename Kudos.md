# Kudos
### `#kudos` items

```dataview
LIST item.text
FROM #kudos 
FLATTEN file.lists as item
WHERE contains(item.text, "#kudos")
SORT file.day DESC
```
