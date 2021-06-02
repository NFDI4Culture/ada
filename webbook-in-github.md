# Webbook in GitHub: Specification for a small code package

In a nutshell: For the Handbuch.io project we want to replace the use of Markdown on GitHub Pages as an output format and replace it with XHTML. The reason for this change is that the Markdown transformation isn't needed for GitHub Pages output. We will want Markdown for other outputs and possibly as an authoring format.  

Currently we have to output HTML or XHTML and then transform to Markdown. This is problematic and we lose formats on a number of items: endnotes, footnotes, anchors, images, tables, etc.

## Example content that we want to display

Our output that we want to display in GitHub Pages is EPUB 3.x XHTML (uncompressed) which exports to GitHub automatically.

package xmlns="http://www.idpf.org/2007/opf" version="3.0"

See example XHTML content output: https://github.com/TIBHannover/open-science-guide-of-guides/tree/main/epub/EPUB

## How we make GitHub Pages at present
