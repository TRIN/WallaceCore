WallaceCore
===========

TRIN Taxon Profile Project: a quest to build a meta-taxon profile using evidence-based methods.

In this repository:
-------------------
 * `data` - data generated by the Taxon Profile Project
 * `data/csv` - in CSV form
 * `data/foswiki` - original raw Foswiki data from http://trin.org.au/TaxonProfile

As of 2003-02-28, this is very much an incomplete work-in-progress.
### TODO
- [x] Share Foswiki raw topic data
- [x] CSV export terms
- [x] CSV export term attributes
- [x] CSV export term relationships
- [ ] CSV export term relationship mapping scheme
- [ ] CSV export namespaces
- [ ] incorporate namespace examples (where copyright/license allows)
- [ ] CSV export example profile data/TPT profiles (if deemed necessary)
- [ ] CSV export term groupings (is this separate to the term export?)
- [ ] Munge up a graph of everything in graphviz/dot
- [ ] Munge up a graph of everything in RDF
- [ ] Convert interesting Taxon Profile technical content over to markdown format to be curated on github.org

*From <http://trin.org.au/TaxonProfile/Definitions/WC>*

A meta taxon profile:
---------------------

Wallace Core (WC) is a set of terms that can be used as metadata to annotate taxon profiles but it is also intended to function as an interchange framework. This wiki topic aims to describe the structure of Wallace Core and the process of applying it to existing Taxon profiles.

### Description of the framework

The framework takes the form of defined terms which are linked to taxon profiles in much the same way as metadata is used to provide extra meaning to a document. The method of linking the framework and the Taxon Profile is to use terms that describe the relationship. These links describe relationships such as equivalent meaning between the framework and the Taxon profile, but it is more common to describe non equivalent relationships. Some examples of equivalent relationships include; SameAs, and ExactMatch. Some examples of non-equivalent relationships include; BroaderThan, NarrowerThan, IsPartOf and HasPart. It could be argued that the differences between these relationships are subtle if any, but it is the purpose for which these relationships were created that provide their usefulness. BroarderThan and NarrowerThan have their origins in thesaurus construction. IsPartOf and HasPart were derived from records and document management. The reasons for each relationship selection will be explained in the more detail later, but first an overview of how this framework might effect taxonomic work.

### The Term Definitions

The terms are described with a set of attribute pairs which were derived from Dublin Core Terms (DCTerms), Resource Description Framework (RDF) and the Simple Knowledge Organization System (SKOS) projects. A term attribute pair might look like this: rdfs:Label = "Scientific name"

*From <http://trin.org.au/TaxonProfile/>*

A Rosetta stone
===============
We are building a meta-taxon profile and the means to use it to describe individual/given taxon profiles; and hence derive a general model of taxon/species profiles. We believe the means to encode meaning are essential for the use of information in novel contexts. And that this is important.

Our goal is to provide

* an exchange standard for information about taxa
> (as opposed to just for nomenclatural or identification information) 
* a means to translate and link information about taxa across disciplines
* encode similar/common meaning to elements - where possible 

This meta-profile-framework will incorporate sufficient formality that taxon related information from a variety of sources can be

* presented in a formal-resolvable-interchange-linked-data standard
* and read non-geeks in plain language
