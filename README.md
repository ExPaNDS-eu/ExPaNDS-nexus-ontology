# ExPaNDS-nexus-ontology


The purposes of the NeXus Ontology can be summarized as:

- To provide a single controlled vocabulary of NeXus terms (base class and field names) by flattening and joining the separate namespaces of base classes in a consistent and reversible manner.
- To provide global persistent identifiers for each NeXus term.
- To describe the key NeXus concepts and relationships in a single ontology, linking to existing NeXus annotation and documentation, effectively providing a NeXus explorer tool.
- To reflect and formalize the intended semantic of NeXus but add no additional interpretation.
- To allow the ontology to be updated automatically following publication of new classes after approval of the NIAC
- To utilize a framework (i.e. OWL) that allows separate additional ontologies to provide mappings and relationships to terms in other vocabularies and ontologies.

Citation: [10.5281/zenodo.4806026](https://doi.org/10.5281/zenodo.4806026)

### Implementation

The OWL ontology is created automatically by a Python script that parses the NXDL files and converts it into an OWL file, with essentially no user input. 


There are two steps to this process:
- the GitHub API is used to obtain a listing of the urls of the NeXus NXDL files, which are then parsed using the Python minidom module, creating dictionaries of NeXus definitions. 
- the Python dictionaries are used to create the ontology OWL file using the owlready2 module.

The Python script is in Jupyter Notebook


### Maintenance

It is expected that this ontology will be maintained by the Nexus International Advisory Committee (NIAC). The expected location of the repository will be: [NexusOntology](https://github.com/nexusformat/NeXusOntology). 
