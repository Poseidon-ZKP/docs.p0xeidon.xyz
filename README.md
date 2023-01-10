# Documentation Website
[Vercel Deployment](https://docs-p0xeidon-xyz.vercel.app/)

# To run the site
```
git add . && git commit -m "message"
git push
npm run build
```
Then go to folder build/site/
Drage the index.html file to the browser to view the result.

**For any changes made within this repo, you must git push first and then run npm run build**

# To Add Page
```
cd modules/ROOT/pages
```
Then go back to the modules/ROOT/ folder, find
```
nav.adoc
```
Follow the structure:
```
xref: path/to/page[Title of the Page]
```

# To Link to other pages

```
xref: path/to/page[CustomName]
```

# To Add Anchor (Link to other sections in other page)
1. Add anchor to the page you want link to with
```
[#SectionB]
```
2. Add reference using 
```
xref: path/to/page#SectionB[SectionB]
```

