This repository contains material regarding Scholarly Ontology. An ontological framework for modeling scholarly processes. Fruther information can be found in the following references:

1) Scholarly Ontology: modelling scholarly practices. Pertsas, Constantopoulos. IJDL. 2016. DOI: 10.1007/s00799-016- 0169-3
2) Contextualized Integration of Digital Humanities Research: Using the NeMO Ontology of Digital Humanities Methods. Constantopoulos, Hughes, Dallas, Pertsas, Papachristopoulos, Christodoulou. Digital Humanities (DH). Krakow. 2016

# Scholarly Ontology

Scholarly Ontology (SO) is an ontological framework for representing knowledge in the scholarly domain. It offers a flexible mechanism for modeling scholarly practices in the form of research processes that are carried out by scholars and represent their work. Modeling scholarly work with SO, allows for easy access to information, encoded in such a way that can answer questions of the form who does what, how, why, where, etc.

The ontology evolves around the central notion of Activity (i.e. a biological experiment, an archeological excavation, a medical survey, etc.), capturing its various perspectives: Resource, comprising concepts such as ContentItem (i.e. bibliographic references, articles, figures, tables, equations, etc.), Topic, etc. that model what is produced, used or documents an activity; Procedure, comprising the Methods (i.e. procedures) that describe how an activity is conducted; and Agency, comprising concepts such as Actors or Goals, that model who is participating in the activities or why they are conducted.

### Activity Perspective

Activities are intentional acts carried out by instances of the Actor class; they have duration, and occur at a specific time and place. They are real processes, as opposed to plans, or procedures for carrying out processes. Projects and Courses are two kinds of activity of particular interest in the scholarly domain that warrant specialized descriptions and are represented as subclasses of Activity.

Scholalry Ontology distinguishes three broad kinds of object involvement in an activity: input, output and tool. These are further specialized by the properties produces, uses and isDocumentedIn regarding the involvement of information resources and the properties triggeredBy, hasObjective and resultIn regarding the involvement of assertions or their specializations.

### Procedure Perspective

Like in business process modelling, we distinguish between the procedure that prescribes how to perform a specific act and the act itself. In SO procedures or ‘recipes’ are captured by the Method class, while acts are captured by the Activity class. A method hasDescription explaining what it does, isEmployedIn an activity, isEmployedBy actors, comesFrom some discipline, may be influencedBy a school of thought, be referencedIn bibliography (a content item), or taughtIn some courses. A structured description of a method is enabled by the hasPart property yielding a recursive analysis into steps and the previous property establishing causal ordering of steps.

A method may prescribe specific information resource types for inputs and outputs, media types as formats and tools. Finally, methods are designed to address specific goals and treat -through their employment- specific research questions.

### Resource Perspective

Any conceptual object that has a concrete representation, borne by man-made carriers, is considered as a unit of information, independently of those carriers (paper, hard disk, etc.) and is treated as a resource that can be characterized by its topic, type, and format or be described by a set of metadata. In addition, information resources can be used as inputs or outputs of activities. InformationResourceType, and MediaType constitute controlled vocabularies describing the type and format of information resources and can be imported from authorities, such as the Marc21 bibliographic standard and the Internet Assigned Numbers Authority (IANA). Instances of InformationResource can be grouped in aggregations and modelled through the use of an established data model, such as OAI-ORE.

### Agency Perspective

The agency perspective captures the ‘who’ and ‘why’ aspects of the domain by focusing on goals of actors and the intentional context of other relationships. Existing ontologies such as FOAF and SiOC can be reused in conjunction with SO in order to capture the social and community aspects of actors. This can be achieved by further specializing the corresponding SO concepts: Person, Group, Project, Topic, ActorRole and InformationResource.

Actors’ goals constitute the objectiveOf activities and can be addressedBy instances of Method. In addition, they can be further decomposed into more refined goals or be dependent upon other goals as indicated by the comprises and dependsOn properties respectively. Thus the notion of goal captures the successive refinement from high-level objectives down to narrower goals, as well as the manifestation of chains of dependency among goals.

# Activity Types

Scholarly Ontology allows the indirect linking of concepts through the various Type classes. Especially in the case of ActivityType the hierarchically organized lexical terms serve multiple purposes: (1) they denote the nature of activities; (2) they provide context for other SO relations (e.g. employs, usesTool, etc.) and function as semantic bridge between various perspectives; (3) they provide a retrieval index; (4) they function as a “gateway” through which other taxonomic structures (along with the resources annotated by them) can be imported/mapped (e.g. TaDIRAH, Oxford ICT, etc.).
