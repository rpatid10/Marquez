# Marquez
Marquez is an open source metadata service for the collection, aggregation, and visualization of a data ecosystem's metadata. It maintains the provenance of how datasets are consumed and produced, provides global visibility into job runtime and frequency of dataset access, centralization of dataset lifecycle management, and much more. Marquez was released and open sourced by WeWork.


NameSpace:
A namespace enables the contextual grouping of related jobs and datasets. Namespaces must contain only letters (a-z, A-Z), numbers (0-9), underscores (_), dashes (-), colons (:), slashes (/), or dots (.). A namespace is case-insensitive with a maximum length of 1024 characters. Note jobs and datasets will be unique within a namespace, but not across namespaces.

Sources:
A source is the physical location of a dataset such as a table in PostgreSQL, or topic in Kafka. A source enables the grouping of physical datasets to their physical source.

Dataset:
A dataset has an owner, unique name, schema, version, and optional description. A dataset is contained within a datasource. A datasource enables the grouping of physical datasets to their physical source. A version pointer into the historical set of changes is present for each dataset and maintained by Marquez. When a dataset change is committed back to Marquez, a distinct version ID is generated, stored, then set to current with the pointer updated internally.

Job:
All job objects are immutable and are uniquely identified by a generated ID. Marquez will create a version of a job each time the contents of the object is modified. For example, the location of a job may change over time resulting in new versions. The accumulated versions can be listed, used to rerun a specific job version or possibly help debug a failed Job run.

Run Job:
Creates a new run object for a Job.

start Job:
Marks the run as RUNNING for a Job.

Tag: 
Creates a new tag object.

Lineage:
Create a dependency(flow) b/w all the object.
.


