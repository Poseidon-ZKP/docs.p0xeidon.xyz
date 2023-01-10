# Documentation Website
[Vercel Deployment](https://docs-p0xeidon-xyz.vercel.app/p0x-lab/1.0.0/index.html)

# To Add Page
```
cd modules/ROOT/pages
```
Then go back to the modules/ROOT/ folder, find
```
nav.adoc
```
Follow the structure:
xref: path/to/page[Title of the Page]

# To Link to other pages

```
xref: path/to/page[CustomName]
```

# To Add Anchor (Link to other sections in other page)
1. Add anchor to the page you want link to with [#SectionName]
2. Add reference using 
```
xref: path/to/page#SectionName[CutomName]
```

