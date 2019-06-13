# AWCA
AWCA stands for Ancient World Citation Analysis, and is an undergraduate research apprenticeship program through the Data Science Education Program at UC Berkeley.
## The project description
The goal is to build a citation network from any collection of PDFs. The project is using a collection which I've scanned in the domain of ancient Near Eastern Studies, Classics, Archaeology, and Middle Eastern Languages (located on my Google Drive). The result of this project will make this collection more internationally accessible for research by scholars in these fields.
* The first Jupyer notebook will run the Tesseract OCR in a JupyterNotebook. To do this the PDF must be converted to .TIF images. 
* The next Jupyter notebook will use the CLTK (classical languages toolkit) to pre-process the OCR output. These results will then be used for both citation analysis and bibliographic analysis. We will also introduce tools/methods for computational textual analysis (e.g. Gensim).
* The network files (.gexf) illustrate the results of the project in multi-modal networks of authors-to-authors (i.e. who cites whom?) and authors-to-primary sources (i.e. who cites what?), with links to the OCRed text in 'bags of words' (to avoid copyright issues). 
