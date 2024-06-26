# ノ Curve Lang 
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
python3 curve app.crvm config.yaml
```

Windows:
```
py curve app.crv config.yaml
```

The command is basically:

```
<python-command> curve <your-curve-app> <your-config-file>
```

### Code Documentation

To create elements, invoke the `%` selector.
```
%h1 "My Curve App"
%p "This is a p tag with the classname of example." :class=example
```

To create attributes for elements, invoke the `:` selector.
```
%h1 "This is a red header." :class=redHeader
%style "#redHeader { color: red; }"
```

For comments, simply put a `#`.

```
# This is a comment!
```

### Scripting

The `==>` indicator in Curve indicates scripting. Since Curve was designed to be easy to understand for beginner programmers, there are many JavaScript shorthands.
Here's an example in JavaScript:
```
let x = document.querySelector("#myElement");
x.innerHTML = "Hello, World!"
```
In Curve would be:
```
==> var x = id("myElement")
==> x.value = "Hello, World!"
```
Which is in my opinion, a lot easier. 
For detecting clicks, here's some JavaScript code:
```
let x = document.querySelector("#myButton");
x.addEventListener("click", () => {
    // Code Here
});
```
In Curve is:
```
==> @x = id("myButton")
==> x.on("click", func{ console.log("Hello, World!") })
```

### Styles

Styles are normal CSS. Shorthand coming soon!

```
--> #myContainer { color: red; }
```

### Create Curve App

Running `py create-curve-app` will bring up a menu to create a curve app in a new directory.


### Other Config Options

In your `config.yaml` file you have different options.

- `disableDefaultCSS` does exactly what it sounds like it does.
- `cssDependencies` are a list of URLs with CSS dependencies. (Pairs great with `disableDefaultCSS`!)
- `jsDependencies` are a list of URLs with JavaScript dependencies.

---

# Todo:
- [X] Add Javascript Dependencies via config file
- [X] Add CLI Flag to Specify Config File
- [X] `create-curve-app` command
- [X] Add CSS Dependencies via config file
- [X] More config stuff in general
- [X] Better Documentation
- [ ] Add option to disable opening in browser in config
- [ ] Add option for live server in config
- [X] CSS using `-->`
