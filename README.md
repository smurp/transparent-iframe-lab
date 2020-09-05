# transparent-iframe-lab

The objective here is to explore how best to achieve an IFRAME which:
* covers an entire window
* is mostly `transparent` so the user sees and can use the page below
* but also has widgets on it which the user *can* manipulate
* using pure CSS
* and resulting in undiminised functionality of the page below.

The motivation for this effort is to create `overlays` for browser
extensions which can augment pages without imparing their usability.

## Help! :-)

This is a tricky undertaking which, as far as I can tell so far,
is quite likely not possible.  Why is this so hard?

1. If the IFRAME src doc has `html, body {pointer-events: none}` then it's own
widget content works just fine, but the clicks on the `blank spaces`
simply don't propagate to the document containing the IFRAME.
2. If the IFRAME tag itself has `{pointer-events: none}` then user clicks
do propagate right through the IFRAME onto the containing document but
there appears to be no styling of the page in the IFRAME which can
intercept clicks... understandably, because the IFRAME itself is tranparent
to them.
3. There does not appear to be another way...

If you can demonstrate a remedy to this connundrum please drop a line to `smurp@smurp.com`






