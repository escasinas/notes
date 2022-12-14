# R Jupyter

##### Setup R for Jupyter Notebook/Lab

In RStudio or R console:
```
install.packages('IRkernel')
```

```
IRkernel::installspec(user = FALSE)
```

##### Add keyboard shortcut for <-
Settings -> Advanced Settings Editor -> Keyboard Shortcuts -> JSON Settings Editor
```
{
    "shortcuts": [
         {
            "command": "notebook:replace-selection",
            "selector": ".jp-Notebook",
            "keys": ["Alt -"],
            "args": {"text": ' <- '}
        }
    ]
}
```
