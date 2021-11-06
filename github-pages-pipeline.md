# GitHub Pages Pipeline – Challenge 

ADA Pipeline is an open-source collaborative book authoring workflow that outputs as a multi-format finished publication, with automatic typesetting, and versioning. The output formats targets are: website, paginated web, screen PDF, print-on-demand PDF, eBook, and source. ADA chains together different tools in as an extensible pipeline, currently including the following key applications: Fidus Writer, Vivliostyle, and GitHub.

Over 20 books have been made with over 100 authors using ADA.

Here are two example books, one using Jekyll and the other Hugo for website display.

  - Should Schools Reopen? – https://github.com/Independent-SAGE/Should-Schools-Reopen
  - Krisenmanagement – https://github.com/akademie-oeffentliches-gesundheitswesen/krisenmanagment

If you would like to try out the system email or DM Simon Worthington, simon.worthington@tib.eu – @mrchristian99

  - Fidus Writer instance – https://write.handbuch.io/
  - ADA Information – https://github.com/TIBHannover/ADA

## The problem that needs to solve

Our problem is producing Markdown that will work with GitHub Pages.

The pipeline outputs a variety of file formats and any of these could be used for a tranformation to Markdown.

It important to look at these new output file examples ( > 4 Nov 21) as output file markup has been changed over time.

See files here: https://github.com/TIBHannover/ADA-Reference-Publication

Other respositories will have older file types with outdated markup.

Output formats include:

  -  HTML as a unified file
  -  Multifile HTML
  -  Unzipped EPUB
  -  EPUB
  -  LaTeX 

## Ideas for options to solve the problem

For both options the ADA Pipeline is designed in a way that the user forks a template repository from our master repository and then writes their book source file automatically to the forked repository. This template repository still need to be made, but can quickly be put together.

  1. Better Markdown conversion with CI on GitHub
  2. Use a source file, e.g., the unified single HTML files and render this is GitHub Pages

### Options explained

#### 1. Better Markdown conversion with CI on GitHub

We have used a variety of tools to generate markdown but each options has problems. One eample was with R, 'fidus2GitHub' https://github.com/akademie-oeffentliches-gesundheitswesen/fidus2github 

What we need is a process to take one of our output files and and convert it to Markdown and make it work with this framework / theme – Docsify https://docsify.js.org/#/

The idea would be that we find a library for Markdown transformation, have a CI process running on GitHub, then process files and output on for GitHub Pages to serve the files.

If the user adds new source files to GitHub pages then the CI would be processed and new Markdown files generated.

For the Docsify theme files need to be placed in a specific directory. For some settings of the theme some additional field content needs inputting, this could be done by direct file editing on GitHub.

#### 2. Use a source file, e.g., the unified single HTML files and render this is GitHub Pages

A more elegant option is to use the unified HTML output as Markdown only gets rendered back to HTML for display.

The idea would be that a piece of JavaScript would need to be written to make the navigation menu similar to how the different Markdown frameworks to. And we need and a few other features.

This option also does away with a CI process being needed.

The process could also use some standard web CSS framework.

## What we need the system to do

Our current semi-automatic process has following features that we need to replace in this new solution to our problem.

  1. Present the book in the same way the current Docsity setup does - https://health-sprints.github.io/Should-Schools-Reopen/#/report/chapter_0
  2. Produce a navigation menu from the document headers
  3. Add title at top of navigation
  4. Be mobile first
  5. Have a previous, next at the bottom of chapters, which are defined as H2 by Fidus Writer. The 'previous, next' might not be needed in the unified HTML files, as opposed to other source versions which are multi-document types.
  6. Have a fixed header set of menus that link to files on GitHub for the different versions: webbook, PDF, eBook, print-on-demand page, GitHub source, verion history, release history and publisher. These links can mostly be static links as we have a set directory structure for the book.
  7. Adding GitHub Release number and GitHub Version number added to the site somehow as showing version histories is important to our publishing project. A simple approach here is only to Releases and that way these can be added in book info and metadata by the author.

## Current workflow



## Applications used

  - Fidus Writer – Real-time collaborative web based academic wordprocessor / https://www.fiduswriter.org/
  - Vivliostyle – CSS Typesetting / https://vivliostyle.org/
  - GitHub and GitHub Pages – 
  - Docsify – Site genertor / https://docsify.js.org/#/?id=docsify
  - Datacite – DOIs 
  - ORCID – Author PIDs 
  - Thoth – Single source metadata generator / https://thoth.pub/
  - WikiData – Book Graph / early example of an inputted book – Citizen Science Skilling for Library Staff, Researchers, and the Public –  https://www.wikidata.org/wiki/Q108784094
  - WikiCommons – Deposit
  - Open Library –  
  - Ingram Spark – 
  - Ingram Lightning Source – 
  - Acamdemic Repository – 
  - Amazon Seller Central – 

## Workflow


---
