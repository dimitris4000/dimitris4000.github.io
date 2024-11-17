
# File structure
 - *public* This directory is completely generated and contains all the static code required for the site to run after build. Feel free to delete and recreate by regenerating the site with `hugo` command (see "How to build production" section)
 - *docs* This is a symlink to the `public` directory. It is required because this is the directory Github pages reads to serve the page.

# How to spinup dev server with draft articles rendering
hugo serve --buildDrafts

# How to build production
HUGO_ENV="production" hugo

# About Theme

## Shortcodes

**Image Gallery**
Here’s a custom Hugo shortcode that creates an image gallery in a masonry style using GLightbox, allowing you to specify a folder containing images. This approach will display images from a specified folder in a masonry layout, and each image will open in a lightbox when clicked.
```
{{/*< img_gallery  folder="img/travel/" >*/}}
```

**Info Card / Info Box**
Displays information in a card format.
```
{{/* < info_cards header="lorem-ipsum" title="What is Lorem Ipsum?" content="Lorem Ipsum is simply dummy text of the printing and typesetting industry." > */}}
```

**Card**
Adds cards with text and links.
```
{{/* < bs_img_card title="Some" link="https://some.com/"
descr="Lorem Ipsum is simply dummy text of the printing and typesetting industry." > */}}

{{/* < bs_img_card title="Example" link="https://www.example.io/" 
descr="Lorem Ipsum is simply dummy text of the printing and typesetting industry." > */}}

{{/* < bs_img_card title="Here" link="https://www.here.com/"
descr="Lorem Ipsum is simply dummy text of the printing and typesetting industry." > */}}
```

**Details**
This simply adds the html5 detail attribute, supported on all modern browsers. Use it like this:
```
{{/* < details "This is the details title (click to expand)" > */ }}
Some placeholder content for the collapse component. This panel is hidden by default but revealed when the user activates the relevant trigger.
{{ /* < /details > */}}

```

**Split**
This adds a two column side-by-side environment (will turn into 1 col for narrow devices):
```
{{ /* < columns > */ }}
This is column 1.
{{ /* < column > */ }}
This is column 2.
{{ /* < endcolumns > */ }}
```




## Parameters
Theme Parameters
```
    readingTime
        Type: Boolean (true or false)
        Description: When set to true, displays an estimated reading time for each post. This helps readers gauge how long it will take to read the content.

    wordCount
        Type: Boolean
        Description: Enables or disables the word count display for each post. Useful for readers interested in post length.

    hideAuthor
        Type: Boolean
        Description: Controls the visibility of the author information on each post. Set to false to display the author section or true to hide it.

    previewCardImagePlacement
        Type: String ("top" or "middle" or "bottom" or "none" )
        Description: Determines where the preview image appears on post cards in lists or summaries. "top" places the image above the text, “middle”: Centers the image within the text area, "bottom" places below the text, and "none" hides the preview image entirely,.

    hidePostImage
        Type: Boolean
        Description: Controls the visibility of the featured image on individual post pages. Set to true to hide post images or false to show them.

    useHLJS
        Type: Boolean
        Description: Enables Highlight.js, a JavaScript library for syntax highlighting in code blocks. Set to true to use Highlight.js for syntax highlighting.

    socialShare
        Type: Boolean
        Description: Adds social sharing buttons to posts, allowing readers to share content on various social media platforms.

    showRelatedPosts
        Type: Boolean
        Description: When enabled, displays related posts at the bottom of each post to encourage further reading.

    gcse
        Type: Boolean
        Description: Enables Google Custom Search Engine integration for site search functionality. Requires a configured search engine ID.

    Lastmod
        Type: Boolean
        Description: Controls whether the “Last Modified” date is shown on posts, which can be helpful for showing recent updates.

    rss
        Type: Boolean
        Description: Enables RSS feed generation for the site, making it easy for users to subscribe to your content.

    pagination
        Type: Integer
        Description: Sets the number of posts displayed per page on list or archive pages.

    description
        Type: String
        Description: A short description of your website that may appear in the metadata or be used for SEO.

    lunrSearch
        Type: Boolean
        Description: Enables Lunr.js search, a client-side search engine, allowing users to search content directly on the site.
```

# Useful references
- [Lightbi Theme Articles - by author](https://lightbi-hugo-theme.netlify.app/en/)
