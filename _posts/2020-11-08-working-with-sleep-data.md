---
layout: post
title: Working with Sleep Data (On going)
---

Recently, I learned from a friend that sleep medicine technicians are trained to read polysomnography sleep studies in 30-seconds intervals, but that is an arbitrary setup limited to how much information a person can handle reading these graphs. So it seemed to me that the way PSGs are reviewed is based on human limitations. Inspired by that, I reached out to [National Sleep Research Resource (NSRR)](https://sleepdata.org) for some datasets, with the purpose to find out if I can use clustering to identify patterns that have a shorter time span.

### Obtaining Data

To start, I obtained anonymous three polysomnography files from NSRR. Technically, the process involves installation of Ruby, and their official ruby gem. They have very good [documentation here](https://github.com/nsrr/nsrr-gem).

### Reading EDF Data

Polysomnography are sleep recorded in European Data Format (EDF), which is a standard file format designed for exchange and storage of medical time series [wiki](https://en.wikipedia.org/wiki/European_Data_Format). Since it is not the typical CSV file, I need to find a way to read a EDF and translate it into dataframes before I can start working with the data.

I found two R packages "edf" and "edfReader", tried them both and settled with "edfReader", because the later breaks the reading process into Reader and Signals, which I personally find it more friendly to newbies. "edfReader" was developed with codes from "edf" and I did not find anything that it can do and "edf" cannot.

After reading the header, summary() returns:

<p class="message">
File name            : /Users/jc/learn/polysomnography/edfs/learn-nsrr01.edf  
File type            : EDF  
Version              : 0  
Patient              :   
RecordingId          :   
StartTime            : 1985-01-01 21:58:17   
Continuous recording : TRUE  
Recorded period      : 40920 sec = 11:22:00 h:m:s
Ordinary signals     : 14  
Annotation signals   : 0  
Labels               : SaO2, PR, EEG(sec), ECG, EMG, EOG(L), EOG(R), EEG, AIRFLOW, THOR RES, ABDO RES, POSITION, LIGHT, OX STAT  
</p>

And the signal file shows:

<p class="message">
Start time            : 1985-01-01 21:58:17   
Ordinary signals:
 Continuous recording : TRUE  
 Recorded period      : 40920 sec = 11:22:00 h:m:s
 Period read          : whole recording  
 Signals
 R      name     transducer sampleRate preFilter  samples
 signal                           /sec                    
 1      SaO2                         1              40920
 2      PR                           1              40920
 3      EEG(sec)                   125            5115000
 4      ECG                        250           10230000
 5      EMG                        125            5115000
 6      EOG(L)                      50            2046000
 7      EOG(R)                      50            2046000
 8      EEG                        125            5115000
 9      AIRFLOW                     10             409200
 10     THOR RES                    10             409200
 11     ABDO RES                    10             409200
 12     POSITION                     1              40920
 13     LIGHT                        1              40920
 14     OX STAT                      1              40920
</p>
