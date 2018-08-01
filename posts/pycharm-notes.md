# Pycharm is charming

## Config pylint

#### Install pylint
```
pip install pylint
```

#### Config pylintrc
- Create config file
```
touch ~/.pylintrc
```

- Add settings
```
https://github.com/jerry-le/dotfiles/blob/master/.pylintrc
```

#### Add external tool
- Create new external tool
```
Settings > Preferences > External Tools > Add
```

- Setting
```
Name: pylint
Description: pylint as an external tool
Program: /path/to/pylint (use `which pylint` to find the path)
Arguments: $FilePath$ --rcfile=~/.pylintrc
Working directory: $ProjectFileDir$
```

- Example
![Pylint settings in Pycharm][pylint-settings]


[pylint-settings]: https://i.imgur.com/JwKmkoZ.png
