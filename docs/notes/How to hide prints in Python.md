# How to hide prints in Python
Here's a code example of how to hide prints in [[publish/docs/notes/index]]:

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
