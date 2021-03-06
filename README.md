## Welcome ##

http://pygments-1-4.appspot.com is an unofficial API for the Pygments syntax highlighting library, version 1.4.
It's designed to provide syntax highlighting for web applications that don't have Python installed.

The origional was forked from trevorturk and updated to work with newer versions of Pygments.

## Usage ##

POST to http://pygments-1-4.appspot.com with "lang" and "code" parameters in the body.
You'll receive pygmentized HTML back, which you can store for later display on your site.
You can style the pygmentized HTML using CSS like this: http://github.com/austinbv/pygments/blob/master/default.css

## Ruby Example ##

```ruby
require 'net/http'
require 'uri'

lang = 'python'
code = 'print "Hello World"'

request = Net::HTTP.post_form(URI.parse('http://pygments.appspot.com/'), {'lang'=>lang, 'code'=>code})
puts request.body
```

## More Information ##

This site was created so that http://flowcoder.com could run on http://heroku.com, but please feel free to use it yourself.
If you like, you can fork the code on github and create your own Google App Engine site, though.

Visit http://pygments.org/ for more information about Pygments.
Visit http://github.com/richleland/pygments-css for more example CSS files for use with Pygments.
Visit http://github.com/trevorturk/pygments for more information about this site, and to see the source code.

See also: http://www.hilite.me/ for a similar application with more options.

## MIT License ##

Copyright (c) 2009 Trevor Turk

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
