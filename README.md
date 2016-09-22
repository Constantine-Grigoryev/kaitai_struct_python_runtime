# Kaitai Struct: runtime library for Python

This library implements Kaitai Struct API for Python.

[Kaitai Struct](http://kaitai.io) is a declarative language used for
describe various binary data structures, laid out in files or in memory:
i.e. binary file formats, network stream packet formats, etc.

It is similar to Python's [construct] and [Construct3], but it is
language-agnostic. The format description is done in YAML-based .ksy
format, which then can be compiled into a wide range of target languages.

[construct]: https://pypi.python.org/pypi/construct
[Construct3]: http://tomerfiliba.com/blog/Survey-of-Construct3/

Further reading:

* [About Kaitai Struct](https://github.com/kaitai-io/kaitai_struct/)
* [About API implemented in this library](https://github.com/kaitai-io/kaitai_struct/wiki/Kaitai-Struct-stream-API)
* [Python-specific notes](https://github.com/kaitai-io/kaitai_struct/wiki/Python)

## Installing

### Using `requirements.txt`

If you want to use Kaitai Struct runtime in your project and you use
`requirements.txt` to manage your dependencies, just add the following
line to it:

```
kaitaistruct
```

and then run `pip install -r requirements.txt` to update all your
dependencies.

### Using `pip` directly

You can use

```shell
pip install kaitaistruct
```

to install the package manually using `pip` Python package manager.

### From the source code

You can make Kaitai Struct runtime package by your own. This is
the best way to obtain the freshest developer version of the library,
but be careful: as any developer version it may be a little buggy.
In order to install Kaitai Struct runtime such way, please clone
or download its repository from GitHub, then jump to repository's
root directory (where `setup.py` lives) and run the following:

```shell
pip install .
```

Alternatively, you can bypass `pip` utility (not recommended;
bypassing confuses Python package managers and may cause an error
in case of further `pip`ing the package):

```shell
python setup.py install
```

### Manually

This library is intentionally kept as very simple, one-file `.py`
module. One can just copy it to your project from this repository.
Usually you won't `import` it directly, it will be loaded by Python
source code generated by Kaitai Struct compiler.

## Check installation

The easiest way to make sure that Kaitai Struct runtime has installed
succesfully is try to import one of its components:

```shell
python -c "from kaitaistruct import KaitaiStruct"
```

Normally this snippet exits without any output. A displayed message
indicates an issue.

## Licensing

Copyright 2015-2016 Kaitai Project: MIT license

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
