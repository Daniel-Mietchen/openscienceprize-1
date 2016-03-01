### Science Fair

![Science Fair logo](https://github.com/codeforscience/openscienceprize/raw/master/logo.png)

##### Code For Science / Submission / Open Science Prize 2016
-----

What if you wanted to make a backup copy of all known digitally published scientific literature? What if you wanted to search and read the literature on Svalbard, the Voyager spacecraft or in a remote village? Today it is impossible, as such a dataset has not been aggregated and the software to synchronise and explore it does not exist. Science Fair will change that. Along the way we will ensure that the scientific literature is massively replicated around the world into copies of the Science Fair application running on users machines. You can, in principle, store the whole of scientific literature metadata and open access papers on a large USB stick -- we just need to write the software to make it possible.

Although vast troves of knowledge are contained in the output of scientific research, most of it now is difficult or time-consuming to search or access, and relies on several centralized points of failure, such as journals or government servers. Researchers, students and members of the public who wish to search or analyse the literature are limited by proprietary interfaces and fragmented silos. Our existing infrastructure is focused on large organisations. It should be focused on people.

We propose to develop Science Fair: an open-source desktop application for searching and sharing scientific content. The application will build a decentralised peer-to-peer network of high-quality, open aggregated scholarly metadata, and provide quick and easy search across metadata and full-texts of open access sources, downloading results en masse to the user’s computer for reading, interacting with, and data-mining. 

The initial goal of the project is twofold: to produce high quality article and full-text metadata datasets for scientific literature and release them as open data, and to build an open source application to synchronise, search and selectively download these datasets in a distributed network. Science Fair users will be able to perform exploratory keyword searches (such as “CRISPR”) or more focused searches (such as by author or DOI, or only within figure captions or methods sections) and quickly view and download full-text copies of selected articles. Science Fair keeps an offline copy of the articles, and metadata, meaning users can still use the application without an Internet connection to search and access articles they have already downloaded. When an Internet connection is available, Science Fair will automatically share the underlying data with the peer-to-peer network.

Science Fair doesn’t communicate directly with the huge number of publisher and repository websites. Instead, it uses an aggregated metadata database seeded from those sources that contains BibJSON [1] standardized journal metadata for papers in various open access journals, and an aggregated full-text database that contains semantically marked-up Scholarly HTML [2]. We have created an initial demonstration distributed article metadata database of over 3.5 million articles from Europe PubMed Central [3]. We will extend this by integrating metadata from many other sources such as CrossRef [4] and arXiv [5] and resolving redundancy and conflicts between the datasets.

We use peer-to-peer direct connections to distribute article metadata and open access files between Science Fair users. This means that every user of Science Fair contributes to the network, sharing content directly to other users as well as acting as redundant data sources in case the journal websites go offline [6] or move/lose the data [7]. 

The goals above are accomplished by building on top of established open source projects: ContentMine [8], Dat [9] and Electron [10]. ContentMine is a suite of tools for harvesting and analysing the literature, developed by a Shuttleworth Foundation funded team including Richard Smith-Unna, the UK project lead on Science Fair. Dat is an open source peer to peer dataset versioning and sync tool designed with scientific reproducibility and archiving in mind. It is developed by a not-for-profit team based in the U.S. and funded by the Alfred P. Sloan and John S. and James L. Knight Foundations. The Dat project lead, Maxwell Ogden, is the U.S. project lead on Science Fair.

Electron is an open source desktop application framework that provides a way to use Google’s Chromium browser engine to build cross platform native-feeling applications using web technologies: HTML, CSS and JavaScript. Using Electron means we can, as a small team, provide a compelling user experience across multiple platforms with a single application codebase that runs on all major operating systems. Five years ago we would have needed three separate teams to support OS X, Windows and Linux, but now we only need one.

We will distribute Science Fair through app distribution channels such as the Mac App Store as well as providing downloadable application binaries for OS X, Windows and Linux from our project website. 100% of the code will be open source and available on GitHub.

By building our application on top of the peer-to-peer data sharing tool Dat we will ensure that both metadata and articles are available with low bandwidth costs, and increased redundancy and archival integrity. Peer-to-peer access to papers also enhances reproducibility, as it ensures access to research regardless of the availability of the original data source.

In order to create a search experience that meets the needs of scientific users we will have to create high quality article metadata databases. Members of our team have experience with data mining and aggregation and will produce two major standardized, deduplicated datasets: one with the metadata for all articles from all journals, and another with full-texts, figures and citations of open access articles from all journals. These on their own will be a valuable contribution to the Open Science community, and as the quality of these improve so will the value of the Science Fair application and any other applications that use our data.

When new articles are published by the journals we can automatically start distributing copies of the metadata and full-texts (for open access content) through our peer to peer network. This means there will be no additional bandwidth usage for the journals (we will likely end up saving them bandwidth overall) while at the same time making download speeds faster for users of Science Fair due to the peer-to-peer swarm mechanics.

Science Fair will also be ideally positioned to support the new highly interactive outputs of modern research, which include not only papers but also data, annotations, media, code, and computational environments. Dat supports peer-to-peer sharing of large, versioned data files, and containerized reproducible software [9] -- in contrast to governments or journals providing centralized data hosting and who have an incentive to limit file sizes due to the cost of bandwidth for large data transfers, something we don’t have to worry about thanks to the underlying peer-to-peer technology.

Unlike existing approaches to literature search and download, such as Google Scholar [11] or Papers [12], our software will be free, open and embrace Open Web technologies and peer-to-peer data sharing as our building blocks -- namely Electron and Dat. These technologies will facilitate sharing large amounts of heterogeneous data, and let us create new interfaces to modern research outputs, such as interactive data visualizations, crowdsourced annotations (e.g. via Hypothes.is [13]) or other rich media that go far beyond viewing a PDF.

We believe that the Open Science movement needs to invest in a decentralised open infrastructure for academic publishing. Our project will serve not only as a better user experience for science consumers, but as a proof of principle that such a system is ideally suited for decentralisation, built on open web technologies, available as open source software and based on high quality open data sets.

##### *Additional details*

An early functional prototype of Science Fair is available at [github.com/codeforscience/sciencefair](https://github.com/codeforscience/sciencefair)

We will develop Science Fair according to the following short term and long term goals. Many of these goals are already underway, and we have a strong record of building and contributing to open source and open science projects, and working on projects with distributed teams.

Short term goals

- Build databases for several metadata sources
- Build open access full-text collections
- Set up Dat servers to provide initial high speed data sources
- Expand search capabilities, including metadata, keyword, image, and full text
- Automatically extract thumbnails and figures to display alongside papers in the app
- Refine and user test the UI/UX

Long term goals

- Support archiving and searching raw data, code, and containers alongside papers
- Design interfaces within the app for interactive media, especially visualization
- Enhance search and recommendation using data mining and machine learning
- Enable crowd-sourced metadata corrections and annotations within the app

Project Team

- Richard Smith-Unna  [@blahah](https://github.com/blahah)
- Maxwell Ogden  [@maxogden](https://github.com/maxogden)
- Jeremy Freeman  [@freeman-lab](https://github.com/freeman-lab)
- Karissa McKelvey  [@karissa](https://github.com/karissa)

All software will be released under BSD/MIT/ISC or similar permissive license, and creative works under CC0 Public Domain Dedication.

[1]: http://okfnlabs.org/bibjson/
[2]: https://europepmc.org/
[3]: http://www.crossref.org/
[4]: http://scholarly.vernacular.io/
[5]: http://arxiv.org/
[6]: http://www.pewresearch.org/fact-tank/2013/10/02/federal-government-shutdown-the-data-casualties/
[7]: https://medium.com/@bmpvieira/when-bioinformatics-apis-break-821ae9919492#.ij7q71kam
[8]: http://contentmine.org
[9]: http://dat-data.com/
[10]: http://electron.atom.io/
[11]: http://hyperos.io/
[12]: https://scholar.google.com/
[13]: http://www.papersapp.com/
[14]: https://hypothes.is/
