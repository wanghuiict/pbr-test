# test OpenStack pbr

## build && install

```
# python setup.py  build

# cat pbrdemo.egg-info/PKG-INFO 

# python setup.py  bdist_rpm

# yum install dist/pbrdemo-0.1.2-1.noarch.rpm
 
# pbrdemo
test OpenStack pbr

```

## version

pbr从git tag得到Version，

但是对于tag的格式有要求，

似乎不能支持v开头的形式，只能支持x.y.z的形式，

例如，v0.1.0没有得到支持，生成的版本是类似0.0.1.dev2

0.1.1可以支持，生成版本0.0.1

## entry_point

```
>>> import pkg_resources
>>> 
>>> named_objects = {}
>>> for ep in pkg_resources.iter_entry_points(group='test_1'):
...    named_objects.update({ep.name: ep.load()})
... 
>>> print named_objects
{'testfun1': <function func1 at 0x7fded7977668>}
>>> named_objects['testfun1']
<function func1 at 0x7fded7977668>
>>> named_objects['testfun1']()
in cls1.fun1()
```

-END-

