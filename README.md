[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

# neo4j-titanic
Simple data pipeline for the *RMS Titanic* dataset using Python and Pandas library for preprocessing. The data is loaded into a Neo4j graph database for exploration and analysis.

#### -- Project Status: [Active]

## Project Description
The pipeline fetches the *RMS Titanic* dataset, cleans, preprocesses it then loads it into a Docker Neo4j instance where relationships between passengers and other entities such as other passengers, lifeboats, cabins, and other data can be visualized, analyzed and explored.

![Neo4j Browser](./img/neo4jbrowser.png)

## Run Pipeline
Ensure that the Pandas library and Docker are installed. To run the pipeline, clone the repo and run:
```
make graph
```
This will perform the following steps:
* Fetch the data from a URL
* Process it and save it to the ./data folder 
* Pull a Neo4j Docker image and run it 
* Load the processed data using the create_db.cyp file

To explore the database, navigate to the [Neo4j Browser](http://localhost:7474/browser/) and run any Cypher query. For info on using Cypher please visit the [Cypher Basics](https://neo4j.com/developer/cypher-basics-i/) at [Neo4j](https://neo4j.com/).

When finished, ```make clean_up``` will stop Neo4j, remove the container and clean up cache files.

## Sources
A complete *Titanic* dataset is available from [https://data.world/nrippner/titanic-disaster-dataset](https://data.world/nrippner/titanic-disaster-dataset). 

## Authors
[Gregory Lindsey](https://github.com/gclindsey) 

## License
This project is licensed under the MIT License - see the LICENSE file for details

[contributors-shield]: https://img.shields.io/github/contributors/abk7777/neo4j-titanic.svg?style=flat-square
[contributors-url]: https://github.com/abk7777/neo4j-titanic/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/abk7777/neo4j-titanic.svg?style=flat-square
[forks-url]: https://github.com/abk7777/neo4j-titanic/network/members
[stars-shield]: https://img.shields.io/github/stars/abk7777/neo4j-titanic.svg?style=flat-square
[stars-url]: https://github.com/abk7777/neo4j-titanic/stargazers
[issues-shield]: https://img.shields.io/github/issues/abk7777/neo4j-titanic.svg?style=flat-square
[issues-url]: https://github.com/abk7777/neo4j-titanic/issues
[license-shield]: https://img.shields.io/github/license/abk7777/neo4j-titanic.svg?style=flat-square
[license-url]: https://github.com/abk7777/neo4j-titanic/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/gregory-lindsey/