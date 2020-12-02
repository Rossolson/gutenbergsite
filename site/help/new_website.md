---
layout: default
title: New Website 2020 | Project Gutenberg
permalink: /help/new_website.html
---

New Website 2020
================

On August 26 2020, the Project Gutenberg website underwent some major changes. These changes had been previewed since early 2020, and visitors to the old site were invited to try the new site, including giving input via a brief survey.

The old site is no longer available. If you found yourself on this page unexpectedly, it is because an old page was redirected here.

Please use the navigation menus at the top of the page to find what you were looking for. All of the functionality, and most of the content, from the old site is still here - but in a different location.

Below, find a description of the motivation behind the changes. Also find a description of known issues, and the items that were not brought to the new website (and how to find archived copies).

THANK YOU for your patience as we continue to update the website to fix remaining problems, and maintain all the functionality and content that visitors expect. If you encounter an issue not described below, or have a suggestion, please email help2020@pglaf.org (details below on other ways of reporting issues).


## Known issues and "TO DO" items

### Updates on fixed items
Let us know if you are still having trouble with these:
- OPDS: Issues resolved
- Kindle: Issues resolved
- Bookshelf detailed listings: Issues resolved

### Functionality issues
1. Redirected pages go from https to http inappropriately. For example, https://www.gutenberg.org/catalog redirects properly but changes to http://www.gutenberg.org/ebooks .. this seems to happen with some search pages, also. Status: Investigating. This looks like an issue with redirect syntax or server config.

### Content issues
1. Need to create a new version of the mention of https://www.gutenberg.org/wiki/Gutenberg:Help_on_Bibliographic_Record_Page from bibrec (help text, appears 4x on each bibrec page linked with the question mark from the dropbox, gdrive and onedrive icons). Also a description of epub, mobi, and other formats. Status: Under development.
2. PDF blank or broken pages. Automated PDF is a new feature that is not fully functional yet. If you find a broken PDF, it should be fixed during upcoming weeks. Meanwhile, use the HTML or other formats - this is the same content as will eventually be in PDF. Status: Fixes ongoing.
3. New mobile bibrec page display. We will move content table below book cover and social links when it's displayed on mobile device. (Working on it)

### User interface and user experience issues
1. OPDS results have a heading, "All Books (sorted by popularity)" regardless of what it is showing. Instead this should be something more generic, like, "<title>Project Gutenberg</title>." Status: Working on it.

### Search-related issues
1. UI/Search: Search output order seems random. Status: Defer. Search is handled by PostgreSQL, and unchanged from the old site.


### Feature requests (things that are not really broken, but would be good to have)
1. Bookshelf editing is not currently available. Bookshelves only have older entries. Most bookshelves had not been updated recently anyway, and we hope to add bookshelf editing capabilities soon. Status: Under development.
2. Bookshelf sorting by author. For example, https://www.gutenberg.org/ebooks/bookshelf/16?sort_order=title&start_index=26 can sort alphabetically by title, but not by author. The sort field is already part of the request (sort_order=title), so sorting by other fields seem viable. Status: Working on it.
3. Long lists should have "Last" as well as First and Next. For example, http://www.gutenberg.org/ebooks/bookshelf/68. Status: Should be possible for bounded lists such as bookshelves, but an attempt to implement this for all lists resulted in severely degraded website performance.
4. The "new books" pane at https://www.gutenberg.org has a pop-up tooltip that mentions the title. Status: Working on it.
5. Fielded search and ordering. If results were presented in a table where any field could be included, such as Author, Title, Language, LC code, subject, bookshelf, release date, most recent update... THEN people could select a column and have results sorted by that column. Status: This is of interest, and non-trivial to implement.

### Items that will not be fixed
1. Wiki "user" pages. These have not been maintained, and are no longer part of the site. Archived pages are likely available at the Wayback machine, https://wayback.archive.org -- first enter the URL (such as https://www.gutenberg.org or a more specific link), then select the date of the archive snapshot to view the removed page.
2. Translated pages. These have not been maintained, and are no longer part of the site. The Wayback machine, again, likely has archived copies.
3. Mobile site (http://m.gutenberg.org) was retired, since the new website is responsive for smaller screens and has all the same functionality. This retirement was originally planned to happen later, but the site was unmaintained and had some issues that forced early retirement. We apologize there was not adequate notice for this change.
4. Bookshelves have lost their hierarchy and metadata. We have the key=value pair for lowest-level bookshelf membership, but not the group it was part of. For example, here is what the top-level grouping for Canada used to look like: https://web.archive.org/web/20200229062612/http://www.gutenberg.org/wiki/Canada_(Bookshelf) .. currently, you can find books in the right category. This, for example, is in "Canada:" https://www.gutenberg.org/ebooks/53929 .. however, the Canada bookshelf doesn't list the granularity, such as by putting #53929 in Autobiography/biography under Canada. Basically, the hierarchy is not presented. Status: being considered as part of the bookshelf ediing tool under Feature Requests. Bookshelves are now database entries, rather than Wiki pages, and the hierarchical structure presentation is not being presented.
5. "Your app is broken." Project Gutenberg does not have, and has never had, an app. Project Gutenberg eBooks require no special apps to read, just the regular Web browsers or eBook readers that are included with computers and mobile devices. No app is required to enjoy Project Gutenberg eBooks. IF YOU ARE HAVING TROUBLE WITH AN APP, it is not an app from Project Gutenberg. Any support/fixes will need to come from whoever made the app. Note that some apps used our OPDS feed, which had some problems that have been fixed.


# New Website Overview

The Project Gutenberg website, along with some of its back-end functionality, has undergone major updates in 2019 and 2020. On August 26 2020, the legacy site was retired and the new site went into service - this followed over six months of public "beta" testing, when members of the public were invited to visit the new site and give input (including a brief anonymous survey).

Input, fixes and suggestions are welcome. The website is still undergoing development, and the basic look-and-feel (menus, colors, fonts, etc.) has been updated with the new design.


## Goals

Goals for the website redesign and back-end updates include:

* Modernize the website, including a responsive design and updated content. Deprecation or removal of outdated content. 
* Abandonment of non-English website pages, which generally have been unmaintained for years. (Interest in non-English eBooks remains strong, and there has been no decrease in the enthusiasm for non-English eBooks.)
* Utilize HTML version 5 and Cascading Style Sheets for the entire experience. The site no longer requires Javascript, and uses dynamically-generated pages only for eBook landing pages and search results. 
* Discontinue the mobile site (previously at http://m.gutenberg.org), which was unmaintained and utilized older-style PHP that was vulnerable to mis-use.
* Stop utilizing MediaWiki for the main pages. Instead, write page content in Markdown. Propagate the content to the website automatically, with HTML5+CSS for layout, menus, etc.
* Make the whole website content publicly available for edit suggestions. We are using github for this. 
* Make the metadata and site structure more easily mirrorable, whether in bulk or for subsets. This is partially done by using github for website content. In the future, we plan to make landing pages use static HTML5+CSS, instead of via autocat3 (below).
* In the future, we hope to make the eBooks themselves available similarly (via github). This will facilitate reader-contributed formats, as well as new methods for errata reporting and fixes.

## How to provide input, fixes and suggestions

Please first check above in case your suggestion is already being worked on.

### General reporting of errors

First, if you find an error, typo, etc. within an eBook you can report it using the [regular mechanisms](/help/errata.html). The eBooks themselves are exactly the same on this new site as on the old (i.e., the exact same files).

If you are not sure how to report a problem you find, it's fine to just email help2020@pglaf.org. It will get to the right person.

### Layout and design

If you have suggestions or find problems with the website pages (i.e., not the eBooks, but the various other items like the "help" and "about" pages), please report them.

Easiest might be email help2020@pglaf.org. Or, you could join the [gutvol-d](https://lists.pglaf.org) mailing list to bring up your suggestions.

### Typos, wording changes, etc.

The words and structure of the website are in a [github repository](https://github.com/gbnewby/gutenbergsite), and are available for submission of issues, pull requests, or examination.

You can also suggest changes or report problems as described above for layout and design.

### Generated formats

A new version of [ebookmaker](https://github.com/gutenbergtools/ebookmaker) went into production in late December 2019. This is what creates our EPUB and MOBI (Kindle) formats. You can run it yourself on the PGLAF upload portal's [ebookmaker test page](https://ebookmaker.pglaf.org).

If you find problems with the generated formats, let us know. The ebookmaker program is under continuous development, and as it is improved we are gradually re-generating all 60,000+ eBooks (and iterating, when further improvements are made).

The link above goes to the github page for ebookmaker. You can submit issue reports or new code ("pull requests") there.

### Compatibility, accessibility, usability

The new website utilizes HTML5 and CSS to provide a single location intended to be suitable for everyone:
* Mobile devices (smartphones etc.).
* Tablets and other touch-screen interfaces.
* Bigger or smaller screens.
* Text-to-speech and text-to-Braille screen readers.
* Suitable for persons with visual impairments, including low vision and color blindness

If you encounter something that doesn't work for you, or could be better, please let us know using one of the methods above. Email help2020@pglaf.org or use one of the other reporting methods described on this page.

It is especially important that we can understand what you are experiencing, and what could be improved. To help with this, please provide a description of how you accessed the website, and the problems encountered. If you know of external testing sites, or standards, or software that we should look into, please let us know.

*Most recently updated: October 8, 2020*
