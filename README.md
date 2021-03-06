# PyNekos: a Python client for the Nekos.moe API 
`PyNekos` provides a simple and pythonic way to use the [Nekos.moe API](https://docs.nekos.moe/).

The full documentation for `PyNekos` can be found [here](https://github.com/ChoiYun/PyNekos/blob/main/docs/doc.md).

## Setup
Some functionalities of the API needs authentication, used for post images and regenerate and get token. This way, if you pretend to use this functionalities, you'll need to [sign up](https://nekos.moe/register)  for a (free) account that authorizes access to the [Nekos.moe API](https://docs.nekos.moe/).  If you pretend to use only the simple functionalities (like get images informations, user informations, search for images, etc), you don't need to pass nothing to the **Neko** class, see [usage](https://github.com/ChoiYun/PyNekos#usage) section below.


## Installation
`PyNekos` requires Python 3.

Use `pip` to install the package from PyPI:

```bash
pip install PyNekos
```


## Usage
Import the package and initiate the Neko class:

```python
from PyNekos.nekosapi import Neko
nyan = Neko()
```

If you pretend to use more advanced functionalities of the API, you'll need the token. To get the token, you'll need your credentials: 

```python
from PyNekos.nekosapi import Neko
nyan = Neko(username='myuser', password='iwillnotshowyouthis')
token = nyan.get_token()
print(token)
```

After that, instance the object again with all informations:

```python
from PyNekos.nekosapi import Neko
nyan = Neko(token="xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx", username="myuser", password="iwillnotshowyouthis")
```

## Examples
You can see the usage of all endpoints of the API in the [example files](https://github.com/ChoiYun/PyNekos/tree/main/examples).

## Changelog
- Version 1.3:

>Implemented **kwargs in some methods for packing and unpacking
>
>Fixed some logic problems
>
>Implemented better exceptions
>
>Method "random_images" now have url of the image and url of the thumbnail in all entries of the json (before only had on the first entrie)


## Contributing
Please contribute! If you want to fix a bug, suggest improvements, or add new features to the project, just [open an issue](https://github.com/ChoiYun/PyNekos/issues) or send a pull request.
