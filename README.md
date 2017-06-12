XML2JSON
========

Python script converts XML to JSON or the other way around

Usage
-----
Make this executable

    $ chmod +x xml2json

Then invoke it from the command line like this

    $ xml2json -t xml2json -o file.json file.xml

Or the other way around

    $ xml2json -t json2xml -o file.xml file.json

Without the `-o` parameter `xml2json` writes to stdout

    $ xml2json -t json2xml file.json

Additional the options:
Strip text (#text and #tail) in the json

    $ xml2json -t xml2json -o file.json file.xml --strip_text

Strip namespace in the json 

    $ xml2json -t xml2json -o file.json file.xml --strip_namespace

In code

    from xml2json import json2xml
    d = {'r': {'@p': 'p1', '#text': 't1', 'c': 't2'}}
    print(json2xml(d))
    > b'<r p="p1">t1<c>t2</c></r>'
    
Installation
------------
Either clone this repo or use `pip` like this:

    pip install https://github.com/hay/xml2json/zipball/master

License
-------
xml2json is released under the terms of the [Apache License](http://www.apache.org/licenses/LICENSE-2.0).

Contributors
------------
Original Contributor - Nirmal Sarswat
Links
------
* [Github](http://github.com/drewlabs/XJT)

How it works
------------

