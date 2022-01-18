## Education In Trentino - Data Integration

Reusability has a vital role in the Data Integration process defined by the ITelos methodology. This project is about the inegration of multiple hetegenious data sources following the standard Data Integration tools and technologies in order to produce useful expolitable knowledge graph maximizing the reuseability of the resources used. In the followingsections, you can find the details of the resources used including the breif description of each of them and links to the resources. 

Scope of the project was a **“A service that will help parent and student to find schools, including details about the school and courses offered, in the region of Trentino based on city, commune, school type, course duration and teaching activities schedules.**


### Datasets

Collection of data that supports the purpose of the project was one of the challenging part of
this work. OPENdata Trentino was use to collect the data sets related to the education data in
Trentino. It is a web portal that contains huge amount of public datasets owned by Autonomous
Province of Trento. 

[Link of Autonomous
Province of Trento](https://dati.trentino.it/)


From the above mentioned portal, following datasets downloaded:
• First dataset that was downloaded is “Trentino educational institutions” . The dataset is
in XML format. It contains List of educational institutions in Trentino, with information such
as, type of institution, site, training offer, contact information, address, school type, number
and list of course offered. 

[Link of Trentino educational institutions](https://dati.trentino.it/dataset/istituzioni-scolastiche-trentino)

Second data set downloaded from the website was “Study courses of the Trentino schools”
that contains list of study courses of Trentino schools with description and status of activity.The dataset is in XML format. This dataset has extra information, like starting year and duration, about the study courses being taught at the school.

[Link of Study courses of the Trentino schools](https://dati.trentino.it/dataset/corsi-di-studio-delle-scuole-trentine)

List of all the communes in the province of Trento was manually downloaded from a website and cleaned.

[Link of Trentino Comune Data](https://en.wikipedia.org/wiki/Municipalities_of_Trentino)


### Knowledge Resource + Schemas 

Follwing were the reference teleologies initially collected to satisfy the purpose of the project
along the integration process :
- [https://schema.org/EducationalOrganization](https://schema.org/EducationalOrganization)
- [https://schema.org/School](https://schema.org/School)
- [https://schema.org/ElementarySchool](https://schema.org/ElementarySchool)
- [https://schema.org/HighSchool](https://schema.org/HighSchool)
- [https://schema.org/MiddleSchool](https://schema.org/MiddleSchool)
- [https://schema.org/Preschool](https://schema.org/Preschool)
- [https://schema.org/City](https://schema.org/City)
- [https://schema.org/Person](https://schema.org/Person)
- [https://schema.org/Course](https://schema.org/Course)

### ER Model

Based on the knowledge and data resources collected,follwing was the ER modelthat was created on the knowledge level which was later modified and also mapped to the refined datasets using data mapping tools.

![test image](https://www.datapine.com/blog/wp-content/uploads/2016/08/data-interpretation-art.jpg)
![ER Model](https://github.com/alihamzaunitn/kdi-educationtrentino/blob/master/Documentation/ERmodel_formalModelingPhaseV2.png)

### ETG Model
From the model, ETG were created that define the conceptual relation of the entitites that are involved in the scope of the project. ETG in form of an OWL file that was created using the Protege tool which provides great support in this.
[Link of the ETG Folder](https://github.com/alihamzaunitn/kdi-educationtrentino/blob/master/Teleologies/Formal%20Modeling/education%20in%20trentino%20-%20kdi%20project%20ontology%20v2.owl)


### Knowledge Graph

The goal of the data integration project was to construct a solution that can answer CQs (competency questions). Unfortunately due to some unforeseen errors, we were not able to explored the final graph in the GrapghDb or any other similar tool for graph exploration. Invalid Base IRI
error was encountered while importing the files in the GraphDb. We tried to fix the issue by
redoing the mapping in the karmalinker and again generated the RDF graph files but this did
not fix the issue. Despite doing the necessary research, we could not track down the issue. As
result of this we were not able to properly explore the finally produced Knowledge Graph. We
were able to import only part of graphs in the GraphDB that are also shown in the figures
below.

![Graph1](https://github.com/alihamzaunitn/kdi-educationtrentino/blob/master/Documentation/Screenshot%202022-01-09%20022225.png)
![Graph2](https://github.com/alihamzaunitn/kdi-educationtrentino/blob/master/Documentation/comune%20graph.png)

Associated properties to each of the concepts can also be seen on the detailed widget on the
right side. Despite this major setback, the analysis of the potential usage of the KG can be done on
the conceptual bases following the modeling/entity matching done in the karmalinker. We tried
to answer CQs following the incoming/outgoing links and in most of the cases we were able
to find the desired data. For example, if someone wants to search all schools in Trento, we
can very well start from the comune data-set looking for Trento comune and then following its
conceptual link in the schools dataset to find out link of all school that are located in Trento
comune. All of this reasoning was done manually without use of any tool due to the reason
mentioned above. A possible solution of this problem could be by making sure that there is no
entity that is un-mapped or improperly mapped in the karmalinker and then generate the RDF
graphs. We could not do this as per time limitation and limited availability of the tools involved
these phases of the project.

### GITHUB Repository
All of the mentioned work can be found in the below github respository (master branch).
[Github Reposity Link - KDI Education In Trentino](https://github.com/alihamzaunitn/kdi-educationtrentino/tree/master)


