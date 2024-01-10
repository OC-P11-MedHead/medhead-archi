# Repository des documents d'architecture MedHead

Ce document contient tous les documents d'architecture concernant la création du nouveau système de réservation d'urgence de lit d'hôpitaux de MedHead Consortium.
nn
b
b
b
b
b
b
b
b
b
b
b
b
b
b
b
b
b
## Table of content

* [CI/CD Documentation](#CI/CD)
* [Principes de l'architecture](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Principes%20de%20l'architecture.pdf)
* [Document de définition de l'architecture](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Document%20de%20d%C3%A9finition%20de%20l'architecture.pdf)
* [Données de référence sur les spécialités NHS](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Donn%C3%A9es%20de%20r%C3%A9f%C3%A9rence%20sur%20les%20sp%C3%A9cialit%C3%A9s%20NHS.pdf)
* [Déclaration des travaux d’architecture.pdf](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/D%C3%A9claration%20des%20travaux%20d%E2%80%99architecture.pdf)
* [Exigences pour le développement de la POC.pdf](https://github.com/OC-P11-MedHead/medhead-archi/blob/main/Exigences_pour_le_de%CC%81veloppement_de_la_POC.pdf)


### CI/CD

La pipeline a été réalisé avec Github Action. 

Les étapes de la pipeline CI/CD se décomposent de la façon suivante lors de chaque **push** sur la branche **MAIN**:

| Etape | Description |
| ----- | ----------- |
| Build | Création de l'environnement Linux, Java.. |
| Check for change in MS X | Détection s'il y a eu des changements sur les différents micro-services pour effectuer les tests |
| Test | Si un changement a eu lieu sur un micro-service, la phase de test est exécutée |
| Publish Docker image | Une image est publiée sur le docker hub du projet [Docker Hub](https://hub.docker.com/repositories/yvalero) |

Le détail du workflow est accessible ici : [WorkFlow](https://github.com/OC-P11-MedHead/medhead-app/blob/main/.github/workflows/workflow.yaml)

> L'étape de déploiement n'est pas réalisée dans le cadre du POC, elle devra être mise en place lors de la mise à disposition de l'environnement de PRE-PROD, PROD.