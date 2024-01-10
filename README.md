# Repository des documents d'architecture MedHead

Ce document contient tous les documents d'architecture concernant le projet de création du nouveau système de gestion des interventions d'urgence de MedHead Consortium.

## Table of content

* [Principes de l'architecture](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Principes%20de%20l'architecture.pdf)
* [Document de définition de l'architecture](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Document%20de%20d%C3%A9finition%20de%20l'architecture.pdf)
* [CI/CD Documentation](#CI/CD Documentation)
* [Données de référence sur les spécialités NHS](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Donn%C3%A9es%20de%20r%C3%A9f%C3%A9rence%20sur%20les%20sp%C3%A9cialit%C3%A9s%20NHS.pdf)
* [Déclaration des travaux d’architecture.pdf](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/D%C3%A9claration%20des%20travaux%20d%E2%80%99architecture.pdf)
* [Exigences pour le développement de la POC.pdf](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Exigences_pour_le_de%CC%81veloppement_de_la_POC.pdf)


### CI/CD Documentation

La pipeline a été réalisé avec Github Action. 

Les étapes se décomposent de la façon suivantes lors de chaque push sur la branche **MAIN**:

* Build
* Check for changes in micro-service X
* Test
* Publish Docker image

Le détail du workflow est accessible ici : [WorkFlow](https://github.com/OC-P11-MedHead/medhead-app/blob/main/.github/workflows/workflow.yaml)