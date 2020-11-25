---
layout: post
title: Working with Sleep Data (On going)
---

Recently, I learned from a friend that sleep medicine technicians are trained to read polysomnography sleep studies in 30-seconds intervals, but that is an arbitrary setup limited to how much information a person can handle reading these graphs. So it seemed to me that the way PSGs are reviewed is based on human limitations. Inspired by that, I reached out to [National Sleep Research Resource (NSRR)](https://sleepdata.org) for some datasets, with the purpose to find out if I can use clustering to identify patterns that have a shorter time span.

To start, I obtained anonymous three polysomnography files from NSRR. Technically, the process involves installation of Ruby, and their official ruby gem. They have very good [documentation here](https://github.com/nsrr/nsrr-gem).

Polysomnography are sleep recorded in European Data Format (EDF), which is a standard file format designed for exchange and storage of medical time series [wiki](https://en.wikipedia.org/wiki/European_Data_Format). Since it is not the typical CSV file, I need to find a way to read a EDF and translate it into dataframes before I can start working with the data.
