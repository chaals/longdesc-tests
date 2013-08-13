longdesc-tests
==============

Proposed tests for the HTML Image Description Extension specification http://www.w3.org/TR/html-longdesc

There are 11 tests for descriptions, under different combinations of circumstances - images included "normally", as data: URIs, or missing, with the descriptions internal or external to the page, as a data: URI, or in a location only reachable by taking into account the base element.

The same tests can be used to determine whether in various scenarios the User Agent enables the user to access the description, and whether the description can be found through system accessibility APIs.

Links to the test files along with a description of expected results can be found below:

## Longdesc value as data:URI

In order for the following tests to pass, the tester must be able to access the image description (longdesc). Success is the display of the "Longdesc test Pass page" (page title) which simply consists the word "Pass" contained in a heading level 1.

* [data:URI image with data:URI description](data-uri-image-data-uri-description.html)
* [Empty image with data:URI description](empty-image-data-uri-description.html)
* [External image with data:URI description (with extra spaces)](external-image-data-uri-description-girt-by-spaces.html)
* [External image with data:URI description](external-image-data-uri-description.html)

## Longdesc value as external URI

In order for the following tests to pass, the tester must be able to access the "Longdesc test Pass Page" which consists of the word "Pass" in a heading level 1 followed by a long description of the image.

* [data:URI with External description](data-uri-image-external-description.html)
* [Empty image with an External description](empty-image-external-description.html)
* [External image with External description (with extra spaces)](external-image-external-description-girt-by-spaces.html)
* [External image with External description](external-image-external-description.html)

## Longdesc value as internal URI (same page link)

In order for the following tests to pass, the tester must verify that the focus has moved to text that reads "Pass, if the focus is here"

* [data:URI with Internal description.html](data-uri-image-internal-description.html)
* [Empty image with an Internal description.html](empty-image-internal-description.html)
* [External image with an Internal description (with extra spaces)](external-image-internal-description-girt-by-spaces.html)
* [External image with an Internal description](external-image-internal-description.html)

## Longdesc value as external URI in presence of `<base>` element

In order for the following tests to pass, the tester must be able to access the "Longdesc test Pass Page" which consists of the word "Pass" in a heading level 1 followed by a long description of the image. *NOTE: the URI of the pass page will actually be fail.html, but the page indicates a pass - this is used to demonstrate that URIs are quite often opaque or misleading strings and should not be presented directly to the user*

* [External image with External Description (relative base element set)](external-image-with-relative-base-external-description.html) 
* [External image with External Description (absolute base element set)](external-image-with-absolute-base-external-description.html)

## Other tests

In order to tests that the HTML attribute reflects changes made by javascript, the tester must be able to access the "Longdesc test Pass Page" which consists of the word "Pass" in a heading level 1 followed by a long description of the image.  Displaying the "Longdesc test Fail Page" would indicate a failure of this test.

* [Longdesc value updated by javascript](reflected-changing-longdesc.html) 

The following test page loads an an image with a long description from a separate document using an `<iframe>`. In order for the following tests to pass, the tester must be able to access the "Longdesc test Pass Page" which consists of the word "Pass" in a heading level 1 followed by a long description of the image.  *NOTE: Some tools are known to not provide discoverability of descriptions of images loaded in an `<iframe>`*

* [Image in an `<iframe>` with External Description](iframe-discoverability.html) 

The following test page contains an invalid long description (plain text) and can be used to test User Agent and validation tool handling. *NOTE: Handling of invalid longdescs by user agents is currently undefined.*

* [Invalid long description (plain text)](invalid-longdescription.html) 

## Supporting files

Below is a list of files that are required to make one or more of the tests work:

* [fail.html](fail.html)
* [pass.html](pass.html)
* [picture.png](picture.png)
* [rebased/picture2.png](rebased/picture2.png))
* [rebased/fail.html](rebased/fail.html) (actually a pass message - URIs are quite often opaque or misleading strings)



