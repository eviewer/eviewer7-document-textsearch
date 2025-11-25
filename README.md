# eViewer Search Text Sample

The **eViewer Search Text Sample** demonstrates how text search features
can be seamlessly integrated into the eViewer environment. This sample
highlights how users can enter keywords, quickly locate matching text
inside a document, and navigate through each search result with ease.

Designed to help developers understand and implement search
functionality, this sample operates fully on the client side, ensuring
fast and efficient interactions without relying on any backend services.
It serves as a simple and practical example for adding smooth and
accurate search capabilities to document-based applications.

## Set up eViewer v7

Follow the steps below to run the eViewer Search Text Sample:

1.  Clone this repository and host it via an HTTP server.
2.  Download the viewer static files from the **eViewer7 npm repo** into
    the `viewer` folder.\
    All viewer files should be placed in the root viewer folder.
3.  Open **eViewerPage.html** in your browser to launch the viewer.

## Using Search Text in eViewer

Follow the steps below to explore and use the search text functionality:

1.  Open a document in the viewer.
2.  Navigate to the **Text Search** option available in the top toolbar.
3.  Enter the word or phrase you want to search for.
4.  Choose your search scope:
    -   Current File
    -   All Files
    -   Selected Files
5.  Use Advanced Search options such as:
    -   Whole Word
    -   Case Sensitive
    -   Include Annotations
6.  Click **Search** to highlight all matching results in the document.
7.  Use the **Next** and **Previous** buttons or the results panel to
    navigate through matches.
8.  If multiple documents are open, expand or collapse results per
    document to see where matches were found.

![](https://eviewer.net/wp-content/uploads/2025/11/Search-Text.png)


## Search Text via APIs

The top section of the eViewer interface includes controls that directly
map to the underlying eViewer Search API. These UI elements allow both
users and developers to perform text search operations through simple
actions. This area demonstrates how the same operations can be automated
programmatically.

These controls showcase how eViewer's API functions can be used to
perform search actions:

-   **Search** - Initiates the text search operation by calling the
    API and highlights all occurrences of the entered keyword.

![](
https://eviewer.net/wp-content/uploads/2025/11/Search-Text-API.png)

## Commonly Used API in This Sample

- [`searchText`](https://eviewer.net/developer-guide/#Text_Search)



For complete API documentation, visit:\
**https://eviewer.net/developer-guide/**

## API Implementation Code

Below are JavaScript examples demonstrating how to perform text search
programmatically inside the eViewer application:

``` javascript
function OntextSearch() {
    let textValue = "text_to_search_goes_here";

    eViewerObj.documentService.searchText(textValue).then((response) => {
        console.log("searchText: " + response);
        textSearchForm.reset();
    });
}
```

## Try the Demo

Experience the live version of this sample here:

[Live
Demo](https://mst2019b2.eastus.cloudapp.azure.com:8443/eviewer7-document-textsearch)

## License

The license key is provided by **MST**.

For licensing inquiries or more information, contact:\
**info@ms-technology.com**
