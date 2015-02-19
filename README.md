# bigyll

Jekyll layouts for @timcw's [Big](https://github.com/tmcw/big) presentation system

### How it works:
Just drop the `_layouts` folder into the Jekyll directory you want to serve Big presentations from. If you already have layouts, just add the Big layout file.

The file `example.markdown` in `_drafts` shows a demo of how to write Big presentations using this layout.

For example:
```markdown
---
layout: big
title:  "Bigyll example"
sections:
- this is slide 1
- this is slide 2
---
```

Do note that if you want to use Markdown formatting --- such as images, bold/italic, et cetera --- in your slides, you have to format your sections as blocks using the pipe (`|`) character, as in the following example:
```markdown
---
layout: big
title:  "Bigyll example"
sections:
- |
    this slide has *emphasized text*
- | 
    this slide has
    two lines of text
- | 
    this slide has [a link](github.com/hawkw/bigyll)
---
```
This is due to issues in the way Jekyll parses YAML front-matter. I'm looking into a workaround but for now, just keep that in mind.


#### Styles:
There's now support for @mdnzr's [fork](https://github.com/mdznr/big), which sizes text using the golden ratio, and @jed's [weenote](https://github.com/jed/weenote), for making [Takahashi](http://en.wikipedia.org/wiki/Takahashi_method)-style presentations. Just use the `big-mdnzr` or `big-weenote` layouts instead of the default `big` layout.

### To-do:

 -[x] Include the JS and CSS in a site-level directory and link them in.
 -[ ] Maybe add support for [big-themes](https://github.com/tmcw/big-themes)
 -[ ] Make it possible to write presentations with the Markdown syntax from [big.py](https://github.com/harperreed/bigpy)

