---
title: rOpenSci News Digest, July 2022
author:
  - The rOpenSci Team
date: '2022-07-22'
slug: ropensci-news-digest-july-2022
categories: []
tags:
  - newsletter
description: Code of Conduct Update, new packages and package news
params:
  last_newsletter: '2022-06-24'
  doi: "10.59350/hge37-v9p96"
---


<!-- Before sending DELETE THE INDEX_CACHE and re-knit! -->

Dear rOpenSci friends, it's time for our monthly news roundup!
<!-- blabla -->
You can read this post [on our blog](/blog/2022/07/22/ropensci-news-digest-july-2022).
Now let's dive into the activity at and around rOpenSci!

## rOpenSci HQ

### rOpenSci Code of Conduct update

We are pleased to announce the release of a new version of our Code of Conduct.  
Based on the feedback of our community we added greater detail about acceptable and unacceptable behaviors in online settings and we have the first translation of the text to Spanish.

#### Committee changes

We thank [Megan Carter](https://www.esipfed.org/about/people/megan-carter) for serving as independent community member until June, 2022 and welcome back [Kara Woo](https://karawoo.com/) to serve on this role.
[Yanina Bellini Saibene](/author/yanina-bellini-saibene/) joins the committee as the new rOpenSci Community Manager.

You can read all the details in our [blog post](/blog/2022/07/12/coc-update/).


## Software :package:

### New packages




The following three packages recently became a part of our software suite:

+ [datefixR](https://docs.ropensci.org/datefixR), developed by Nathan Constantine-Cooke: There are many different formats dates are commonly represented with: the order of day, month, or year can differ, different separators ("-", "/", or whitespace) can be used, months can be numerical, names, or abbreviations and year given as two digits or four. datefixR takes dates in all these different formats and converts them to Rs built-in date class. If datefixR cannot standardize a date, such as because it is too malformed, then the user is told which date cannot be standardized and the corresponding ID for the row. datefixR' also allows the imputation of missing days and months with user-controlled behavior.  It is available on [CRAN]( https://CRAN.R-project.org/package=datefixR). It has been [reviewed](https://github.com/ropensci/software-review/issues/533) by Kaique dos S. Alves, and Al-Ahmadgaid B. Asaad.

+ [epair](https://docs.ropensci.org/epair), developed by G.L. Orozco-Mulfinger together with Madyline Lawrence, and Owais Gilani: Aid the user in making queries to the EPA API site found at https://aqs.epa.gov/aqsweb/documents/data_api. This package combines API calling methods from various web scraping packages with specific strings to retrieve data from the EPA API. It also contains easy to use loaded variables that help a user navigate services offered by the API and aid the user in determining the appropriate way to make a an API call. 

+ [readODS](https://docs.ropensci.org/readODS), developed by Chung-hong Chan together with Gerrit-Jan Schutten, and Thomas J. Leeper: Read ODS (OpenDocument Spreadsheet) into R as data frame. Also support writing data frame into ODS file.  It is available on [CRAN]( https://CRAN.R-project.org/package=readODS). It has been [reviewed](https://github.com/ropensci/software-review/issues/386) by Emma Mendelsohn, and Adam H. Sparks.

Discover [more packages](/packages), read more about [Software Peer Review](/software-review).

### New versions



The following eight packages have had an update since the last newsletter: [datefixR](https://docs.ropensci.org/datefixR "Standardize Dates in Different Formats or with Missing Data") ([`v1.0.0`](https://github.com/ropensci/datefixR/releases/tag/v1.0.0)), [dittodb](https://docs.ropensci.org/dittodb "A Test Environment for Database Requests") ([`v0.1.4`](https://github.com/ropensci/dittodb/releases/tag/v0.1.4)), [EDIutils](https://docs.ropensci.org/EDIutils "An API Client for the Environmental Data Initiative Repository") ([`v1.0.1`](https://github.com/ropensci/EDIutils/releases/tag/v1.0.1)), [jagstargets](https://docs.ropensci.org/jagstargets "Targets for JAGS Workflows") ([`1.0.3`](https://github.com/ropensci/jagstargets/releases/tag/1.0.3)), [lingtypology](https://docs.ropensci.org/lingtypology "Linguistic Typology and Mapping") ([`v1.1.9`](https://github.com/ropensci/lingtypology/releases/tag/v1.1.9)), [restez](https://docs.ropensci.org/restez "Create and Query a Local Copy of GenBank in R") ([`v2.0.0`](https://github.com/ropensci/restez/releases/tag/v2.0.0)), [rtweet](https://docs.ropensci.org/rtweet "Collecting Twitter Data") ([`v1.0.2`](https://github.com/ropensci/rtweet/releases/tag/v1.0.2)), and [tidyqpcr](https://docs.ropensci.org/tidyqpcr "Quantitative PCR Analysis with the Tidyverse") ([`v1.0.0`](https://github.com/ropensci/tidyqpcr/releases/tag/v1.0.0)).

## Software Peer Review

There are fifteen recently closed and active submissions and 2 submissions on hold. Issues are at different stages: 

* Two at ['6/approved'](https://github.com/ropensci/software-review/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A6/approved):

     * [datefixR](https://github.com/ropensci/software-review/issues/533), Fix Really Messy Dates. Submitted by [Nathan Constantine-Cooke](http://constantine-cooke.com). 

    * [epair](https://github.com/ropensci/software-review/issues/418), Grabs data from EPA API, simplifies getting pollutant data. Submitted by [Leo Orozco-Mulfinger](https://github.com/GLOrozcoM). 

* One at ['5/awaiting-reviewer(s)-response'](https://github.com/ropensci/software-review/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A5/awaiting-reviewer(s)-response):

     * [phruta](https://github.com/ropensci/software-review/issues/458), Phylogenetic Reconstruction and Time-dating. Submitted by [Cristian Román Palacios](http://cromanpa94.github.io/cromanpa/). 

* Three at ['4/review(s)-in-awaiting-changes'](https://github.com/ropensci/software-review/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A4/review(s)-in-awaiting-changes):

     * [hudr](https://github.com/ropensci/software-review/issues/524), A R interface for accessing HUD (US Department of Housing and Urban Development) APIs. Submitted by [Emmet Tam](https://github.com/etam4260/etam4260). 

    * [octolog](https://github.com/ropensci/software-review/issues/502), Better Github Action Logging. Submitted by [Jacob Wujciak-Jens](https://github.com/assignUser). 

    * [healthdatacsv](https://github.com/ropensci/software-review/issues/358), Access data in the healthdata.gov catalog. Submitted by [iecastro](http://iecastro.netlify.com). 

* Four at ['3/reviewer(s)-assigned'](https://github.com/ropensci/software-review/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A3/reviewer(s)-assigned):

     * [spiro](https://github.com/ropensci/software-review/issues/541), Manage Data from Cardiopulmonary Exercise Testing. Submitted by [Simon Nolte](https://github.com/smnnlt). 

    * [canaper](https://github.com/ropensci/software-review/issues/475), Categorical Analysis of Neo- And Paleo-Endemism. Submitted by [Joel Nitta](https://joelnitta.com).  (Stats).

    * [tsbox](https://github.com/ropensci/software-review/issues/464), Class-Agnostic Time Series. Submitted by [Christoph Sax](http://www.cynkra.com).  (Stats).

    * [ROriginStamp](https://github.com/ropensci/software-review/issues/433), Interface to OriginStamp API to Obtain Trusted Time Stamps. Submitted by [Rainer M Krug](https://github.com/rkrug). 

* Two at ['2/seeking-reviewer(s)'](https://github.com/ropensci/software-review/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A2/seeking-reviewer(s)):

     * [aorsf](https://github.com/ropensci/software-review/issues/532), Accelerated Oblique Random Survival Forests. Submitted by [Byron](https://github.com/bcjaeger). 

    * [bssm](https://github.com/ropensci/software-review/issues/489), Bayesian Inference of Non-Linear and Non-Gaussian State Space. Submitted by [Jouni Helske](http://jounihelske.netlify.app).  (Stats).

* Three at ['1/editor-checks'](https://github.com/ropensci/software-review/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A1/editor-checks):

     * [daiquiri](https://github.com/ropensci/software-review/issues/535), Data Quality Reporting for Temporal Datasets. Submitted by [Phuong Quan](https://github.com/phuongquan). 

    * [wmm](https://github.com/ropensci/software-review/issues/522), World Magnetic Model. Submitted by [Will Frierson](https://github.com/wfrierson). 

    * [rdbhapi](https://github.com/ropensci/software-review/issues/443), Interface to DBH-API. Submitted by [Marija Ninic](https://hkdir.no/). 

Find out more about [Software Peer Review](/software-review) and how to get involved.

## On the blog

<!-- Do not forget to rebase your branch! -->



* [rOpenSci Code of Conduct Update](/blog/2022/07/12/coc-update) by Yanina Bellini Saibene, Mark Padgham, and Kara Woo. Update on Code of Conduct 2022.



### Tech Notes

* [Evaluating GitHub Activity for Contributors](/blog/2022/07/01/evaluating-github-activity-for-contributors) by Maëlle Salmon. How to evaluate the activity of a GitHub repository as an user or potential contributor. This post was discussed on the [R Weekly Highlights podcast](https://share.fireside.fm/episode/87RSVeFz+17WMAquN?t=1491).

* [Upgrading rtweet](/blog/2022/07/21/rtweet-1-0-0) by Lluís Revilla Sancho. Update from rtweet 0.7.0 to 1.0.2.

<!--
## Use cases



`snakecase::to_sentence_case(english(length(usecases)))` use case`if (length(usecases) > 1) "s"` of our packages and resources ha`if (length(usecases) > 1) "ve" else "s"` been reported since we sent the last newsletter.



Explore [other use cases](/usecases) and [report your own](https://discuss.ropensci.org/c/usecases/10)!
-->
## Call for maintainers

We're looking for a new maintainer, or a new maintainer _team_, for each of the following packages:

* [nbaR](https://docs.ropensci.org/nbaR/), R client library for the Netherlands Biodiversity Api (NBA). [Issue for volunteering](https://github.com/ropensci/nbaR/issues/64).

* [elastic](https://docs.ropensci.org/elastic/), R client for the Elasticsearch HTTP API. [Issue for volunteering](https://github.com/ropensci/elastic/issues/292).

If you're interested, please comment in the issues or email `info@ropensci.org`.

For more info, see

* [our guidance on _Changing package maintainers_](https://devguide.ropensci.org/changing-maintainers.html);
* [our _Package Curation Policy_](https://devguide.ropensci.org/curationpolicy.html).

## Package development corner

Some useful tips for R package developers. :eyes:

### pak::pak()

Say you cloned a repository and are now getting ready to debug it.
How do you make sure you have all its development dependencies installed?
[Simply](https://twitter.com/GaborCsardi/status/1545306904028741632) run [`pak::pak()`](https://pak.r-lib.org/reference/pak.html)! 
Easy to remember and to type, and it works!

### Update to CRAN NEWS.md parsing

If you maintain a [changelog for your package](https://blog.r-hub.io/2020/05/08/pkg-news/), as [you should](https://devguide.ropensci.org/releasing.html?q=news#news), and have chosen the Markdown format (`NEWS.md`) to do so, you might need to pay attention to its formatting for optimal parsing by

* pkgdown, see the docs for [`pkgdown::build_news()`](https://pkgdown.r-lib.org/reference/build_news.html), for instance pay attention to [headings](/blog/2022/01/31/package-build-failures/#wrong-newsmd-structure);

* [R itself](https://stat.ethz.ch/pipermail/r-package-devel/2022q3/008239.html) -- if all goes well a `NEWS.md` file that is correct for pkgdown will be correct for R too. You can follow the [debugging steps recommended by Henrik Bengtsson](https://stat.ethz.ch/pipermail/r-package-devel/2022q3/008238.html) to find what's wrong in your `NEWS.md` file.

### How to handle CRAN checks with `_R_CHECK_DEPENDS_ONLY_`=true

In some cases CRAN might run [checks without installing the Suggested dependencies](https://stat.ethz.ch/pipermail/r-package-devel/2022q2/008193.html).
How to ensure your vignettes still "work", that is to say, that R CMD check will not produce any error or warning?
- [pre-build](/blog/2019/12/08/precompute-vignettes/) your vignettes;
- make them pkgdown [articles](https://usethis.r-lib.org/reference/use_vignette.html) instead (no vignette, no vignette error!);
- execute code conditionally based on the availability of packages, with knitr `eval` chunk option for instance.

## Last words

Thanks for reading! If you want to get involved with rOpenSci, check out our [Contributing Guide](https://contributing.ropensci.org) that can help direct you to the right place, whether you want to make code contributions, non-code contributions, or contribute in other ways like sharing use cases.

If you haven't subscribed to our newsletter yet, you can [do so via a form](/news/). Until it's time for our next newsletter, you can keep in touch with us via our [website](/) and [Twitter account](https://twitter.com/ropensci).
