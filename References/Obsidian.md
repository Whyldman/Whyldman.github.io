
**List all notes where this note is linked** (aka Inbox)
`````
```dataview
list from [[]] and !outgoing([[]])
```
`````

List notes where this note is linked but are not in the current file. Also have the right tag fields
`````
```dataview
table type, summary from #region and [[]] and !outgoing([[]]) where contains(location, this.file.link)
```
`````

Request a name and move to a new folder but only if it's untitled 

```
<%*
let title = tp.file.title
if (title.startsWith("Untited")) {
title = await tp.system.prompt("Title?");
}
await tp.file.rename(title)
await tp.file.move("PATH_TO_FILE/" + title)
-%>

<%*
let titel = tp.file.titleif (title.startsWith("Untited") {
	title = await tp.system.prompt("Title");
}
await tp.file.rename(title)
-%>
```
