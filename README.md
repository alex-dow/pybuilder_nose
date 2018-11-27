# DEAD

Sadly this project is no longer active. Feel free to fork it and carry it on if you find it useful.

# pybuilder_nose

PyBuilder plugin to easily run nosetests.

## Usage

Add plugin dependency to your build.py

```
  use_plugin('pypi:pybuilder_nose')
```

If you are also using the plugin python.unittest, you should remove it.

In theory, this is all you need to do to start using Nose for unit testing and code coverage reports. However, if you want to tweak it, all nose command line parameters are available for configuration through the project properties. Simply append "nose_" for the property key.

For example, if you want to replace the html coverage directory:

```python
@init
def init(project):
  project.set_property('nose_html-coverage-dir', '/path/to/html')
```

This is equivalent to running

```
$ nodetests --html-coverage-dir=/path/to/html
```

## Todo List
Separate coverage from unit tests so you can have both an analze and a run_unit_tests task

## Changelog

0.0.5 - Fixed a py3 incompatibility


