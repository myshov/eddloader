# Eddloader

A simple synchronous script loader based on pattern "Externally Defined Dependencies".

## Usage

Add to the html file the script tag with appropriate data-attributes:

```html
<script type="text/javascript" src="eddloader.js" data-edd-path='' data-edd-deps='deps.json'></script>
```

The json file with dependencies must have property `files` with list of dependencies:

```json
{
    "files": {
        "file1.js": ["file2.js", "file3.js"],
        "file2.js": [],
        "file3.js": ["file4.js"],
        "file4.js": []
    }
}
```

## Licence

MIT
