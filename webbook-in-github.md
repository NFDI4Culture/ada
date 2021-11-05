# Creating GitHub Page Pipeline

We have an existing book publishing pipeline, the 'ADA Pipeline' that deposits files on GitHub. The pipeline then uses GitHub pages to display a website for a book.

ADA is an open-source pipeline to enable collaborative book authoring and output as multi-format finished publication that have automatic typesetting,  and revisioning, as: website, paginated web, PDF, print-on-demand, eBook, and source. ADA chains together different tools in extensible pipelines: Fidus Writer, Vivliostyle, and GitHub.

Over 20 books have been made with over 100 authors.

Here are two example books, one using Jekyll and the other Hugo for website display.

  - Example 1
  - Example 2

Our problem is producing Markdown that will work with GitHub pages.

The pipeline outputs a variety of file formats, any of these could be used to tranform to Markdown.

Formats:

  -  HTML as a unified file
  -  Format2

See files here: 

## Ideas for options to solve the problem

For both options the ADA Pipeline is designed in a way that the user forks a template repository from our master repository and then writes their book source file automatically to the forked repository.

  1. Better Markdown conversion with CI on GitHub
  2. Use a source file, e.g., the unified single HTML files and render this is GitHub Pages

### Options explained

1. Better Markdown conversion with CI on GitHub

We have used a variety of tools to generate markdown but each options has problems. One eample was with R, LINK. 

What we need is a process to take one of our output files and and convert it to Markdown and make it work with a Hugo GitHub Pages template. Currently we use this Theme / Framework NAME and LINK.

The idea would be that we find a library for Markdown converstion, have a CI process running on GitHub, then process files and output on for GitHub Pages to read the files.

If the user adds new source files to GitHub pages then the CI would be processed and new Markdown files generated.

For the Hugo theme files need to be placed in a specific directory. For some settings of the theme some additional field content needs inputting, this could be done by direct file editing on GitHub.

3. Use a source file, e.g., the unified single HTML files and render this is GitHub Pages

A more elegant option is to use the unified HTML output as Markdown only gets rendered by to HTML by GitHub Pages.

The idea would be that a piece of Javascript would need to be written to make the navigatio menu we need and to dd other features.

This option also does away with a CI process being needed.

The process could also use some standard web CSS framework as well for styling like Bootstrap.

## What we need the system to do

Uur current manual process and GitHub Pages Hugo use gives us the following features that we need to replace.



## Current workflow




---


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

We want to make websites like this Jekyll site from the decompressed XHNTL of an EPUB 3.0 - [Der Kinder-und Jugendgesundheitsdienst](https://akademie-oeffentliches-gesundheitswesen.github.io/KJGD/)

Use the EPUB XHTML like so - https://github.com/TIBHannover/open-science-guide-of-guides/tree/main/epub

Apply the Webbook unoficial standrad and W3C manifest.

Render as a website and have ToC work as menu linking to content headers.

Be able to apply CSS stylesheets, so as to change template style.

Apply CSS template from Fidus Writer or direct from GitHub Template repo.

Have connect to other formats stored in same repo.

Have required metadata and setting inputted.

## Stage 3

Combine W3C Publication Manifest (W3C 2020) https://www.w3.org/TR/pub-manifest/ with WebBook Level 1 (Unofficial Proposal Draft by Daniel Glazman http://glazman.org/e0/webbook.html
