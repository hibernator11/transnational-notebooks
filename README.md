

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/hibernator11/transnational-notebooks/HEAD)

[![DOI](https://zenodo.org/badge/307151796.svg)](https://zenodo.org/badge/latestdoi/307151796)


# transnational-notebooks
This project includes a collection of Jupyter notebooks to create transnational and multilingual datasets reusing digital collections provided by GLAM institutions.

## Analysing multilingual newspapers: The French Revolution
This [notebook](French-Revolution.ipynb) uses historic newspapers and select digitized newspaper pages provided by [Chronicling America](https://chroniclingamerica.loc.gov/about/) and [Europeana Newspapers](https://pro.europeana.eu/page/iiif) to create a transnational and multilingual dataset based on the French Revolution. 

Chronicling America provides an extensive application programming interface (API) which you can use to explore all of the data. The information is also published as, including the OCR text files. Europeana Newspapers is based on IIIF to search and access information about the digital objects.

The dataset is reused in order to identify named entities in the documents retrieved. We use multilingual named entity recognition based on the pre-trained BERT model to identify locations in the corpora. A random sample is selected from the corpora to identify the locations. Finally, a network graph is created to identify the most commons places named in the text.


## Golden Age: A transnational approach
This [nootebook](Golden-Age-extraction.ipynb) starts by retrieving the authors of the Dutch Golden Age from Wikidata. The authors are enriched with paintings in two relevant repositories, the [Rijksmuseum](https://www.rijksmuseum.nl/en) and the [Harvard Art Museums](https://harvardartmuseums.org/). In this sense, different approaches are implemented in order to merge the datasets such as using the VIAF identifier and the number of the painters.

The data is transformed to RDF using the [RDFLib Python library](https://rdflib.readthedocs.io/en/stable/) by means of the [schema.org](https://schema.org/) vocabulary. Authors and paintings are described and linked using the properties provided by the vocabulary schema. Finally, the RDF dataset is reused by means of SPARQL queries.


## National libraries and authors of 17th century: A Wikidata approach
This [notebook](Wikidata-lod-extraction.ipynb) describes how to query [Wikidata](https://www.wikidata.org) in order to retrieve authors provided by several national libraries. The SPARQL endpoint of Wikidata returns a JSON file as a result that is locally stored. The next step is based on the packaging of the dataset by means of the [Python Package library](https://specs.frictionlessdata.io/data-package). The result is a simple container format for describing a collection of data in a package. Finally, the data is analysed by means of charts in order to identify patterns and insights.


## Additional information
This collection of Jupyter notebooks has been inspired by the [International GLAM Labs Community](https://glamlabs.io/) and the [GLAM Workbench](https://glam-workbench.github.io/). 

