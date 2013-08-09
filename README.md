longdesc-tests
==============

Proposed tests for the HTML Image Description Extension specification http://www.w3.org/TR/html-longdesc

There are 11 tests for descriptions, under different combinations of circumstances - images included "normally", as data: URIs, or missing, with the descriptions internal or external to the page, as a data: URI, or in a location only reachable by taking into account the base element.

The same tests can be used to determine whether in various scenarios the User Agent enables the user to access the description, and whether the description can be found through system accessibility APIs.

*((data-uri-image-data-uri-desc.html))
*((data-uri-image-external-desc.html))
*((data-uri-image-internal-desc.html))
*((empty-image-data-uri-desc.html))
*((empty-image-external-desc.html))
*((empty-image-internal-desc.html))
*((external-image-data-uri-desc.html))
*((external-image-external-desc.html))
*((external-image-internal-desc.html))
*((external-image-with-relative-base-external-desc.html))
*((external-image-with-absolute-base-external-desc.html)) will only work if the base href is changed to match the location from which it is run…
*((reflected-changing-longdesc.html)) tests that the javascript attribute really reflects the HTML attribute

All the tests previously mentioned can used to determine if the presence of a longdesc is discoverable.

((iframe-discoverability.html)) includes an image with a description in a separate document that is loaded within an iframe, to test whether tools provide discoverability in that situation (at least some are known to fail that test).

((invalid-longdesc.html)) can be used to test validation tools, but handling of invalid longdescs by user agents is currently undefined.

There are some files required to make one or more tests work:

*((fail.html))
*((pass.html))
*((picture.png))
*((rebased/picture2.png))
*((rebased/fail.html)) (actually a pass message - URIs are quite often opaque or misleading strings)



