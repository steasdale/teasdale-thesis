# gemenet

This repository contains data, text, and images for my PhD thesis.

The repository is arranged into the following folders.

## chapters

This folder contains the content of my thesis, organized into chapters and sections written in Markdown format. Markdown was deliberately chosen to separate content from presentation, ensuring that the text remains structurally clear, portable, and easily convertible into multiple publication formats. By focusing on semantic rather than visual markup, this approach enhances version control, readability, and long-term preservation of the research content.

## data

This folder contains CSV data files derived from the analyses used in my thesis. The dataset was created through a structured, multi-stage methodology designed to ensure transparency, interoperability, and reproducibility of results and ensure alignment with FAIR (Findable, Accessible, Interoperable, and Reusable) data principles.

1. A corpus of over two thousand notarial contracts related to the economies of slavery was identified and systematically summarized to capture key transactional details.
2. A representative subset of these contracts was digitized as high resolution JPEG files for future textual and quantitative analysis.
3. The digitized materials were organized into a structured digital archive using the [Tropy](https://tropy.org/) archival management software, ensuring consistent metadata and provenance tracking.
4. Bibliographic records for each contract were created in [Zotero](https://www.zotero.org/), enabling citation management and linkage to archival references.
5. Each contract was categorized by legal type—sales, manumissions, leases, etc.—and the principal transactors and enslaved individuals were identified and extracted.
6. Detailed name entity recognition enabled the reconstruction of attributes such as gender, place of residence, age, ancestry, occupation, and social status for most slaveholders and enslaved persons.
7. Additional attributes were extracted, including geographical location, date, sale price, legal conditions, and contextual socioeconomic information.
8. Cleaned and normalized data were encoded into CSV files, with standardized headers and controlled vocabularies for each contract type.
9. The prosopography subfolder includes relational mappings linking individuals across contracts, supporting network and kinship analysis.
10. Finally, the CSV data were imported into an [Omeka-S](https://omeka.org/s/) database and encoded using a custom ontology extending the [CIDOC-CRM](https://cidoc-crm.org/) 7.1.2 framework, facilitating semantic interoperability and long-term reu.

## images

This folder contains the images created for my thesis, primarily consisting of visualizations generated from the structured data contained in the **data** folder. All images are saved in SVG (scalable vector graphics) format, which was chosen for its flexibility, precision, and long-term usability. SVG files preserve full image quality at any resolution, making them ideal for both digital and print dissemination. Their vector-based structure ensures that graphics remain sharp when zoomed or resized, while maintaining significantly smaller file sizes compared to raster formats. This format also allows for direct embedding of metadata**, **text-based editing, and easy version control, ensuring transparency in data visualization design. In addition, SVG files (like the MD files for content) are search-engine optimized (SEO-friendly) and machine-readable, enabling images to be indexed, parsed, and reused in digital repositories and web environments.

## rdf

This folder contains the RDF files for [CIDOC-CRM](https://cidoc-crm.org/) 7.1.2 and [Schema.org](https://schema.org/) 22.0 releases used to model the data in [Omeka-S](https://omeka.org/s/).

## templates

This folder contains templates in JSON format for classes used to model the data in Omeka-S. The classes use elements and properties from CIDOC-CRM and Schema.org ontologies.


The official PDF version of my thesis is available from the University of Toronto at the following link:

https://utoronto.scholaris.ca/items/d03d5ae9-7a01-476f-854c-1db7cad9ac56
