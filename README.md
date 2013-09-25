longdesc-tests
==============

Proposed tests for the [HTML Image Description Extension specification](http://www.w3.org/TR/html-longdesc). These tests are © chaals, and available under the [W3C Software license](http://www.w3.org/Consortium/Legal/copyright-software)

## Multifunction tests

These 15 tests include descriptions under different combinations of circumstances - images included "normally", as data: URIs, or missing, with the descriptions internal or external to the page, as a data: URI, or in a location only reachable by taking into account the base element.

The same tests are used to provide 3 results:
1 Can the user discover there is an image that has a long description available?
2 Can the user access the description? To pass, the user should arrive at the "pass page" which has a heading "Pass" followed by a description, or the focus must be on the text "Pass, if the focus is here" which is followed by a description of the image.
3 Is the long description available to system accessibility APIs

### Longdesc value as data:URI

* [data:URI image with data:URI description](https://rawgithub.com/chaals/longdesc-tests/master/data-uri-image-data-uri-description.html)
* [Empty image with data:URI description](https://rawgithub.com/chaals/longdesc-tests/master/empty-image-data-uri-description.html)
* [External image with data:URI description (with extra spaces)](https://rawgithub.com/chaals/longdesc-tests/master/external-image-data-uri-description-girt-by-spaces.html)
* [External image with data:URI description](https://rawgithub.com/chaals/longdesc-tests/master/external-image-data-uri-description.html)

### Longdesc value as external URI

* [data:URI with External description](https://rawgithub.com/chaals/longdesc-tests/master/data-uri-image-external-description.html)
* [Empty image with an External description](https://rawgithub.com/chaals/longdesc-tests/master/empty-image-external-description.html)
* [External image with External description (with extra spaces)](https://rawgithub.com/chaals/longdesc-tests/master/external-image-external-description-girt-by-spaces.html)
* [External image with External description](https://rawgithub.com/chaals/longdesc-tests/master/external-image-external-description.html)

### Longdesc value as internal URI (same page link)

* [data:URI with Internal description.html](https://rawgithub.com/chaals/longdesc-tests/master/data-uri-image-internal-description.html)
* [Empty image with an Internal description.html](https://rawgithub.com/chaals/longdesc-tests/master/empty-image-internal-description.html)
* [External image with an Internal description (with extra spaces)](https://rawgithub.com/chaals/longdesc-tests/master/external-image-internal-description-girt-by-spaces.html)
* [External image with an Internal description](https://rawgithub.com/chaals/longdesc-tests/master/external-image-internal-description.html)

### Longdesc value as a fragment in an external resource

* [data:URI with External description fragment](https://rawgithub.com/chaals/longdesc-tests/master/data-uri-image-external-description-fragment.html)
* [Empty image with an External description fragment](https://rawgithub.com/chaals/longdesc-tests/master/empty-image-external-description-fragment.html)
* [External image with External description fragment (with extra spaces around the URL)](https://rawgithub.com/chaals/longdesc-tests/master/external-image-external-description-fragment-girt-by-spaces.html)
* [External image with External description fragment](https://rawgithub.com/chaals/longdesc-tests/master/external-image-external-description-fragment.html)

### Longdesc value as external URI in presence of `<base>` element

* [External image with External Description (relative base element set)](https://rawgithub.com/chaals/longdesc-tests/master/external-image-with-relative-base-external-description.html) 
* [External image with External Description (absolute base element set)](https://rawgithub.com/chaals/longdesc-tests/master/external-image-with-absolute-base-external-description.html)

### Longdesc for an image within an iframe

* [Image in an `<iframe>` with External Description](https://rawgithub.com/chaals/longdesc-tests/master/iframe-discoverability.html) 

## Other tests

[Longdesc value updated by javascript](https://rawgithub.com/chaals/longdesc-tests/master/reflected-changing-longdesc.html) tests that the HTML attribute reflects changes made by javascript. To pass, the browser must redirect to the "Longdesc test Pass Page" which has the word "Pass" as a heading, followed by a description of the image.  Displaying the "Longdesc test Fail Page" would indicate a failure of this test. 

[Invalid long description (plain text)](https://rawgithub.com/chaals/longdesc-tests/master/invalid-longdesc.html) contains an invalid long description (plain text) and can be used to test User Agent and validation tool handling. *NOTE: Handling of invalid longdescs by user agents is currently undefined.*
[Invalid long description (empty attribute)](https://rawgithub.com/chaals/longdesc-tests/master/empty-longdesc.html) contains an invalid long description (plain text) and can be used to test User Agent and validation tool handling. *NOTE: Handling of invalid longdescs by user agents is currently undefined.*
[Pointer to an invalid long description (not contained in a well-formed fragment)](https://rawgithub.com/chaals/longdesc-tests/master/fail-fragment-pointer.html) points to a long description in a [page fragment whose target is an empty element](https://rawgithub.com/chaals/longdesc-tests/master/fail-fragment-pointer.html). Validation tools should at least generate a warning, since an empty element is almost certainly not an adequate description, and is likely instead to reflect not passing the relevant authoring requirement.

## Supporting files

The following files are required to make one or more of the tests work:

* [README.md](https://rawgithub.com/chaals/longdesc-tests/master/README.md) - this documentation
* [README-offline.html](https://rawgithub.com/chaals/longdesc-tests/master/README-offline.html) - an HTML version of this content to allow the contents of the repository to be posted somewhere as a self-contained bundle.
* [fail.html](https://rawgithub.com/chaals/longdesc-tests/master/fail.html)
* [pass.html](https://rawgithub.com/chaals/longdesc-tests/master/pass.html)
* [fail-fragment.html](https://rawgithub.com/chaals/longdesc-tests/master/fail-fragment.html)
* [pass-fragment.html](https://rawgithub.com/chaals/longdesc-tests/master/pass-fragment.html)
* [picture.png](https://rawgithub.com/chaals/longdesc-tests/master/picture.png)
* [rebased/picture2.png](https://rawgithub.com/chaals/longdesc-tests/master/rebased/picture2.png))
* [rebased/fail.html](https://rawgithub.com/chaals/longdesc-tests/master/rebased/fail.html) (actually a pass page, used to test what happens in the presence of a `<base>` element)



