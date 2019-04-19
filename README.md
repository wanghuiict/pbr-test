test OpenStack pbr

```
# python setup.py  build
running build
running build_py
running egg_info
writing pbr to pbrdemo.egg-info/pbr.json
writing pbrdemo.egg-info/PKG-INFO
writing top-level names to pbrdemo.egg-info/top_level.txt
writing dependency_links to pbrdemo.egg-info/dependency_links.txt
writing entry points to pbrdemo.egg-info/entry_points.txt
[pbr] Processing SOURCES.txt
[pbr] In git context, generating filelist from git
warning: no previously-included files found matching '.gitreview'
warning: no previously-included files matching '*.pyc' found anywhere in distribution
writing manifest file 'pbrdemo.egg-info/SOURCES.txt'


# cat pbrdemo.egg-info/PKG-INFO 
Metadata-Version: 1.1
Name: pbrdemo
Version: 0.1.1
Summary: test OpenStack pbr
Home-page: https://launchpad.net/pbr
Author: wanghuiict
Author-email: wanghuiict@gmail.com
License: Apache-2
Description: test OpenStack pbr
        
        create
        
        
Keywords: setup
distutils
Platform: UNKNOWN
Classifier: Development Status :: 4 - Beta
Classifier: Environment :: Console
Classifier: Environment :: OpenStack
Classifier: Intended Audience :: Developers
Classifier: Intended Audience :: Information Technology
Classifier: License :: OSI Approved :: Apache Software License
Classifier: Operating System :: OS Independent
Classifier: Programming Language :: Python

```


pbr从git tag得到Vrsion，

但是对于tag的格式有要求，

似乎不能支持v开头的形式，只能支持x.y.z的形式，

例如，v0.1.0没有得到支持，生成的版本是类似0.0.1.dev2

0.1.1可以支持，生成版本0.0.1




