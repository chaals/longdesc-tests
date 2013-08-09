longdesc-tests
==============

Proposed tests for the HTML Image Description Extension specification http://www.w3.org/TR/html-longdesc

There are 11 tests for descriptions, under different combinations of circumstances - images included "normally", as data: URIs, or missing, with the descriptions internal or external to the page, as a data: URI, or in a location only reachable by taking into account the base element.

The same tests can be used to determine whether in various scenarios the User Agent enables the user to access the description, and whether the description can be found through system accessibility APIs.

* [data-uri-image-data-uri-description.html](data-uri-image-data-uri-description.html)
* [data-uri-image-external-description.html](data-uri-image-external-description.html)
* [data-uri-image-internal-description.html](data-uri-image-internal-description.html)
* [empty-image-data-uri-description.html](empty-image-data-uri-description.html)
* [empty-image-external-description.html](empty-image-external-description.html)
* [empty-image-internal-description.html](empty-image-internal-description.html)
* [external-image-data-uri-description-girt-by-spaces.html](external-image-data-uri-description-girt-by-spaces.html)
* [external-image-external-description-girt-by-spaces.html](external-image-external-description-girt-by-spaces.html)
* [external-image-internal-description-girt-by-spaces.html](external-image-internal-description-girt-by-spaces.html)
* [external-image-data-uri-description.html](external-image-data-uri-description.html)
* [external-image-external-description.html](external-image-external-description.html)
* [external-image-internal-description.html](external-image-internal-description.html)
* [external-image-with-relative-base-external-description.html](external-image-with-relative-base-external-description.html)
* [external-image-with-absolute-base-external-description.html](external-image-with-absolute-base-external-description.html) will only work if the base href is changed to match the location from which it is run…
* [reflected-changing-longdesc.html](reflected-changing-longdesc.html) tests that the javascript attribute really reflects the HTML attribute

All the tests previously mentioned can used to determine if the presence of a longdesc is discoverable under various conditions.

[iframe-discoverability.html](iframe-discoverability.html) includes an image with a description in a separate document that is loaded within an iframe, to test whether tools provide discoverability in that situation (at least some are known to fail that test).

[invalid-longdescription.html](invalid-longdescription.html) can be used to test validation tools, but handling of invalid longdescs by user agents is currently undefined.

There are some files required to make one or more tests work:

* [fail.html](fail.html)
* [pass.html](pass.html)
* [picture.png](picture.png)
* [rebased/picture2.png](rebased/picture2.png))
* [rebased/fail.html](rebased/fail.html) (actually a pass message - URIs are quite often opaque or misleading strings)



