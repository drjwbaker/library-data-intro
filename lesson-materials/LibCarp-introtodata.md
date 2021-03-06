# Library Carpentry Week One: Introduction to Data

_____
##Lesson Plan

_____
### Data collection

Conducted as attendees enter the room

Thinking about the program as a whole (the use of regular expressions, the command line, 
Git and OpenRefine), please rate your skill level. Would you say that you know:

a) Nothing
b) A little
c) Lots
d) Lots and lots

_____
### Overview

#### Introduction

Welcome to Library Carpentry! This series of introductory workshops on software skills for librarians started life as an exploratory programme funded by the Software Sustainability Institute and supported by [Software Carpentry](http://software-carpentry.org/) and City University London. Thanks also go to the British Library and the University of Sussex where James Baker, who developed the workshops, worked worked when planning and delivering the workshops. The aim of Library Carpentry is to create a set of tools the community can manage, support, enrich, and reuse as it sees fit. Periodically during the sessions we will collect anonymous feedback that will go into improving the classes and ensuring that they best fit the evolving needs and requirements of the library and information science community.

The rationale for Library Carpentry is twofold. First, as Andromeda Yelton argues in her excellent recent [ALA Library Technology Report](http://journals.ala.org/ltr/issue/view/506) 'Coding for Librarians: learning by example', code is a means for librarians to take control of practice and to empower themselves and their organisation to meet user needs in flexible ways. Second, librarians play a crucial role in cultivating world class research. And in most research areas today world class research relies on the use of software. Librarians with software skills are then well placed to continue that cultivation of world class research.

In order to kick start your exploration of software, this four module program will cover the following: **SLIDE**

- 1: Basics - jargon busting, data structures, and the use of regular expressions
- 2: Controlling data using the command line (in the Unix Shell)
- 3: Versioning data (with Git)
- 4: Cleaning data (with [OpenRefine](http://openrefine.org/))

#### Where to go for help

**SLIDE** 

First, use your skill level stickers to identify people on your table who can help: you will all be following along from the same worksheets, so someone around you may have got past the point you are stuck at. 

Second, there are helpers on hand to help if those around you can't. You should all have access to coloured sticky notes: a pink sticky note on your laptop indicates that you need help (it might also alert the attention of someone around you!). So, please use them. 

Third, before each of the classes, you may be required to install software: all issues doing this should be reported to the Github issues page for the week, posting something there will alert someone to give you help in advance **bring up Github pages**. 

Fourth, and finally, as much of the program is self-directed, we encourage you to finish up or repeat tasks after class time: if you run into issues, again report them to the relevant Github issues page.

#### Final points of admin

**SLIDE** 

Most of the classes will involve following along from a worksheet. Much of the time you will be encouraged to go along at your own pace. For some of you this will feel like a lot of material, for others it might not feel like enough. Remember that the session is introductory. If you finish early, our end time is not a hard stop, so you may of course leave. 

Alternatively, you might want to use the time to search online for more information or advanced skills guides. You may even wish to deepen your own skills by staying around and helping someone else out: there is nothing better for really getting to know something than teaching it to someone else! If you don't finish, don't worry, there are no prerequisites between classes and if you have time, you can always carry on at home.

Finally computers are stupid, can frustrate, and as you all have different machines it can be tricky to resolve problems. Please be patient, particularly if your issue is local. Stepping outside and taking a gulp of fresh air always helps.

#### This week

**SLIDE**

- Jargon Busting (45 minutes)
- Foundations (45 minutes)
- Regular Expressions (45 minutes)

_____
### Jargon Busting (Group Task)

#### Requirements

- boards/pads
- pens
- sticky notes*

####Purpose

- icebreaker
- finding confidence level
- expectation management

####Task

**SLIDE**

This group task is an opportunity for you to get help understanding terms, phrases, or ideas around code or software development that you've come across and perhaps feel you should know better.

- Start by getting into groups of 4 or 5.
- Next make a big list of all the problem terms, phrases, and ideas that come up. Retain duplicates. Then (taking common words as a starting point) work together to try to explain what a term, phrase, or idea means (note: use both each other and the internet as a resource!). Make a note of those your group resolves and those you are still struggling with. **15 minutes**
- **Trainer note**: alongside this make a note of common problem terms, phrases, and ideas that both do and do not map to what Library Carpentry will cover (paying special attention to common problems that will not be covered)
- Report back on an issue resolved by your group **1 minute each**
- **Trainer note**: Report on mapping exercise: what is and isn't going to be covered.

_____
### Foundations

**SLIDE** Before we crack on with using the computational tools at our disposal, I want to spend some time on some foundation level stuff - a combination of best practice and generic skills that frame what we'll be doing over the nest stages of the program.

**Trainer Note**: we recommend using this section as an opportunity to discuss foundational skills that you think are relevant.

#### The Computer is Stupid

**SLIDE** This does not mean that the computer isn't useful. Given a repetitive task, an enumerative task, or a task that relies on memory, it can produce results faster, more accurately, and less grudgingly than you or I. Rather when I say that you should keep in mind that the computer is stupid, I mean to say that computer only does what you tell it to. If it throws up an error it is often not your fault, rather in most cases the computer has failed to interpret what you mean because it can only work with what it knows (ergo, it is bad at interpreting). This is not to say that the people who told the computer what to tell you when it doesn't know what to do couldn't have done a better job with error messages, for they could. So keep in mind as we go along that if you find an error message frustrating, it isn't the computer's fault that it is giving you an archaic and incomprehensible error message, it is a human person's.

#### Why take an automated or computational approach

**SLIDE** Otherwise known as the 'why not do it manually?' question. To start with, I'm not anti-manual. I do plenty of things manually that a machine could do in an automated way because either a) I don't know how to automate the task or b) I'm unlikely to repeat the task and estimate that automating it would take longer. However once you know you'll need to repeat a task, you have a compelling reason to consider automating it. This is one of the main areas in which programmatic ways of doing outside of IT service environments are changing library practice. Andromeda Yelton, a US based librarian closely involved in the Code4Lib movement, put together an excellent American Library Association Library Technology Report called "Coding for Librarians: Learning by Example." The report is pitched at a real world relevance level, and in it Andromeda describes scenarios library professionals told her about where learning a little programming, usually learning ad-hoc, had made a difference to their work, to the work of their colleagues, and to the work of their library.

Main lessons:

- **Borrow, Borrow, and Borrow again**. This is a mainstay of programming and a practice common to all skill levels, from professional programmers to people like us hacking around in libraries;
- **The correct language to learn is the one that works in your local context**. There truly isn't a best language, just languages with different strengths and weaknesses, all of which incorporate the same fundamental principles;
- **Consider the role of programming in professional development**. That is both yours and of those you manage;
- **Knowing (even a little) code helps you evaluate projects that use code**. Programming can seem alien. Knowing some code makes you better at judging the quality of software development or planning activity that include software development
- **Automate to make the time to do something else!** Taking the time to gather together even the most simple programming skills can save time to do more interesting stuff! (even if often that more interesting stuff is learning more programming skills ...)

**SLIDE: Cost/benefit slide**

#### Keyboard shortcuts are your friend

**SLIDE** Though we will get more computational over the course of the programme, we can start our adventure into programming - as many of you will have already - with very simple things like keyboard shortcuts. We all have our favourites. Labour saving but also exploiting this stupid machine in the best possible way. Alongside the very basic ones (ctrl+s for save; ctrl+c for copy; ctrl+x for cut; ctrl+v for paste) my favourite (in a Windows or Linux machines) is alt+tab, a keyboard shortcut that switches between programs {**Trainer note**: ask other helpers what their favourites are}. You can do all the lessons in Library Carpentry without keyboard shortcuts, but note that they'll likely come up a lot.

#### Plain text formats are your friend

**SLIDE** Why? Because computers can process them!

If you want computers to be able to process your stuff, try to get in the habit where possible of using platform-agnostic formats such as .txt for notes and .csv or .tsv for tabulated data (the latter pair are just spreadsheet formats, separated by commas and tabs respectively). These plain text formats are preferable to the proprietary formats used as defaults by Microsoft Office because they can be opened by many software packages and have a strong chance of remaining viewable and editable in the future. Most standard office suites include the option to save files in .txt, .csv and .tsv formats, meaning you can continue to work with familiar software and still take appropriate action to make your work accessible. Compared to .doc or .xls, these formats have the additional benefit of containing only machine-readable elements. Whilst using bold, italics, and colouring to signify headings or to make a visual connection between data elements is common practice, these display-orientated annotations are not (easily) machine-readable and hence can neither be queried and searched nor are appropriate for large quantities of information (the rule of thumb is if you can't find it by CTRL+F it isn't machine readable). Preferable are simple notation schemes such as using a double-asterisk or three hashes to represent a data feature: in my own notes, for example, three question marks indicate something I need to follow up on, chosen because `???` can easily be found with a CTRL+F search.

`???` was also chosen by me because it doesn't clash with existing schemes. Though it is likely that notation schemes will emerge from existing individual practice, existing schema are available to represent headers, breaks, et al. One such scheme is Markdown, a lightweight markup language. Markdown files are as .md, are machine readable, human readable, and used in many contexts - GitHub for example, renders text via Markdown. An excellent [Markdown cheat sheet is available on GitHub](https://github.com/adam-p/markdown-here) for those who wish to follow – or adapt – this existing schema. Notepad++ http://notepad-plus-plus.org/ is recommended for Windows users as a tool to write Markdown text in, though it is by no means essential for working with .md files. Mac or Unix users may find Komodo Edit, Text Wrangler, Kate, or Atom helpful. Combined with [pandoc](http://pandoc.org/), a markdown file can be exported to PDF, LaTeX or other formats, so it is a great way to create machine-readable, easily searchable documents that can be repurposed in many ways. It is a universal document converter.

#### Naming files sensible things is good for you and for your computers

**SLIDE** Working with data is made easier by structuring your stuff in a consistent and predictable manner.

Why?

Without structured information, our lives would be much poorer. As library and archive people we know this. But I'll linger on this a little longer because for working with data it is especially important.

Examining URLs is a good way of thinking about why structuring research data in a consistent and predictable manner might be useful in your work. Good URLs represent with clarity the content of the page they identify, either by containing semantic elements or by using a single data element found across a set or majority of pages.

**look at webpages** A typical example of the former are the URLs used by news websites or blogging services. WordPress URLs follow the format:

-   `ROOT/YYYY/MM/DD/words-of-title-separated-by-hyphens`
-   <http://cradledincaricature.com/2015/07/24/code-control-and-making-the-argument-in-the-humanities/>

A similar style is used by news agencies such as a *The Guardian* newspaper:

-   `ROOT/SUB_ROOT/YYYY/MMM/DD/words-describing-content-separated-by-hyphens`
-   <http://www.theguardian.com/uk-news/2014/feb/20/rebekah-brooks-rupert-murdoch-phone-hacking-trial>

In archival catalogues, URLs structured by a single data element are often used. The NLA's TROVE structures its online archive using the format:

-   `ROOT/record-type/REF`
-   <http://trove.nla.gov.au/work/6315568>

And the Old Bailey Online uses the format:

-   ROOT/browse.jsp?ref=REF`
-   <http://www.oldbaileyonline.org/browse.jsp?ref=OA16780417>

What we learn from these examples is that a combination of semantic description and data elements make for consistent and predictable data structures that are readable both by humans and machines. Transferring this to your stuff makes it easier to browse, to search, and to query using both the standard tools provided by operating systems and by the more advanced tools Library Carpentry will cover.

In practice, the structure of a good archive might look something like this:

- A base or root directory, perhaps called 'work'.
- A series of sub-directories such as 'events', 'data', ' projects' et cetera
- Within these directories are series of directories for each event, dataset or project. Introducing a naming convention here that includes a date element keeps the information organised without the need for subdirectories by, say, year or month.

All this should help you remember something you were working on when you come back to it later (call it real world preservation).

The crucial bit for our purposes, however, is the file naming convention you choose. The name of a file is important to ensuring it and its contents are easy to identify. 'Data.xslx' doesn't fulfil this purpose. A title that describes the data does. And adding dating convention to the file name, associating derived data with base data through file names, and using directory structures to aid comprehension strengthens those connection.

To recap, the key points about structuring your data are:

-   Data structures should be consistent and predictable
-   Consider using semantic elements or data identifiers to data directories
-   Fit and adapt your data structure to your work
-   Apply naming conventions to directories and file names to identify
    them, to create associations between data elements, and to assist
    with the long term readability and comprehension of your data
    structures

_____
### Regular Expressions

**SLIDE** One of the reason why I have stressed the value of consistent and predictable directory and filenaming conventions is that working in this way enables you to use the computer to select files based on the characteristics of their file name. So, for example, if you have a bunch of files where the first four digits are the year and you only want to do something with files from '2014', then you can. Or if you have 'journal' somewhere in a filename when you have data about journals, you can use the computer to select just those files then do something with them. Equally, using plain text formats means that you can go further and select files or elements of files based on characteristics of the data *within* files.

A powerful means of doing this selecting based on file characteristics is to use regular expressions, often abbreviated to regex. A regular expression is a sequence of characters that define a search pattern, mainly for use in pattern matching with strings, or string matching, i.e. "find and replace"-like operations. Regular expressions are typically surrounded by `/` characters, though we will (mostly) ignore those for ease of comprehension. Regular expressions will let you:

- Match on types of character (e.g. 'upper case letters', 'digits', 'spaces', etc.)
- Match patterns that repeat any number of times
- Capture the parts of the original string that match your pattern

As most computational software has regular expression functionality built in and as many computational tasks in libraries are built around complex matching, it is good place for Library Carpentry to start in earnest.

**SLIDE** A very simple use of a regular expression would be to locate the same word spelled two different ways. For example the regular expression `organi[sz]e` matches both "organise" and "organize".

A very simple use of a regular expression would be to locate the same word spelled two different ways. For example the regular expression `organi[sz]e` matches both "organise" and "organize".

But it would also find `reorganise`. So there are a bunch of special syntax that help us be more precise.

The first we've seen: square brackets can be used to define a list or range of characters to be found. So: **SLIDE**

- `[ABC]` matches A or B or C
- `[A-Z]` matches any upper case letter
- `[A-Za-z0-9]` matches any upper or lower case letter or any digit (note: this is case-sensitive)

Then there are: **SLIDE**

- `.` matches any character
- `\d` matches any single digit
- `\w` matches any part of word character (equivalent to `[A-Za-z0-9]`)
- `\s` matches any space, tab, or newline
- `\` NB: this is also used to escape the following character when that character is a special character. So, for example, a regular expression that found `.com` would be `\.com` because `.` is a special character that matches any character.
- `^` asserts the position at the start of the line. So what you put after it will only match the first characters of a line or contents of a cell.
- `$` asserts the position at the end of the line. So what you put after it will only match the last character of a line of contents of a cell.
- `\b` adds a word boundary. Putting this either side of a stops the regular expression matching longer variants of words. So:
	- the regular expression `foobar` will match `foobar` and find `666foobar`, `foobar777`, `8thfoobar8th` et cetera
	- the regular expression `\bfoobar` will match `foobar` and find `foobar777`
	- the regular expression `foobar\b` will match `foobar` and find `666foobar`
	- the regular expression `\bfoobar\b` will find `foobar`

**SLIDE** {**Question**}: So, what is `^[Oo]rgani.e\b` going to match.

Other useful special characters are **SLIDE**:

- `*` matches when the preceding character appears any number of times including zero
- `+` matches when the preceding character appears any number of times excluding zero
- `?` matches when the preceding character appears one or zero times
- `{VALUE}` matches the preceding character the number of times define by VALUE; ranges can be specified with the syntax `{VALUE,VALUE}`
- `|` means or.

{**Questions**}: So, what are these going to match?

- **SLIDE** `^[Oo]rgani.e\w*`
- **SLIDE** `[Oo]rgani.e\w+$`
- **SLIDE** `^[Oo]rgani.e\w?\b`
- **SLIDE** `^[Oo]rgani.e\w?$`
- **SLIDE** `\b[Oo]rgani.e\w{2}\b`
- **SLIDE** `\b[Oo]rgani.e\b|\b[Oo]rgani.e\w{1}\b`

**SLIDE** This logic is super useful when you have lots of files in a directory, when those files have logical file names, and when you want to isolate a selection of files. Or for looking at cells in spreadsheets for certain values. Or for extracting some data from a column of a spreadsheet to make  new columns. I could go on. The point is, it is super useful in many contexts. To embed this knowledge we won't - however - be using computers. Instead we'll use pen and paper. I want you to work in teams of 4 to work through the exercises in the handout. I have an answer sheet over here if you want to check where you've gone wrong. When you finish, I'd like you to split your team into two groups and write each other some tests. These should include a) strings you want the other team to write regex for and b) regular expressions you want the other team to work out what they would match. Then test each other on the answers. If you want to check your logic, use [regex101](https://regex101.com/), [myregexp](http://myregexp.com/) or [regexper.com](http://regexper.com/): the first two help you see what text your regular expression will match, the latter visualises the workflow of a regular expression.

#### Exercise

What does `Fr[ea]nc[eh]` match?

- this matches `France`, `French`, `Frence`, and `Franch`. It would find words where there were characters either side of these so `Francer`, `foobarFrench`, or `Franch911`.

What does `Fr[ea]nc[eh]$` match?

- this matches `France`, `French`, `Frence`, and `Franch` at the end of a line. It would find words where there were characters before these so `foobarFrench`.

What would match the strings `French` and `France` only that appear at the beginning of a line?

- `^France|^French` This would also find words where there were characters after `French` such as `Frenchness`.

How do you match the whole words `colour` and `color` (case insensitive)?

- In real life, you *should* only come across the case insensitive variations `colour`, `color`, `Colour`, `Color`, `COLOUR`, and `COLOR` (rather than, say, `coLour`. So one option would be `\b[Cc]olou?r\b|\bCOLOU?R\b`. This can, however, get quickly quite complex. An option we've not discussed is to take advantage of the `/` delimiters and add an ignore case flag: so `/colou?r/i` will match all case insensitive variants of `colour` and `color`.

How would you find the whole-word `headrest` and or the 2-gram `head rest` but not `head  rest` (that is, with two spaces between `head` and `rest`?

- `\bhead ?rest\b`. Note that although `\bhead\s?rest\b` does work, it would also match zero or one tabs or newline characters between `head` and `rest`. In most real world cases it should, however, be fine :)

How would you find a 4 letter word that ends a string and is preceded by at least one zero?

- `0+[a-z]{4}\b`

How do you match any 4 digit string anywhere?

- `\d{4}`. Note this will match 4 digit strings only but will find them within longer strings of numbers.

How would you match the date format `dd-MM-yyyy`?

- `\b\d{2}-\d{2}-\d{4}\b` In most real world situations, you are likely to want word bounding here (but it may depend on your data).

How would you match the date format `dd-MM-yyyy` or `dd-MM-yy` at the end of a string only?

- `\d{2}-\d{2}-\d{2,4}$`

How would you match publication formats such as `British Library : London, 2015` and `Manchester University Press: Manchester, 1999`?

- `.* : .*, \d{4}` You will find that this matches any text you put before `British` or `Manchester`. In this case, this regular expression does a good job on the first look up and may be need to be refined on a second depending on your real world application.

_____
## Next module

**SLIDE**

Shell. Instructions of what to install per operating system on the Github page.


_____
### References

James Baker , "Preserving Your Research Data," *Programming Historian* (30 April 2014), [http://programminghistorian.org/lessons/preserving-your-research-data.html](http://programminghistorian.org/lessons/preserving-your-research-data.html). The sub-sections 'Plain text formats are your friend' and 'Naming files sensible things is good for you and for your computers' are reworked from this lesson.

Owen Stephens, "Working with Data using OpenRefine", *Overdue Ideas" (19 November 2014), [http://www.meanboyfriend.com/overdue_ideas/2014/11/working-with-data-using-openrefine/](http://www.meanboyfriend.com/overdue_ideas/2014/11/working-with-data-using-openrefine/). The section on 'Regular Expressions' is reworked from this lesson developed by Owen Stephens on behalf of the British Library

Andromeda Yelton, "Coding for Librarians: Learning by Example", *Library Technology Reports* 51:3 (April 2015), doi: [10.5860/ltr.51n3](http://dx.doi.org/10.5860/ltr.51n3)

Fiona Tweedie, "Why Code?", *The Research Bazaar* (October 2014), [http://melbourne.resbaz.edu.au/post/95320810834/why-code](http://melbourne.resbaz.edu.au/post/95320810834/why-code)
