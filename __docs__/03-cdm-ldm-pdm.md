# Data Model

## Conceptual Data Model (CDM)

High-level conceptual data models provide concepts for presenting data in ways that are close to the way people perceive data.

A relationship represents an association among entities : for example, a user can own many articles.

A relationship exists between the user and each article.

We have made CDM with [Mocodo Online](https://www.mocodo.net/).

```
WRITE, 0N USER, 11 ARTICLE
ARTICLE: code_article, title, link, starred, order
BELONGS TO, 1N ARTICLE, 0N CATEGORY

USER: code_user, username, email, password
CREATE, 0N USER, 11 CATEGORY
CATEGORY: code_category, name, color, order
```

Here, you can find our homemade design with Adobe Illustrator :

![CDM](media/wallink_CDM.jpg)

## General Purpose Modeling (or Logical Data Model / GPM or LDM)

Record-based logical data models provide concepts users can understand but are not too far from the way data is stored in the computer.
Three well-known data models of this type are relational data models, network data models and hierarchical data models.

We will use here the relationnal model that represents data as relations, or tables.

Details :

```
ARTICLE ( code_article, title, link, starred, order, #code_user )
The item_code field is the primary key of the table. It was already an ID of the ARTICLE entity .
The title , link , starred and order fields were already simple attributes of the ARTICLE entity .
The code_user field is a foreign key. It migrated by the WRITE functional dependency association from the USER entity , losing its identifying character.

BELONGS TO ( #code_article, #code_category )
The item_code field is part of the primary key of the table. It is a foreign key that migrated directly from the ARTICLE entity .
The code_category field is part of the table's primary key. It is a foreign key that migrated directly from the CATEGORY entity .

CATEGORY ( code_category, name, color, order, #code_user )
The code_category field is the primary key of the table. It was already an identifier of the CATEGORY entity .
The name , color and order fields were already simple attributes of the CATEGORY entity .
The code_user field is a foreign key. It migrated through the CREATE functional dependency association from the USER entity , losing its identifying character.

USER ( code_user, username, email, password )
The code_user field is the primary key of the table. It was already an identifier of the USER entity .
The username , email and password fields were already simple attributes of the USER entity .
```

Here, you can find our homemade design with Adobe Illustrator :

![LDM](media/wallink_LDM.jpg)

## Physical Data Model (PDM)

A physical data model is a database-specific model that represents relational data objects (for example, tables, columns, primary and foreign keys) and their relationships.

A physical data model can be used to generate DDL statements which can then be deployed to a database server.

Using the workbench, you can create a physical data model in several ways:

- Create a blank physical model by using a wizard
- Create a physical model from a template by using a wizard
- Reverse engineer a physical model from a database or a DDL file by using a wizard or by dragging data objects from the Data Source Explorer
- Import a physical data model file from the file system
- Create a physical model by transforming from a logical data model

For PDM, we use the ERD Tool from pgAdmin4

![PDM](media/wallink_PDM.jpg)
