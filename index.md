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

![ER Model](https://github.com/alihamzaunitn/kdi-educationtrentino/blob/master/Documentation/ERmodel_formalModelingPhaseV2.png)

### ETG Model
From the model, ETG were created that define the conceptual relation of the entitites that are involved in the scope of the project. ETG in form of an OWL file that was created using the Protege tool which provides great support in this.
[Link of the ETG Folder](https://github.com/alihamzaunitn/kdi-educationtrentino/blob/master/Teleologies/Formal%20Modeling/education%20in%20trentino%20-%20kdi%20project%20ontology%20v2.owl)


**Bold** and _Italic_ and `Code` text

[Link](url) and ![ER Model](https://github.com/alihamzaunitn/kdi-educationtrentino/blob/master/Documentation/ERmodel_formalModelingPhaseV2.png)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/alihamzaunitn/kdi-educationtrentino/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
