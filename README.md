# AMD vs. Intel on 3DMark's Benchmarking Tools

A research outlining the difference between Intel and AMD CPUs on 3DMark's modern benchmarking tools
(Fire Strike, Time Spy, and Port Royal)

This is currently limited on RTX 3080 data due to scraper constraints but will update once I am able to get more data.

## Summary

Following the RTX 3080's release, the major hardware bottleneck are on the CPUs themselves. This was done well before Zen 3 launch so all the data only extends up to 10th Gen Intel CPUs and Zen 2 AMD CPUs. Under a microscope, it is easy to say that one semiconductor company puts out better consumer-grade CPUs across the board for specific real-world workloads. This research was built upon that presumption to either dispel or reinforce it with 3DMark's modern benchmarking tools as references.

## Rationale

3DMark's data is publicly available. It is currently the most accessible out of the tools available for end-users albeit its imperfections in handling unfinished runs and lack in hardware metrics beyond clock speeds. That said, scalability and generalization is the main goal for the scraper I made solely for 3DMark. It is meant to continuously collect data while also taking into consideration future APIs 3DMark will be adding as part of its currently-supported suite. If the data holds up without bias, the scraper can be easily modified for other benchmarking tools provided the same data can be collected from each result.

## Process

The absence of any 3DMark data collated and formatted for this research prompted the creation of a scraper. I will not be adding in the scraper any time soon on this repository since it still is being continuously refactored.

Due to some faulty results caused by prematurely-ended runs, EDA took out a lot of the results that net a 0 score.

## Changelogs

11.11.20 - New data is set to be added by 11.13.20 but the GPU scope is still limited to Turing GPUs (RTX 30XX) since I have to cap my scraper's speed. Also, a proper readme!

## Stack

Research is in Python on Jupyter Notebook.
Data was collected in Python with BS4.
Class balancing, basic EDA (imputation, dropping nulls), and Mood's median test were done as the main components of this research.
Boxplots were used as main visual reference for identifying outliers.
