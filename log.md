10.03.16
DHPrimer tutorial lab

# My Learning Profile & Pathway

## Background

- **Discipline:** History
- **Role:** Undergraduate Student
- **Programming Experience:** No experience

## Research Interests

- Creating timelines
- Collecting web data
- Working with archives
- Network analysis
- Sentiment analysis

## Learning Goals

- Learn programming for academic work
- Scrape and collect web data
- Map networks and historical relationships
- Build a digital archive or collection

## Personalized Learning Pathway

- **Recommended Language:** Python
- **Estimated Total Time:** 9.1 hours
- **Number of Modules:** 10

### Module Sequence

1. **Orientation** — Welcome! A quick introduction to the interface and concepts powering this platform. (~0.1 hours)
2. **Digital Literacy Foundations** — Understanding files, data formats, plain text vs binary, character encoding, and version control concepts. (~1 hours)
3. **Python Basics for Humanists** — Variables, data types, control flow, functions, file I/O, and working with libraries. (~1 hours)
4. **Web Data Collection** — HTML structure, web scraping ethics, BeautifulSoup, APIs and JSON, rate limiting. (~1 hours)
5. **Sentiment and Emotion Analysis** — Computational approaches to detecting emotional valence in text. Using lexicons and ML classifiers to track narrative arcs. (~1 hours)
6. **Understanding Large Language Models** — Explore the architecture and cultural implications of large language models. From vectors and embeddings to self-attention, recurrent networks, and RLHF alignment — and why LLMs are complex systems built on a vast statistical representation of human language. (~1 hours)
7. **Text Analysis Fundamentals** — String operations, regular expressions, word frequency, text cleaning, NLP basics with NLTK. (~1 hours)
8. **Working with Structured Data** — CSV files, Pandas basics, filtering, sorting, grouping, merging datasets, and metadata. (~1 hours)
9. **Data Visualization for DH** — Visualization principles, bar/line/scatter plots, customization, timelines, physicalization, and geographic visualization. (~1 hours)
10. **Network Analysis for Humanists** — Modeling relationships using nodes and edges. Learn to build, visualize, and analyze networks using NetworkX. (~1 hours)
---------
code out of sandbox 

import js
from js import document, URL, Blob

# Part 1: Python - Create content (directly or read from virtual FS)
content = 'First Line of Analysis\nSecond Line of Analysis'
filename = 'analysis_results.txt'

# Part 2: JavaScript Bridge - Trigger browser download
# 1. Create a JavaScript Blob from the string
blob = Blob.new([content], {type: 'text/plain'})

# 2. Create a temporary URL for the Blob
url = URL.createObjectURL(blob)

# 3. Create a hidden <a> element and trigger click
link = document.createElement('a')
link
.href = url
link.download = filename
document.body.appendChild(link)
link.click()

# 4. Cleanup
document.body.removeChild(link)
URL.revokeObjectURL(url) 

---

`something = "blah blah blah"`

`print (something)`

-------

[markdown cheatshet](https://www.markdownguide.org/cheat-sheet/)

A file is a discrete container for data. In Digital Humanities, we often distinguish between:

    -Plain Text (.txt, .csv): Files containing only characters, readable by any computer. These are the "gold standard" for long-term preservation.
    -Structured Data (.json, .xml): Files that use tags or keys to organize data (common in TEI encoding).
    -Binary Files (.docx, .pdf, .jpg): Files that require specific software to interpret their internal structure.
    

Common DH File Extensions

| Extension	Type	| DH Use Case |
|-----------|------------|
| .txt	| Plain Text	| Cleaned corpora for text analysis. |
| .csv	| Comma Separated Values | Datasets for mapping or network analysis. |
| .xml / .tei	| Extensible Markup Language	| Scholarly digital editions.|
| .json	| JavaScript Object Notation	| Data harvested from web APIs or social media.|


File Path: The specific address of a file.

    -Absolute Path: The full address from the "root" (e.g., C:\Users\Humanist\Project\data.txt or /).
    -Relative Path: The address relative to where you are currently "standing."
        -. (dot) represents the current folder.
        -.. (double dot) represents the parent folder (moving up one level).

this started off so strong and suddenly jumped way over my head.

<img width="558" height="69" alt="Screenshot 2026-10-03 at 1 38 59 PM" src="https://github.com/user-attachments/assets/207547df-a2d1-4aca-a668-e2df2666de40" />

how was i supposed to know to use this? its nowhere in any of the instructions. am i missing something? 

<img width="971" height="661" alt="Screenshot 2026-10-03 at 1 48 59 PM" src="https://github.com/user-attachments/assets/b4ba53d7-44a1-469b-9b3a-8fd833f1a75b" /> 

i don't think im cut out for this. 

i dont know how to create a directory. i don't know where to find that out. 
i used the hints. 

i was hoping there would be satisfaction in finally figuring something out. there is not. i just feel like i wish i was Amish and didn't know what a laptop was 

i keep getting confused about what is instructions and what is actually code. i dont know how to make an indent.

<img width="816" height="289" alt="Screenshot 2026-10-03 at 2 22 53 PM" src="https://github.com/user-attachments/assets/40b4a8e1-b375-4620-9af6-e48906f6a17d" />
<img width="738" height="130" alt="Screenshot 2026-10-03 at 2 23 09 PM" src="https://github.com/user-attachments/assets/8f626881-cb9e-46cf-9789-d807b76426ed" />

it has been an hour and a half. i feel like an idiot. i am so overwhelmed by the amount of information.

-----------------------------------------------
10.05.26

# GIS layer examples

- points: artefacts, graves, samples, postholes
- lines: walls, paths, roads, rivers
- polygons: structures, excavation units, sites
- rasters: historical maps, aerial imagery, elevation
- attributes: date, type, depth, condition, interpretation

# GIS workflow

1. organize existing data (vector, imagery, historical maps, etc.)
2. collect site data (points, lines, polygons) and attribute information
3. ensure quality control and accuracy of information
4. conduct spatial analysis
5. interpret spatial patterns in archaeological context
6. communicate results through maps and documentation

# coordinate systems 

- geo coordinate systems enable spatial location of features on Earth using specified two-dimensional numbers
- projection errors: misalignment, shifting, cross-region displacement 

-----------------

# QGIS
 - SHP files need all the accompanying other files to actually work and they all have to have the same name

1. clip: isolate all entities within a given polygon (how many homes are within this 5km radius; a circle?)
2. buffer: visualize given area around specified entity (5km radius around hospital)
3. least-cost path analysis (
