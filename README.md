# redirect-index
Example of an HTML index page that redirects to a custom blog post.

Step 1: Choose the website you want to redirect people from (e.g. *https://example.com/*). This is where you will add the `index.html` file once ready.

Step 2: Open `index.html` (inside the `html` folder) in a text editor and edit the below lines of code to specify the website you want to redirect to. You can use the '?' in the URL to choose how to direct.

For example, if you want to redirect to *https://kucharski.substack.com/p/post-name*, then the below code will do this if the visitor goes to  *https://example.com/?post-name*. Similarly, *https://example.com/?another-post* would take the visitor to *https://kucharski.substack.com/p/another-post*.

If the visitor just navigates to *https://example.com/*, they'll get redirected to the 2nd web address below (i.e. *https://kucharski.substack.com/*).


```
            if (directLinkValue) {
				// If direct URL parameter provided, redirect to this specific page
                window.location.href = "https://kucharski.substack.com/p/" + directLinkValue;
            } else {
                // If no direct URL parameter provided, redirect to homepage
                window.location.href = "https://kucharski.substack.com/";
            }
```

Step 3: Add `index.html` to the relevant home folder for your website, so that when people visit, this is the HTML that will be displayed (and hence redirect people appropriately).