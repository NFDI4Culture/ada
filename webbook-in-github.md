# Webbook in GitHub: Specification for a small code package

In a nutshell: For the Handbuch.io project we want to replace the use of Markdown on GitHub Pages as an output format and replace it with XHTML. The reason for this change is that the Markdown transformation isn't needed for GitHub Pages output. We will want Markdown for other outputs and possibly as an authoring format.  

Currently we have to output HTML or XHTML and then transform to Markdown. This is problematic and we lose formats on a number of items: endnotes, footnotes, anchors, images, tables, etc.

## Example content that we want to display

Our output that we want to display in GitHub Pages is EPUB 3.x XHTML (uncompressed) which exports to GitHub automatically.

package xmlns="http://www.idpf.org/2007/opf" version="3.0"

See example XHTML content output: https://github.com/TIBHannover/open-science-guide-of-guides/tree/main/epub/EPUB

## How we make GitHub Pages at present

  1. Create docs, CSS, covers, metadata in Fidus Writer
  2. Export HTML to GitHub and merge with a basic template repo - https://github.com/TIBHannover/open-science-guide-of-guides/tree/main/html
  3. Convert HTML to MD using Cloudconvert https://cloudconvert.com/ - 
  4. Use Jekyl, Hugo, or Docsify to make a Markdown Github Pages website - Docsify is latest framework used https://docsify.js.org/#/
  5. Develop Markdown website locally with lots of minor edits
  6. Serve website from GitHub pages and link to other formats held on GitHub: CSS Typesetting; PDF, EPUB, PoD, sources

## What we want to do

