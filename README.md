# ノ Curve ੭ Lang 〰
### Comprehensive Universal Rendering Via Enhancements 🐚

All of the names of the elements are coherent with HTML.
You cannot use `<link>`, `<br>`, or `<hr>` yet.

In your directory, 
create this file structure:
```
|── my-crv-app
    |── config.yaml
    |── app.crv
```

`config.yaml` is your project configuration. 
Here's an example:

```yaml
project:
  # The name of your project will go here.
  title: "Example Curve Project"
```

Then your `app.crv` file is your editable code.

### Running Files

To run files, use python. Download the `curve` file from the directory above and put it in the same directory as your app.

Linux/Mac:
```
python3 curve app.crv
```

Windows:
```
py curve app.crv
```

---

# Todo:
- [ ] Add Javascript Dependencies via config file
- [ ] Add CLI Flag to Specify Config File
- [ ] `create-curve-app` command
- [ ] Compile curve to executable for better CLI access / pip module?
- [ ] Add CSS Dependencies via config file
- [ ] More config stuff in general
- [ ] Better Documentation
- [ ] Add option to disable opening in browser in config
- [ ] Add option for live server in config
      
