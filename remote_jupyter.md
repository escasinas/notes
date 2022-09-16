### Accessing jupyter notebook remotely

1) Generate a jupyter config in the remote machine
```
jupyter notebook --generate-config
vim .jupyter/jupyter_notebook_config.py
```

2) Change these settings
```
c.NotebookApp.token = ''
c.NotebookApp.open_browser = False
c.NotebookApp.port = <PORT> # pick any port number
```

3) Run `jupyter notebook` on the remote machine

4) On your host machine, set up an SSH tunnel
```
ssh -L <PORT>:localhost:<PORT> user@remote_host
```

5) On your host browser, go to `http://localhost:<PORT>/`
