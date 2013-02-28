This is raw data exported out of the TRIN Wiki at <http://trin.org.au/TaxonProfile/>

This comes from Foswiki structured data which may require some minor transformation to be acceptable for further work.

Some of the fields are Foswiki metadata which have their own conventions and semantics, refer to <http://foswiki.org/System/QuerySearch>.

Summary:
-------
* `web` is a Foswiki term for a namespace or container path, like a directory in a filesystem.
* `topic` is a Foswiki term for what might be known as a page in other platforms, but there are some interesting differences documented at <http://foswiki.org/System/TopicsAndWebs>
* `parent.name` aka `META:TOPICPARENT.name`: topic parent which allows for hierarchical grouping and classification of topics
* `info.author` aka `META:TOPICINFO.author`: username which last modified the topic. A username of JohnDoe can be resolved at <http://trin.org.au/Main/JohnDoe>. Usernames of the form `BaseUserMappinag_nnn` are guest, superuser or machine (non-human) accounts.
* `info.date` aka `META:TOPICINFO.date`: last-modified date, in unix epoch seconds
* `info.version` aka `META:TOPICINFO.version` the current revision number of the topic.
* `preferences[name='PERM_ID_MD5'].value` aka `META:PREFERENCES[name='PERM_ID_MD5'].value`: permanent ID to assist locating topics even after renaming. Resolvable at `http://trin.org.au/permalink/(value)`
* `META:CREATEINFO.author`: username which created the topic.
* `META:CREATEINFO.date`: creation date, in unix epoch seconds

Files:
------
### `terms.csv`
TermForm topics from <http://trin.org.au/TaxonProfile/Definitions/>. Includes both WallaceCore terms and terms from documented example profiles.

### `term_attributes.csv`
TermAttributeForm topics (TermForm field definitions) from <http://trin.org.au/TaxonProfile/Builder/>. Each field definition contains:

 * `ExportAs` - The namespace and term as it will be exported
 * `Definition` - Definition of the term by the namespace(Source) creator
 * `IntentandUsage` - Description of how the attribute will by used locally (eg. locally in WC)
 * `Example` - A verbatum (ideally practical) biological example of the term in use.
 * `Source` - Additional human readable textual description for the term
 * `Considered` - Other terms that have been included in the decision to use this term.
 * `Notes` - User Information to assist with using this term.
 * `Namespace` - The URL that the attribute belongs; e.g. <http://purl.org/dc/elements/1.1/>
 * `Type` - A term type describing what and how the term is used, e.g. The term is a LSID and will contain a URI, assigining a Type of RDF:About will identify this term as a resource in the RDF namespace

### `relationships.csv`
RelationshipForm topics from <http://trin.org.au/TaxonProfile/Relationships/>. Each relationship contains:

 * `Source` - The term that is the subject of the mapping link
 * `SourceRev` - The version of the term that is the subject of the mapping link
 * `SourcePermaID` - The peralink of the term that is the subject of the mapping link
 * `Relationship` - The mapping term that describes the relationship between the subject term and the object term
 * `RelationshipRev` - The version of the mapping term that describes the relationship between the subject term and the object term
 * `RelationshipPermaID` - The permalink for the mapping term that describes the relationship between the subject term and the object term
 * `Destination` - The term that is the object of the mapping link
 * `DestinationRev` - The version of the term that is the object of the mapping link
 * `DestinationPermaID` - The permalink for the term that is the object of the mapping link
 * `Notes` - Comments about to the mapping of the Source, relationship and destination relationship
 * `HappinessIndex` - A number intended to indicate how satisfied '9' or dissatisfied '0' relationhsip owners are with this mapping
 * `ImportTopic` - If the relation was imported from an external source, this is the topic which held the data (or its placeholder).
 * `ImportTopicRev` - As above, the revision of the data source (or its placeholder).
 * `ImportTopicPermaID` - As above, the PermaID of the data source (or its placeholder).
