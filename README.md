# Pygame Playground

Getting to know PyGame through samples and mini-games!

## Setting up

You'll need the following prerequisites; consult your particular platform to best fulfill these requirements.

* Python 3.
* Pip 3.
* `virtualenv`.

Afterwards, follow the below instructions.

1. `cd` into `src`.
2. Create a Python 3 virtual environment: `virtualenv -p python3 env`.
3. Activate the Python virtual environment: `source env/bin/activate`.
4. Install Python dependencies: `pip install -r requirements.txt`.
5. You should now be able to any of the examples in the directories in `src`.

## Note for VS Code and pylint users

`pylint` will complain that `pygame` has no members such as `init()`, `quit()`, etc. To fix this issue, you'll need to [whitelist C extensions](https://stackoverflow.com/questions/50569453/why-does-it-say-that-module-pygame-has-no-init-member). Adding the following pylintArgs to your `.vscode/settings.json` should be sufficient.

```javascript
{
    "python.linting.pylintArgs": [
        "----extension-pkg-whitelist=1xml"
    ]
}
```
