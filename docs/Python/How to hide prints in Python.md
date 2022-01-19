# How to hide prints in Python
Here's a code example of how to hide prints in [[Python]]:

```Python
class HidePrints:
    def __enter__(self):
        self._original_stdout = sys.stdout
        sys.stdout = open(os.devnull, 'w')

    def __exit__(self, exc_type, exc_val, exc_tb):
        sys.stdout.close()
        sys.stdout = self._original_stdout

		
with HidePrints():
    function_that_prints_bullshit()
```
--- 

### Related Notes
```dataview
TABLE WITHOUT ID
	file.cday as "Created",
	link(file.link, file.title) as "File Name"

FROM "" WHERE
	file!=this.file
	AND !contains(file.path, "Templates")
	AND (
		contains(file.outlinks, this.file.link)
		OR contains(this.file.outlinks, file.link)
	)

SORT file.ctime DESC
```