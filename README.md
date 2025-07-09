
## SearxMe Extension — Private Web Searching with Your Own SearXNG Instance

This extension has been tested on Firefox and Zen Browser. Although not explicitly tested, it should work on any Firefox-based browser.

### Prerequisites

- Firefox or Zen Browser (Firefox-based)
- Access to your SearXNG instance URL

### Installation


#### 1. Clone the Repository

```bash
git clone https://github.com/yaxirhuxxain/searxMe-extension.git
```

#### 2. Update the Search URL

* Open `manifest.json` inside the cloned `searxMe-extension` folder
* Locate the line with `"search_url": "https://your-instance.com/search?q={searchTerms}"`
* Replace `https://your-instance.com` with your SearxMe instance URL, i.e.:

```json
"search_url": "https://search.example.com/search?q={searchTerms}"
```
or 

```json
"search_url": "http://localhost:port/search?q={searchTerms}"
```


* Save the file

#### 3. Create the ZIP Archive

* Inside the `searxMe-extension` folder using terminal (macOS/Linux) or PowerShell (Windows) run:

```bash
zip -r ./searxMe-extension.zip .
```

* Or on Windows (GUI):

  * Right-click the `searxMe-extension` folder
  * Select **Send to → Compressed (zipped) folder**

> **Important:** The ZIP must contain the extension files at the root level, not inside a subfolder.

#### 4. Load the Extension in Firefox or Zen Browser

* Open a new tab and enter this address in the URL bar: `about:debugging#/runtime/this-firefox`
* Click **Load Temporary Add-on...**
* Select the `.zip` file you created
* Verify it loads without errors

#### 5. Set SearxMe as Your Search Engine and Test

* Go to **Settings → Search** in your browser
* Select **searxMe** as the default search engine
* Test it to ensure it works


### Feedback & Support

If you encounter any issues or have suggestions, please open an [issue or start a discussion](https://github.com/yaxirhuxxain/searxMe-extension/issues) in the repository. Your feedback is always welcome—cheers!
