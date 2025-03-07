---
slug: rgbif-seven-years
title: 'rgbif: seven years of GBIF in R'
date: '2018-08-22'
author: Scott Chamberlain
topicid: 1307
tags:
  - biodiversity
  - occurrence
  - rgbif
  - GBIF
  - tech notes
params:
  doi: "10.59350/w1ghx-ah773"
---



[rgbif][] was seven years old yesterday! 



## What is rgbif?

`rgbif` gives you access to data from the Global Biodiversity Information Facility ([GBIF][]) via their API.

A samping of use cases covered in `rgbif`:

* Search for datasets 
* Get metrics on usage of datasets
* Get metadata about organizations providing data to GBIF
* Search taxonomic names
* Get quick taxonomic name suggestions
* Search occurrences by taxonomic name/country/collector/etc.
* Download occurrences by taxonomic name/country/collector/etc.
* Fetch raster maps to quickly visualize large scale biodiversity



## History

Our first commit on `rgbif` was on [2011-08-26][firstcomm], uneventfully adding an empty README:

[![first_commit](/img/blog-images/2018-08-22-rgbif-seven-years/rgbif-first-commit.png)][firstcomm]

We've come a long way since Aug 2011. We've added a lot of new functionality and many new contributors.



### Commit history

Get git commits for `rgbif` using a few packages as well as [git2r](https://github.com/ropensci/git2r), our R package for working with git repositories:


```r
library(git2r)
library(ggplot2)
library(dplyr)

repo <- git2r::repository("~/github/ropensci/rgbif")
res <- commits(repo)
```

A graph of commit history


```r
dates <- vapply(res, function(z) {
    as.character(as.POSIXct(z$author$when$time, origin = "1970-01-01"))
}, character(1))
df <- tbl_df(data.frame(date = dates, stringsAsFactors = FALSE)) %>% 
    group_by(date) %>%
    summarise(count = n()) %>%
    mutate(cumsum = cumsum(count)) %>%
    ungroup()
ggplot(df, aes(x = as.Date(date), y = cumsum)) +
    geom_line(size = 2) +
    theme_grey(base_size = 16) +
    scale_x_date(labels = scales::date_format("%Y/%m")) +
    labs(x = 'August 2011 to August 2018', y = 'Cumulative Git Commits')
```

![commits](/img/blog-images/2018-08-22-rgbif-seven-years/commits.png)

### Contributors

A graph of new contributors through time


```r
date_name <- lapply(res, function(z) {
    data_frame(
        date = as.character(as.POSIXct(z$author$when$time, origin = "1970-01-01")),
        name = z$author$name
    )
})
date_name <- bind_rows(date_name)

firstdates <- date_name %>%
    group_by(name) %>%
    arrange(date) %>%
    filter(rank(date, ties.method = "first") == 1) %>%
    ungroup() %>%
    mutate(count = 1) %>%
    arrange(date) %>%
    mutate(cumsum = cumsum(count))

## plot
ggplot(firstdates, aes(as.Date(date), cumsum)) +
  geom_line(size = 2) +
  theme_grey(base_size = 18) +
  scale_x_date(labels = scales::date_format("%Y/%m")) +
  labs(x = 'August 2011 to August 2018', y = 'Cumulative New Contributors')
```

![contribs](/img/blog-images/2018-08-22-rgbif-seven-years/contribs.png)

`rgbif` contributors, including those that have opened issues (click to go to their GitHub profile):

[adamdsmith](https://github.com/adamdsmith) - [AgustinCamacho](https://github.com/AgustinCamacho) - [AlexPeap](https://github.com/AlexPeap) - [andzandz11](https://github.com/andzandz11) - [AugustT](https://github.com/AugustT) - [benmarwick](https://github.com/benmarwick) - [cathynewman](https://github.com/cathynewman) - [cboettig](https://github.com/cboettig) - [coyotree](https://github.com/coyotree) - [damianooldoni](https://github.com/damianooldoni) - [dandaman](https://github.com/dandaman) - [djokester](https://github.com/djokester) - [dlebauer](https://github.com/dlebauer) - [dmcglinn](https://github.com/dmcglinn) - [dnoesgaard](https://github.com/dnoesgaard) - [DupontCai](https://github.com/DupontCai) - [EDiLD](https://github.com/EDiLD) - [elgabbas](https://github.com/elgabbas) - [emhart](https://github.com/emhart) - [fxi](https://github.com/fxi) - [gkburada](https://github.com/gkburada) - [hadley](https://github.com/hadley) - [ibartomeus](https://github.com/ibartomeus) - [JanLauGe](https://github.com/JanLauGe) - [jarioksa](https://github.com/jarioksa) - [jhpoelen](https://github.com/jhpoelen) - [jkmccarthy](https://github.com/jkmccarthy) - [johnbaums](https://github.com/johnbaums) - [jwhalennds](https://github.com/jwhalennds) - [karthik](https://github.com/karthik) - [kgturner](https://github.com/kgturner) - [Kim1801](https://github.com/Kim1801) - [ljuliusson](https://github.com/ljuliusson) - [luisDVA](https://github.com/luisDVA) - [martinpfannkuchen](https://github.com/martinpfannkuchen) - [MattBlissett](https://github.com/MattBlissett) - [MattOates](https://github.com/MattOates) - [maxhenschell](https://github.com/maxhenschell) - [Pakillo](https://github.com/Pakillo) - [peterdesmet](https://github.com/peterdesmet) - [PhillRob](https://github.com/PhillRob) - [poldham](https://github.com/poldham) - [qgroom](https://github.com/qgroom) - [raymondben](https://github.com/raymondben) - [rossmounce](https://github.com/rossmounce) - [sacrevert](https://github.com/sacrevert) - [sckott](https://github.com/sckott) - [scottsfarley93](https://github.com/scottsfarley93) - [SriramRamesh](https://github.com/SriramRamesh) - steven2249 - [stevenpbachman](https://github.com/stevenpbachman) - [stevensotelo](https://github.com/stevensotelo) - [TomaszSuchan](https://github.com/TomaszSuchan) - Uzma-165 - [vandit15](https://github.com/vandit15) - [vervis](https://github.com/vervis) - [vijaybarve](https://github.com/vijaybarve) - [willgearty](https://github.com/willgearty) - [zixuan75](https://github.com/zixuan75)



## rgbif usage

[Carl Boettiger][carl] and I wrote a preprint paper describing `rgbif` in 2017, in PeerJ Preprints.

> Chamberlain SA, Boettiger C. (2017) R Python, and Ruby clients for GBIF species occurrence data. PeerJ Preprints 5:e3304v1 <https://doi.org/10.7287/peerj.preprints.3304v1>

In that paper we also discuss Python ([pygbif][]) and Ruby ([gbifrb][]) GBIF clients. Check those out if you also sling Python or Ruby.

The paper above and/or the package have been cited **56** times over the past 7 years.

The way `rgbif` is used in research is most often in download occurrence data for a set of study species.

One example comes from the paper 

> Carvajal-Endara, S., Hendry, A. P., Emery, N. C., & Davies, T. J. (2017). Habitat filtering not dispersal limitation shapes oceanic island floras: species assembly of the Galápagos archipelago. Ecology Letters, 20(4), 495–504. <https://doi.org/10.1111/ele.12753>

{{< figure class="center" width="100%" link="https://doi.org/10.1111/ele.12753" src="/img/blog-images/2018-08-22-rgbif-seven-years/rgbif-methods.png" width=550 caption="Carvajal-Endara et al." >}}


In another example (note the mention of removing certain records based on GBIF flags, check out `rgbif::occ_issues` to learn more)

> Werner, G. D. A., Cornwell, W. K., Cornelissen, J. H. C., & Kiers, E. T. (2015). Evolutionary signals of symbiotic persistence in the legume–rhizobia mutualism. Proc Natl Acad Sci USA, 112(33), 10262–10269. <https://doi.org/10.1073/pnas.1424030112>

{{< figure class="center" width=600 link="https://doi.org/10.1073/pnas.1424030112" src="/img/blog-images/2018-08-22-rgbif-seven-years/rgbif-methods2.png" caption="Werner et al." >}}

## Some features coming down the road

* Fully automated pagination across the package. Some functions have automated pagination (`occ_search`/`occ_data`/all `name_` functions). So users don't have to do manual pagination.
* Improved `map_fetch()` function. We just released this function in the last version, but it's still early days and needs to improve a lot based on your feedback
* Improved occurrence downloading queue: we rolled this out recently but just like `map_fetch` it's in its early days and definitely has many rough edges. Please let us know what you think!



## Thanks!

We all owe a large debt of gratitude to [GBIF][] for making an awesome resource for all those using their data, and to all the organizations/people that contribute data to GBIF.

A huge thanks goes to all `rgbif` users and contributors! It's great to see how useful `rgbif` has been through the years, and we look forward to making it even better moving forward.


[rgbif]: https://github.com/ropensci/rgbif
[firstcomm]: https://github.com/ropensci/rgbif/commit/9042246555151240a5136ccf7530d0524bfb1cb5
[carl]: https://www.carlboettiger.info/
[pygbif]: https://pypi.org/project/pygbif
[gbifrb]: https://rubygems.org/gems/gbifrb
[GBIF]: https://www.gbif.org/
