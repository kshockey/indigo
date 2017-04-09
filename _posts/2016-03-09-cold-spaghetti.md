---
layout: post
title: "Cold Spaghetti, Cold Spaghetti"
date:   2016-03-09
categories:
tags: cataloging, MARC, FRBR, documentation, scholarship, social justice, metadata
---

>The bells explain what they've been lacking all along
>They were disorganized and that was what was wrong
>
>-They Might Be Giants, ["The Bells Are Ringing"](https://www.youtube.com/watch?v=cSEQ0kMt-0k)

The link between RDA and FRBR has always been a bit fuzzy for me. Reading the following passage in Karen Coyle's book made something click for me in an alarming way.

>What is notable about FRBR, and in some respects RDA also, is that it makes numerous assumptions that were never tested. Because FRBR was couched in terms of a known technology [entity-relation model], it was assumed to be technically valid and perhaps even implementable, in spite of the declarations of technology neutrality. Yet no implementations of FRBR, even on a small set of test data, were developed as part of the FRBR Study Group's process. RDA is therefore a cataloging standard based on an unproven conceptual model. The technology that would support them, is at the time of this writing [2015?], still unavailable.
>
>-Karen Coyle, [(<i>FRBR before and after: a look at our bibliographic models</i>](http://www.kcoyle.net/beforeAndAfter/index.html), p. 68.

We screwed up, often and badly. We're not fixing it, really. And no, I am not talking about the retention and continued of MARC as librarianship's primary metadata standard, which Coyle regards as "[q]uite possibly the greatest mistake in the last two to three decades" (p. 51).

Interoperability has always been some form of making the peg fit the whole by manipulating the shape of the peg and the shape of the hole to varying degrees based on a project's context. This metaphor is so applicable to just about everything that it is essentially how we conceive of concept modeling and the alteration of worldviews in cognitive science. In light of [Andreas Orphanides](http://2016.code4lib.org/Architecture-is-politics-the-power-and-the-perils-of-systems-design)'s assertion that metadata is a social justice issue, we have failed our users so much[^1]. We have bludgeoned the hole with a badly-shaped peg using countless dollars, labor hours, papers, conferences, hours of coding, years [decades?] of time while yelling, "LOOK, LIBRARY DATA MATTERS AND IS TOTALLY RELEVANT!" That's why interoperability guiding the databases that underlie most, if not all, of the library's activities is passed on through this frustrating cabal-like induction-through multi-trial ceremony that is cataloging and metadata classes and/or ad-hoc "put this literal string here" on-the-fly training[^2].

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Teaching RDA in MARC to noobs is hard! Like it doesn&#39;t make sense. It jumps all over! Record all this info on M, except a little of W&amp;E too!</p>&mdash; Amber Billey (@justbilley) <a href="https://twitter.com/justbilley/status/707001167788777476">March 8, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

The FRBR-RDA-MARC relationship reminds me of a model used to describe the affordances and hinderances of trying to create legal, free cultural objects on the web in our current copyright regime[^3]. [Lawrence Lessig](http://www.lessig.org/about/) developed an idea through his early books, now enshrined in the structure of the [Creative Commons License](https://creativecommons.org/licenses/), about the interacive, intertwined levels involved in ensuring the spectrum of "copyrights" (or degrees of copyrightness, based on the license) is represented across the various technologies (i.e. contexts) of their domain. When trying to describe what the alphabet soup that facilitates surrogate modeling (read: cataloging), we fail to distinguish the participation of each acronym in the constellated network of bibliographic control, from the philosophical concept to the display constant in a catalog[^4] I will write about this at length in the upcoming blog post mentioned in note three, but the MARC record as it stands is an ad-hoc amalgamation of purpose and the library catalog as it stands fails at most things because it tries to do everything[^5]. With that in mind, let's clear up what these things are and do:

>1. FRBR is a <b>conceptual model</b>.
>2. RDA is a <b>data standard/code/rule set</b>[^6].
>3. MARC is... <b>a lot of things</b>.

MARC, like the library catalog, is so abstracted both conceptually and physically from what it was designed to do in its original context that it really isn't easy to pin down. In the constellated network I am trying to illuminate for you, MARC is a coding language. The MARC record, a byproduct of the original purpose of machine readable cataloging, is a structural format (a container?) for the data considered valid and relevant in the bibliographic universe according to the specifications in RDA. Because of the semantic meanings implied by the coded data fields of MARC, it's also...a data standard. This is a large part of why bludgeoning MARC with the RDA toolkit is so difficult![^7] If you don't use it regularly, I urge you to try the MARC to RDA mappings and the RDA to MARC mappings in the toolkit some time. Undoubtedly one of the hardest tools to use in that toolkit (aside from perhaps the rulebook itself). Where does FRBR come in? It's a conceptual model that is supposed to underpin RDA, which specifies rules for data construction and inclusion, which can then be thrown at MARC like cold spaghetti.

At another time I can illuminate the interrelationships between the things above. What you need to know for this argument is that the conceptual model of FRBR has an intellectual history that is heavily influenced by (you guessed it) MARC (Clarke 2015). In our own little and not so little ways, MARC still pervades all our services. People don't Boolean search any more (unless you're me). People do not understand the vocabularies required to properly execute a subject search in our catalogs, which is the primary collocation method through which people engage in an unknown item search (and people want to do unknown item searches way more than we think). Even when we have new, rich, expansive possibilities for what to do with our data, we are so busy manipulating the shiny new holes to fit our heavy, misshapen peg--which continues to have absurd amounts of resources thrown at it while its affordances and extremly numerous limitations are known many times over--that we forget to (or do not have the ability or desire to) demonstrate to the money why MARC is such an unimaginable burden and waste.

[Are we having fun yet?](https://www.youtube.com/watch?v=VflIdXP46RU)

[^1]: In a piece in press, I argue that American librarianship is focused on intellectual freedom and neutrality to the exclusion of social justice. This plays into design decisions regarding the rules, tools, systems, standards, and governance of institutions tasked with developing and maintaining library catalogs.

[^2]: OR: outsourced to corporate vendors who don't give a shit about your users because they just want to sell books...using labor extracted from the people who fit the previous two descriptions.

[^3]: Another blog post is forthcoming about how people who think about metadata in and around libraries use technical and conceptual language very poorly, which results in us not understanding 1) what a thing is, 2) what a thing is supposed to be doing, 3) what the thing is actually doing. It contains a lot more Coyle and some other reading that has struck me as of late.

[^4]: I chose to say display constant instead of stopping at the literal string that a cataloger inputs into the MARC workform because the MARC codes have specific semantic meanings that tell the user things, particularly with regard to subject access and entity relationships.

[^5]: Not to overindulge the "make it more like G--gle" problem, but people do not think the G is everything because everything happens on its dot com search engine--that is one specific thing better than any else of its kind. They think it's everything because it's a multi-national, multi-billion dollar hypercapitalist blight that has its hands in most tech pies through <u>other</u> technologies.

[^6]: Calling this a data standard [implied: model] is a misnomer. It does not specify structural format [in this case the MARC record] of the data like a data standard typically does. RDA itself switches between the terms "code" and "standard" (which are not even close to the same thing).

[^7]: I will never utter the following words again, so listen up: Michael Gorman was...right...about RDA being a debacle, but not for the reasons he specified. The Anglo-American Cataloging Rules were very clear about what they were and what they did. It's right there in the name: Rules.

stuff i used

Billey, A. [@justbilley] Teaching RDA in MARC to noobs is hard! Like it doesn't make sense. It jumps all over! Record all this info on M, except a little of W & E too! [Tweet]. Retrieved from https://twitter.com/justbilley/status/707001167788777476.

Clarke, R.I. (2015). "Breaking records: the history of bibliographic records and their influence in conceptualizing bibliographic data." <i>Cataloging & Classification Quarterly 53</i>: 3-4, 286-302.

Coyle, K. (2016). <i>FRBR before and after: a look at our bibliographic models.</i> Chicago: ALA Editions.

Orphanides, A. (2016, March 9). Architecture is politics: the powers and perils of systems design. Presented at code4lib 2016, Philadelphia, PA, USA.
