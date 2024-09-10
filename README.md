# versioning-ontology
This ontology represents generic concepts for doing semantic versioning and dependency tracking for a suite of artifacts for semantic systems in production.  Versioned artifacts are given semantic version numbers of the form "N.N.N" (as described in https://semver.org/). This ontology provides the ability to state that a particular version of one ontology depends on the semantic version number of another ontology being in a certain range.  For example, version 6.3.0 of a disease taxonomy depends on:
1. the version of a disease ontology being at least 3.1.0 and less than 4.0.0.
2. the version of gist core being between at least 12.1.0 and less than 13.0.0.

The need for specifying such dependencies arises when ontologies use terms from imported ontologies.

Several SPARQL queries are provided to perform the following tasks:
1. Find all versioned artifacts and their dependencies.
2. Find all cases where a version dependency requirement is not met. Return result in English.
3. Validate several types of dependency conflicts, returning results as a SHACL `ValidationReport`.
