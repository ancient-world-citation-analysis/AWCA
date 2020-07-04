# Ancient World Citation Analysis [AWCA](https://github.com/admndrsn/AWCA/blob/master/AWCA_Poster_AAContent_2020.pdf)
![AWCA](https://github.com/admndrsn/AWCA/blob/master/AWCA_Poster_AAContent_2020.png)
Ancient World Computational Analysis is made possible through the Data Science Discovery Program at UC Berkeley.

# Current Team
- 2020: Adam Anderson (PI), Jason Webb, Kenan Jiang, Kewei Chen, Max Ziff, and Shrey Bhate.
- 2019: Adam Anderson (PI), Alan Cha, Jason Webb, Kenan Jiang.
- visiting scholars: Aleksi Sahala, Ilya Akdemir, Isaac Dalke.

## The project description
The goal is to build a citation network from any collection of PDFs. The project is using a collection of texts in the domain of Near Eastern Studies, Classical Philology and Archaeology. The result of this project will make this collection of tools and methods more internationally accessible for research by scholars in many fields, not just my own. My field of study is Near Eastern Languages and Civilizations, with special emphasis in Assyriology and the Bronze Age. We implement tools for 'distant reading' to accompany the close readings taught in these fields.

## Hypothesis
Deep learning tools and methods are capable of generating multi-dimensional language models for quantitative 'distant reading', but how do we make qualitative assessments of the results? Natural Language Understanding / Processing (NLP) is capable of uncovering long-lost truths by counting the context of every word and tagging each named entity, but how do we apply these novel methods to best serve the fields within this study? Just as translation between languages requires a combination of qualitative and quantitative methods, the types of assessments discovered through quantitative analysis can strengthen our ability to make qualitative observations and new associations (see Zellig Harris, 1954, "Distributional Structure").

# Methods and Tools for computational textual analysis
This series of Python Jupyter Notebooks implements different types of NLP tools for computational text analysis, which is demonstrated on a large text corpus of multilingual, primary and secondary sources in the field of Near Eastern Studies. The methods and tools are intended to be generally applicable to any collection of documents (in many languages). Results can be used to visualize the different types of language models in a network, thereby mapping the contours of the research landscape described within a collection of scholarly works. For the purpose of our initial proof of concept, we utilized a corpus of articles and monographs pertaining to the Old Assyrian Period (1950-1750 B.C.), primarily because it falls within [Anderson's domain expertise](https://montallen.academia.edu/AdamAnderson).
 
The purpose of the following notebooks is to leverage existing NLP tools designed for the ‘distant reading’ of an interrelated collection of texts in different languages. Each notebook applies the results of one type of language model to build an edge list for network analysis. These notebooks include implementations for the following tools:

1. Optical Character Recognition (OCR): the Tesseract OCR in a JupyterNotebook. Coding credit goes to Alan Cha (2019) & Kewei Chen (2020).
2. Preprocessing notebooks: Text preprocessing in Jupyter notebooks using the NLTK (natural languages tool kit) to process the PDF OCR output as .TXT and .CSV files. These results will then be used for both citation analysis and bibliographic analysis. Coding credit to Kenan Jiang and Jason Webb.
3. Topic modeling (LDA): the LDA results are assigned as weights for directed edges, with each source as the highest scoring documents within a topic, to each target drawn from the subsequent highest scoring documents within the same topic. The number of topics can be adjusted within the notebook, as can the number of edges drawn for each topic. Coding credit goes to Kenan Jiang. A public visualization of the network can also be seen at [Polinode](https://app.polinode.com/networks/explore/5e454320abfe3e0016cb91c5).
4. Doc2Vec & Word2Vec: The results of the language model produce cosine similarity scores for any two documents in the dataset. The highest similarity scores (>.9) are assigned as weights in an undirected edge list. Coding credit goes to Kenan Jiang and Jason Webb.
5. BERT implementation: The notebook samples from 150 segments for each document. Coding credit to Kenan Jiang.

Because the dataset includes primary and secondary sources still in copyright, the full text files are included only as ‘bags of words’ and ‘bags of segments’ for BERT. Copies of these works were obtained by scanning and OCR, which introduced numerous errors, especially concerning the transliterated cuneiform text. I hope to address these OCR errors downstream with the results of these language models.

* The [Gephi](https://gephi.org/) network files (.gexf) illustrate the results of the project in multi-modal networks of authors-to-authors (i.e. who cites whom?) and authors-to-primary sources (i.e. who cites what?), with links to the titles of the files, not the content (to avoid copyright issues). 
