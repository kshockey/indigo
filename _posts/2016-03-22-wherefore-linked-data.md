---
layout: post
title: "Wherefore art thou, linked data?"
date:   2016-03-22
categories:
tags: linked data, metadata, scholarship
---

Listen up, [preachers of linked data in libraries](http://www.thedigitalshift.com/2016/02/roy-tennant-digital-libraries/broken-furniture-and-blood-on-the-floor/):

**The record is not going away. It absolutely should not go away.**

In other words:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">This is good, but re: &quot;shackles,&quot; we now have <a href="https://twitter.com/hashtag/SHACL?src=hash">#SHACL</a>. Links must be bundled/bounded in some way or other. <a href="https://twitter.com/rtennant">@rtennant</a> <a href="https://t.co/OVsjZiMMjb">https://t.co/OVsjZiMMjb</a></p>&mdash; Tim Thompson (@timathom) <a href="https://twitter.com/timathom/status/712291910061318145">March 22, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/kshockey04">@kshockey04</a> I often feel like metadata creators and library technologists are talking past each other.</p>&mdash; Erin Leach (@erinaleach) <a href="https://twitter.com/erinaleach/status/712291193682526209">March 22, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

You keep saying it is and all that means is you have no concept of the history of documentation[^1]. You cannot see the forest for its trees (or the links for their semantic meaning). You are talking past library technologists and metadata workers and catalogers and you are wrong[^2]. You are wrong and you are slowing the adaption of linked data technologies in libraries just as much as those who stick to old practices of documentation for their own convenience. For the sake of both parties, we need to clear things up.

# The Library and Documentation

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">I still don&#39;t get it. Linked data is like physics to me: brain can&#39;t won&#39;t don&#39;t. <a href="https://t.co/jueoM57ukP">https://t.co/jueoM57ukP</a></p>&mdash; Emily Drabinski (@edrabinski) <a href="https://twitter.com/edrabinski/status/712287428002840576">March 22, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
<br />
[I mean, does this make any sense to you?](http://experiment.worldcat.org/entity/work/data/2406166) Exactly.

That some of my most intelligent librarian friends "don't get it" is not an indictment of them. The document and its metadata have been the history of our profession as long as there has been a profession. Documentation practices that have existed and exist today exist for very thoughtful, deliberate, and intentional reasons. Linked data and the bibliographic record exist to do some of the same things: to describe a thing by making statements about its existence, to gather disparate types of information about a single thing into one place for human readability, and to describe the relationships between different things. One uses a language made for reading punchcards in the 1960s and one takes advantage of the hypertext transfer protocol. Each does other things--MARC records are used for inventory, while linked data has other applications that non-library technologists use for their projects. That said, both live on the shoulders of giants. Consider the bibliographic workform of the original MARC standard--its form and content built on already existing data and documentation standards (card catalog) that were improved over the previous 75 or so years[^3]. The benefits of the MARC bibliographic workform included internal inventory and the ability to disseminate a workform to other libraries that held the same book. Likewise, in the library context (and in corporate and other contexts as well), linked data relies on making a surrogate entity for any and all data that can be described out of existing data and data structures. Chief among these structures include, golly gee, the [Library of Congress authority files](http://id.loc.gov/), the [Virtual International Authority File](https://viaf.org), and other national bibliographic agencies' bibliographic and authority data, as well as popular metadata records written in [Dublin Core](http://dublincore.org/) and [MODS](http://www.loc.gov/standards/mods/). All of these projects are more or less an integral part of library land and have at their founding or early inception heavy feedback from library technologists.

Let me say this again, in another paragraph: you are standing on the shoulders of library data and documentation practices, linked data practitioners. There is no and, but, & or about it.

# A Linked Data Primer

Friend of the blog Ruth Tillman recently wrote a pretty dang good overview of [RDF & linked data for metadata librarians](http://ruthtillman.com/introduction-rdf-librarians-metadata/) that tackles this subject in depth, so defer to that document if you don't know what I mean with some terms in the next section.

Linked data takes advantage of web technologies to provide granular semantic meaning to data and the relationships between data that is computer-readable. It's called linked because it primarily uses the hypertext transfer protocol's ability to create links between not geographically or digitally proximate documents[^4]. The major difference between something like html and a linked data framework like RDF is what the computer is able to infer from the construction of the data. If I was to link to friend of the blog [Emily Drabinski's website](http://www.emilydrabinski.com/), a computer infers the following:

`The literal string "Emily Drabinski's website," when clicked on, should resolve to the domain "http://www.emilydrabinski.com"`

What the semantic web (the new concept of the web that is built on linked data technology) allows you to do is imbue meaning into that statement. You might want to know, for example, who Emily Drabinski is, whether or not this is the same Emily Drabinski that the web domain in the link refers to, and what Emily Drabinski's website is about. Using [first-order logical](https://en.wikipedia.org/wiki/First-order_logic) statements in the form of triples, linked data can model (and presumably in the future visualize)[^5] more meaningful relationships than previous iterations of markup language. Ruth's primer has a pretty good chart for cognitive procession from RDF as a conceptual model to the actual layout of a triple, so I won't duplicate that. What I will illustrate here is how meaning is imbued. Each triple is considered a semantic statement and they can be built upon each other in a network. To understand the statements, you should know that each triple is expressed in the same order: subject-object-predicate. In other words: the subject has a value (the predicate) which is defined by the object. The following is a set of triples about Emily's website in a format called N-Triples[^6]:

Subject | Predicate | Object
------- | ------ | ---------
<http://www.emilydrabinski.com/> | <http://purl.org/dc/terms/creator> | `_:ed`
`_:ed` | <http://www.w3.org/2000/01/rdf-schema#Literal> | Emily Drabinski
`_:ed` | <http://www.w3.org/2002/07/owl#sameAs> | <http://id.loc.gov/authorities/names/n2009061707.html>
`_:ed` | <http://www.w3.org/2002/07/owl#sameAs> | <http://www.goodreads.com/author/show/3422445.Emily_Drabinski>
`_:ed` | <http://purl.org/dc/terms/contributor> | <http://www.goodreads.com/book/show/7867262-critical-library-instruction>

[^7] [^8] [^9]

In plain English, this reads as the following:

(Emily Drabinski's website url) has a creator: `:ed`.<br />
`:ed` is a literal string that reads "Emily Drabinski."<br />
Emily Drabinski is the same as (Emily Drabinski's LoC authority record).<br />
Emily Drabinski is the same as (Emily Drabinski's Goodreads author page).<br />
Emily Drabinski is a contributor to the book *Critical Library Instruction*.

Because there are machine-readable definitions for all of the objects given, the machine can infer some other things that aren't explicitly stated:

 1. Because Emily Drabinski and her authority file are the same AND Emily Drabinski and her Goodreads profile are the same, *Emily Drabinski's authority file and Emily Drabinski's Goodreads profile are the same.*[^10]
 2. Emily Drabinski, all 3 instances of her, both authored her website and contributed (edited) the book *Critical Library Instruction.* This avoids the need to write (authority file) authored (website) and (authority file) edited book AND Goodreads profile authored website and Goodreads profile edited book--4 entire statements--like traditional binary computer programming. Look at how the computer works for you!

Now, this is a very simple construction. I could say a lot more just because I know Emily professionally. To recap: the machine can now infer things about both Emily and the website and the book because we used defined resources to give meaning to the relationships rather than just a literal-to-resolved domain relationship without machine understanding.

# MARC and static data

Cool! we can make more meaningful statements about literally everything! That's so much more useful than MARC!...But legacy data. What can we do with this?

Mr. Tennant seems to think we are highly misguided on this. We are not; we're being library practical again. Here is a point by point breakdown:

  * Links are only useful if they lead to an authoritative source that has something useful to provide.

  >We should have a whole website dedicated to translating library authority files to actionable links that reference sources like Wikipedia deliberately link to...oh. http://id.loc.gov/

  * Simply translating bibliographic data from one format (MARC) to another (BIBFRAME or Schema.org, for example) does not create useful links.

  >The first problem with this point: BIBFRAME has been so thoroughly misguided from its founding documents that it literally models MARC data for linked data purposes. Look at that: a functional[^11] model for MARC data that can be incorporated into linked data with RDF/XML/OWL interoperability. Second: the whole point of linked data is to borrow gratuitously. Bibliographic data can't be borrowed until it exists on the semantic web. It's almost like this is the first step to translating legacy data or something.

  * To achieve true library linked data, individual MARC elements must be turned into actionable entities.

  >Uh, http://bibframe.org/vocab/. A surprising amount of MARC data is actually recursion. I'd be frightened of a schema that attempts to turn every indivudal MARC datum into a linked data resource.

  * Creating actionable entities will require new kinds of processes and services that mostly don’t yet exist.

  >/me pulls out hair. No.

MARC data is semantically imbued already. Semantics in physical documents are inferred by things such as space, place, and code. To illustrate this, we'll continue with *Critical Library Instruction*, [OCLC #:440562980](http://www.worldcat.org/title/critical-library-instruction-theories-and-methods/oclc/440562980). Though today's catalogers are more familiar with the OCLC or their specific ILS's workform for MARC data, the old MARC bibliographic workform places the most important data points near the top left of the document (because that's how we read them as humans). Any guesses as to what they are? If you guessed author and title, pat yourself on the back. Known item searches are one major function of the library catalog and those two data points are the primary ways of knowing an item from a bibliographic standpoint. We'll look at those two elements in the MARC record and dissect their semantic meaning.

>245 10 $a Critical library instruction : $b theories and methods / $c Edited by Maria T. Accardi, Emily Drabinski, and Alana Kumbier.

The first question when students or uninitiated eyes look at that string is "what the heck do those numbers mean?!" That's where [the code](http://www.loc.gov/marc/bibliographic) comes in. Each of those numbers, as well as the delimiters has a specific semantic meaning that dictates what the string means and how it can be used in the MARC standard as well as how it can be displayed with a MARC-compliant OPAC. The Library of Congress MARC website (and OCLC's version of it) is the cipher to making the MARC data human-readable. If we go to the entry for 245, we learn that it is the Title Statement. Without even consulting RDA or AACR2, we can infer that it means "this is the title of the thing."

Okay! So then the title is...$a Critical library instruction : $b theories and methods / $c Edited by Maria T. Accardi, Emily Drabinski, and Alana Kumbier.? I thought the title was just Critical library instruction: theories and methods. The cipher gives the meaning to the delimiters as well: $a is the title, $b is the remainder of title, and $c is the statement of responsibility. That's library jargon, of course--it's the title, subtitle, and author/editor statement. You can see already that MARC has recursion. The statement of responsibility is taken care of in another element field, while "245" and $a seem to mean the same thing. That's why we colloquially refer to it as "245a." The semantic distinction between types and forms of titles are bibliographically specific and require the kind of training that catalogers have in order to parse--it requires knowing the ins and outs of particular formats, what kinds of metadata information those particular formats provide and where, and how to make that metadata work for the user in a MARC-compliant OPAC. To try and say that in a shorter way: the user doesn't care about the difference between "Title," "Title proper," and, "Remainder of title," but that level of granularity is necessary for the cataloger to know for computer parsing, as well as for the librarian to know in order to be able to provide access by unique bibliographic edition[^12].

We express the semantic meaning imbued in MARC data in a different way than an RDF triple word. Turns out humans can mentally manipulate that data to crosswalk it to another semantic model. Consider:

Subject | Predicate | Object
------- | ------ | ---------
OCLC 440562980 | 245 $a | Critical library instruction
OCLC 440562980 | 245 $b | theories and methods
OCLC 440562980 | 245 $c | Edited by Maria T. Accardi, Emily Drabinski, and Alana Kumbier

<br />

Now, a crude method of imbuing "Semantic Web" semantic meaning to these triples, particularly the objects, would be to link them to http://www.loc.gov/marc/bibliographic/bd245.html. However, this still requires a ton of human mediation to make meaning of. Using BIBFRAME, I'm going to make them closer to machine readable.

Subject | Predicate | Object
------- | ------ | ---------
http://www.worldcat.org/oclc/440562980 | [bf:title](http://bibframe.org/vocab/title) | Critical library instruction
http://www.worldcat.org/oclc/440562980 | [bf:subtitle](http://bibframe.org/vocab/subtitle) | theories and methods
http://www.worldcat.org/oclc/440562980 | [bf:responsibilityStatement](http://bibframe.org/vocab/responsibilityStatement) | Edited by Maria T. Accardi, Emily Drabinski, and Alana Kumbier

[^13]

Linked data and MARC data aren't so far off after all. It just requires people who are fluent in the two models and languages to be able to translate. Perhaps our existing tools need updating by someone fluent in both, or we do really need new tools. If you asked me? We need funding and personpower to train people and translate the data through batch processes. Of course, this is a problem because library technologists and cataloging departments especially are woefully understaffed and underfunded in North America, if not in other places.

# Collocation, Or: A record by any other name

The library catalog has two critical functions: to find and locate[^14] a document with a known author, title, or subject; to show what inventory the library has (collocation, in other words)[^12]. The record in a library catalog stands as a surrogate to represent an actual document that is in the library's collection. In other words, records contain metadata about a particular object. Metadata is data is data, which can be linked in the semantic web--the primary application of linked data in libraries, as it currently stands. As Tom said above, data still needs to be bundled. We can imbue all the semantic meaning we want to a particular datum like Emily Drabinski, but it doesn't mean anything until the datum is collocated with other data that sufficiently describes the particular resource in question.

To use an example from above, *Critical Library Instruction* has three main contributors: Emily Drabinski, Alana Kumbier, and Maria T. Accardi. Those three statements independent of each other have particular meaning, but do not make sense as a unit until they are collocated in a single place and presented to humans in a way that makes cognitive sense. Turns out we have a conceptual model for doing that kind of collocation work that is centuries old: the bibliographic record. A surrogate is only as useful as the information it provides the user. Either end of a linked data concept of a "thing" does not prove useful to us: a single RDF triple needs other statements to infer meaning, and linked RDF triples without an human epistemological framework don't mean anything either. Some technologists will tell you that linked data is primarily for computers--this viewpoint misses the fact that computers are tools that humans use; therefore, the tool is only useful if a human can make meaning out of its function. Only in an epistemologically valid framework will the immense benefit of machine inference benefit us.

Enter the record. Linked data gives us the ability to decentralize information about resources and get away from the model of a centralized relational database as a mode of retrieving and displaying information. Linked data also gives us the ability to take semantic shortcuts to devise methods and applications that 1) can be localized in almost infinite ways and 2) allow us to break out of library authority and make full use of the information available to us today as users of the internet. The tools and technology behind the record may become linked data-based, but at the end of the day the user still wants to be able to find what they want with ease, whether the item is known or not. The role of the record in achieving this is pivotal; if we provide a cognitive model that gives too much or too little information, presents the information in a way that is non-intuitive, or requires significant effort to retrieve information, the tool is useless[^15]. Users appreciate the collocation of the information they want about a thing with ease of effort. Think about when you search for the menu of a restaurant. User experience + web architecture research will give you a certain amount of clicks or seconds before the user gives up. The same is true of user studies on library catalogs. How we bundle information to present to users is arguably **more** important than making sure everything is linked; collocating this information in a succinct and useful record remains the primary and best method of presenting a user with information.

In other words: linked data means nothing without proper recording. Stop pretending librarians are held back by the concept of a record. You are wrong.

[^1]: Mr. Tennant is hardly the first to say this. He just happens to be the one I read today.

[^2]: These words sound harsh. However, technologists tend to look over librarians' heads, even when they are [library friendly](2015/07/03/teaching-unsexy.html). I am truly more amenable when we're actually working on a project together. Another note: the shadow conference mentioned in that post was literally the best of my life. I will forever be indebted to how it has shaped the people and things I know. It was not a Bad Thing, it just had the drippings of outside technological social structures as a part of it.

[^3]: And I need not recount how the card catalog was built on the strong documentation of the dictionary catalog.

[^4]: I'm always in awe of how many people don't understand transfer protocols. Web technology uses the hypertext transfer protocol (http://) to connect individual computers to a domain on another computer, or another site on a particular domain. It's why "link" is common terminology--they are "hyperlinks" based on the of the hypertext markup language (html) to connect disparate files on different computers around the world. It was one of two useful weeks in my "technology 101" in library school because I learned more about technology for ftp (file transfer protocol) & sftp that I would never have learned otherwise. (The other useful week was Unix, which let me play around on IU's SLIS server with sftp & secure document storage. It should not surprise you that these were weeks 14-16).

[^5]: One of the reasons so many technologists hate linked data is becuase of its current nonsensical [graphical representation](http://dublincore.org/documents/dcq-rdf-xml/images/Original_RDF_graph.gif). Thanks to the Dublin Core Metadata Initiative for that photo.

[^6]: Refer to Ruth's document for an understanding of this format's relevance. I learned the RDF conceptual model in RDF/XML and it is not the easiest thing for uninitiated eyes to understand.

[^7]: **Technically** Emily Drabinski is not the creator of that website, but that is because of the misguided idea of what creator means on the web. This is by far my least favorite thing about Dublin Core terms.

[^8]: I've left out the namespaces. In a real document those are required. Refer to Ruth.

[^9]: I created `_:ed` so that I could use it multiple times in this document without creating a permanent resource identifier. Ruth talks about this, I think.

[^10]: Obvious, right? Not to a binary computer.

[^11]: Do not get me wrong: **BIBFRAME is awful.**

[^12]: Cutter, Charles A. Rules for a dictionary catalog, by Charles A. Cutter, fourth edition, rewritten. Washington. UNT Digital Library. http://digital.library.unt.edu/ark:/67531/metadc1048/. Accessed March 22, 2016.

[^13]: I'm not fluent in BIBFRAME and it's not a 1:1 MARC model, but I *think* that is a correct usage of bf:responsibilityStatement. I'm not going back to check.

[^14]: Find, select, identify, obtain if you're a FRBR-er.  

[^15]: Let's be real: OPACs already make these mistakes. That doesn't make these assertions any less critical for library technology based on linked data.
