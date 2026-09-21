# Boutique — plateforme e-commerce à microservices

**Boutique** est une application e-commerce de démonstration, construite en microservices multi-langages et opérée par **boutique-systems**. Ce dépôt est un fork de [Online Boutique](https://github.com/GoogleCloudPlatform/microservices-demo)
(`GoogleCloudPlatform/microservices-demo`).

Objectif : disposer d'une base applicative réaliste pour pratiquer l'opération en production — CI/CD, Kubernetes, observabilité, sécurité, GitOps et migrations.

## Déploiement & opération

L'application sera opérée sur **AWS EKS** :

- **Infrastructure** (Terraform) : [`boutique-infra`](https://github.com/boutique-systems/boutique-infra)
- **GitOps** (ArgoCD) : [`boutique-gitops`](https://github.com/boutique-systems/boutique-gitops)
- **Documentation** (ADR, runbooks, post-mortems) : [`boutique-docs`](https://github.com/boutique-systems/boutique-docs)

## Fork

Ce dépôt fork `GoogleCloudPlatform/microservices-demo`. L'upstream est conservé en remote pour synchroniser les mises à jour.

## Services

| Service | Langage | Rôle |
| --- | --- | --- |
| `frontend` | Go | Interface web |
| `cartservice` | C# (.NET) | Panier (état en Redis) |
| `productcatalogservice` | Go | Catalogue produits |
| `currencyservice` | Node.js | Conversion de devises |
| `paymentservice` | Node.js | Paiement |
| `shippingservice` | Go | Devis de livraison |
| `emailservice` | Python | Notifications e-mail |
| `checkoutservice` | Go | Orchestration du checkout |
| `recommendationservice` | Python | Recommandations |
| `adservice` | Java | Publicités |
| `loadgenerator` | Python | Génération de charge (tests) |

## Stack technique

Go, Python, Node.js, Java, .NET · HTTP / gRPC · Redis · OpenTelemetry.
