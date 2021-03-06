==================================
MongoDB Documentation Organization
==================================

This document provides an overview of the global organization of the
documentation resource. Refer to the notes below if you are having
trouble understanding the reasoning behind a file's current location,
or if you want to add new documentation but aren't sure how to
integrate it into the existing resource.

Don't hesitate to open a ticket in the `Documentation Jira Project
<https://jira.mongodb.org/browse/DOCS>`_ or be in contact with someone
on the `documentation team <mailto:docs@10gen.com>`_ if you have any
questions.

Global Organization
-------------------

Indexes and Experience
~~~~~~~~~~~~~~~~~~~~~~

There are two "index files," for the documentation
project. "``/contents.txt``" and "``/index.txt``". The "contents" file
provides an index and top level tree of all documentation in the
resource and Sphinx uses this organization to power the "Next" and
"Previous" page functionality and all overarching outlines of the
resource. The "index" file is not included in the "contents" file (and
thus builds will produce a warning here) and is the page that users
will land on first when visiting the resource.

Having separate "contents" and "index" files provides a bit more
flexibility with the organization of the resource while also making it
possible to customize the primary user experience.

Additionally, in the top level of the "``source/``" directory, there
are a number of "topical" index or outline files. These (like the
"index" and "contents" files) use the "``.. toctree::``" directive to
provide organization within the documentation. The topical indexes
combine to create the index in the contents file.

Topical Indexes and Meta Organization
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Because the documentation on any given subject exists in a number of
different locations across the resource the "topical" indexes provide
the real structure and organization to the resource. This organization
makes it possible to provide great flexibility while still maintaining
a reasonable organization of files and URLs for the
documentation. Consider the following example:

     Given that topic such as "replication," has material regarding
     the administration of replica sets, as well as reference
     material, an overview of the functionality, and operational
     tutorials, it makes more sense to include a few locations for
     documents, and use the meta documents to provide the topic-level
     organization.

Current topical indexes include:

- getting-started
- administration
- applications
- reference
- mongo
- sharding
- replication
- faq

Additional topical indexes are forthcoming.

The Top Level Folders
---------------------

The documentation has a number of top-level folders, that hold all of
the content of the resource. Consider the following list and
explanations below:

- *administration* - contains all of the operational and architectural
  information that systems and database administrators need to know in
  order to run MongoDB. Topics include: monitoring, replica sets, shard
  clusters, deployment architectures, and configuration.

- *applications* - contains information about application development
  and use. While most documentation regarding application development
  is within the purview of the driver documentation, there are some
  larger topics regarding the use of these features that deserve some
  coverage in this context. Topics include: drivers, schema design,
  optimization, replication, and sharding.

  - *applications/use-cases* - contains use cases that detail how
    MongoDB can support various kinds uses and application designs,
    including in depth instructions and examples.

- *core* - contains overviews and introduction to the core features,
  functionality, and concepts of MongoDB. Topics include: replication,
  sharding, capped collections, journaling/durability, aggregation.

- *reference* - contains references and indexes of shell functions,
  database commands, status outputs, as well as manual pages for all
  of the programs come with MongoDB (e.g. ``mongostat`` and
  ``mongodump``.)

- *tutorial* - contains operational guides and tutorials that lead
  users through common tasks (administrative and conceptual) with
  MongoDB. This includes programming patterns and operational guides.

- *faq* - contains all the frequently asked questions related to
  MongoDB, in a collection of topical files.
