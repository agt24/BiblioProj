# Bibliography Project to explore data-sharing by intramural and extramural NIMH investigators
This project will

1. Download the full-text from journal articles in the human neuroimaging literature (likely from 2008-2013).
2.  Determine whether the research is funded as part of the intramural or extramural funding programs at NIMH.
3.  Determine whether raw data in the article has been shared. 
4.  Present with plots and statistics.

## Downloading the data
There are a number of approaches to identifying and accessing the appropriate literature. The methods included below are only suggestions.

#### Neurotrends
Joshua Carp presented his software written in python at [scipy](http://pyvideo.org/video/1977/neurotrends-large-scale-automated-analysis-of-th). The code, hosted on [github](https://github.com/jmcarp) looks nice with extensive efforts to provide a reproducible tool for performing text-mining on the neuroimaging literature.

#### Neurosynth
Also worth looking into. A different end result but similar methods to get there. Code is hosted on [github](https://github.com/neurosynth/neurosynth).

#### EDirect
Entrez comprises a lot of different databases of which Pubmed is the most relevant to our analysis. If the above tools do not work a more direct interaction with the Pubmed database may be necessary. Entrez can be queried and downloaded from using different approaches. E-utilities are a set of eight server-side programs that provide a stable interface into the Entrez query and database system; however, the best approach for interacting programmatically is [EDirect](http://www.ncbi.nlm.nih.gov/books/NBK179288/?report=reader),  a set of perl scripts that provide E-utility functionality from the Unix command line. There is [documentation](https://www.ncbi.nlm.nih.gov/books/NBK3830/?report=reader) for pubmed itself but the best source of information for our purposes is likely to be the E-utility  [documentation](eutils.ncbi.nlm.nih.gov), which contains a section on using EDirect.

Each entry in Pubmed can be uniquely identified using a PMID. This can be used to link a Pubmed entry with another database in Entrez. One such database that might be useful for our purposes is Pubmed central. PMC contains over 300,000 journal articles that are freely accessible. They can be bulk downloaded or programmatically downloaded using PMIDs. The only way to pull down journal articles found in Pubmed that are not in PMC is by using the Linkout functionality of the Pubmed site. This provides a link to the relevant page on ScienceDirect, Elsevier or the like. I assume parsing the subsequent XML to locate and download the pdf shouldn't be too hard but the whole process is not as easy as the above approaches.

## Determining the funding origin an article

spires indexes bibliographic data for nih supported publications

repars allows analysis of funding information about literature.

If the above tools don't bear fruit PARDI and ireport may or may not be relevant/useful.


## Determining the sharing-status of an article
The data would be hosted online at a repository like Dryad, OpenfMRI, figShare, XNAT Central, NITRC-IR, and NDAR. Articles that shared may have a different frequency of keywords like "shared", "hosted", "online","upload", and "repository". A machine learning algorithm to classify shared and unshared is likely a good way to do this.

## Present the results
We can develop ideas on how to organize the results as the project develops.