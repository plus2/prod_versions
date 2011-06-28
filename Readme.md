# prod_versions

Pulls git shas from webpages and compares them to tags in local repos.

## background

The idea is that we arrange for our apps to render the deployed git sha (usually in a comment on their front page). We use [Plus2Version][p2v]  for this.

    <!-- f8c09c36f3fc0b2faa20198a36f26e0249cfd69d -->

`prod_versions` fetches this sha & compares it to shas in the corresponding local repo (currently we're just matching tags... it'd be a good idea to extend this to refs).

## installation

Its node! You need node! Get node!

Then, make yourself a `repos.js` which looks like `repos.eg.js`.

Then run it.

    ./prod_versions

## security concerns

I made the decision that the git sha is opaque and meaningless enough that displaying it on the page of my apps is of no security concern at all.

You might think differently, and I just wanted to bring it to your attention.

## License

Copyright (C) 2011 by PLUS2 Pty. Ltd.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.


[p2v]: https://github.com/plustwo/plus2_version "Plus2Version"
