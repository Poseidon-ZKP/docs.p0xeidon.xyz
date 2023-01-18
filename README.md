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

*For any changes made within this repo, you must git push first and then run npm run build to see the changes.

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

# To Setup Mermaid Enviornment 
0. Make sure you have installed asciidoctor
```
brew install asciidoctor
```
1. Generate a Gem file using following command
```
bundle init 
```
2. Open the Gemfile, and then copy paste the following code
```
source "https://rubygems.org"
gem 'asciidoctor-diagram'
gem "asciidoctor-mermaid"
```
3. Then execute bundle in terminal by typing the following command
```
bundle
```

# To create a Mermaid diagram, run the following command
1. Create a new adoc specifically for diagrams in a folder, e.g. the diagram.adoc in zkGroup folder

2. Put your Mermaid diagram in following syntax 

```
[mermaid, target="circuit", format=png]
....
/* Mermaid Diagram Syntax*/
....

```

Where target means the target name, format means the output file type

3. Then run the following command
```
 asciidoctor -r asciidoctor-diagram -D Poseidon-ZK-Contracts/modules/ROOT/images  Poseidon-ZK-Contracts/modules/ROOT/pages/zk-primitives/zk-group/diagram.adoc
```
Please change the last path "Poseidon-ZK-Contracts/modules/ROOT/pages/zk-primitives/zk-group/diagram.adoc" to the path of you desired diagram.adoc

4. Finally put the following image link to the adoc where you want to display the image, for example, if you go to circuit.adoc, you can see the following line:

```
image::circuit.png[circuit]
```

**Note** 
1. Everytime you add new thing to the diagram, you the change will apply to the same file name so you don't need to worry about rename it. 
2. Also, you don't need to specify any path to the image since all images are default to be sit inside the images folder at ROOT folder.
3. After changing the mermaid labeling, the github will no longer show the diagram correctly, please checkout the vercel deployment or your local build for latest update. Vercel deployment address is at the top of the ReadMe.

For more information, please check out this link: https://docs.asciidoctor.org/diagram-extension/latest/#generating-a-diagram-from-a-terminal

