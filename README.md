# Projet-du-Semestre
Rapport 0 mini projet
Zakaria maouedji & Bechiri abdelghani & kouira noufel


Sommaire : 
1.	Description
2.	conception
3.	Outils 
1.description : Tout développeur d’applications informatiques comprend que les applications conçues spécifiquement pour la plate-forme sur laquelle elles seront exécutées seront plus performantes, plus résilientes et plus faciles à gérer. En effet, le développement pour les plateformes cloud public ou privé ne fait pas exception.
Cependant, peu de gens comprennent exactement comment concevoir et construire une architecture d’application cloud pour les cloud privés ou publics. Ce manque de compétences et d’expérience a conduit à des applications mal conçues pour les plates-formes basées sur le cloud. Par conséquent, ces applications ne fournissent pas la valeur attendue par les entreprises sur la plate-forme cloud.
Voici comment créer une application prête pour le cloud et les concepts d’architecture d’application dont vous aurez besoin pour réussir. Le processus présenté ci-dessous représente une approche étape par étape qui mélange les concepts de développement de logiciels traditionnels et passe en revue les nouveautés du cloud. C’est une collection de meilleures pratiques, de concepts et de procédures pour réussir.
1. Concevoir l’application comme une collection de services
Les applications cloud sont mieux déployées en tant que collection de services cloud ou d’Interface de Programmation Applicative (API). Vous construisez depuis les données aux services, puis combinez ces services dans des services composites ou des applications composites complètes.
C’est une architecture basée ou orientée essentiellement sur le service. Alors que beaucoup comprennent les concepts, les développeurs ont toujours tendance à créer des applications étroitement couplées qui se concentrent sur l’interface utilisateur, plutôt que d’exposer les fonctions sous-jacentes en tant que services qu’elles peuvent exploiter indépendamment.
Lorsque vous développez une architecture d’application pour le cloud, vous traitez des systèmes distribués complexes qui peuvent tirer parti des applications faiblement couplées basées sur de nombreux services pouvant également être dissociés des données (voir « Dissocier les données » ci-dessous). Vous pouvez séparer physiquement les services d’application, les exécuter sur les instances de machine appropriées, et les gestionnaires de service/API ainsi que la technologie de gouvernance qui fournissent des répertoires de services pouvant vous être utiles dans le suivi des nombreux services qui composent votre application.
Des avantages supplémentaires peuvent inclure la réutilisation du service des autres applications ou des services avec une granularité plus large. Vous pouvez diviser les applications en centaines de services sous-jacents qui ont de la valeur lorsqu’ils sont utilisés par d’autres applications. De cette façon, vous ne réinventez pas la roue chaque fois que vous créez une application. Prenons l’exemple d’un service de vérification de crédit que de nombreuses applications utilisent. Combinez-les en un seul service et l’application devient beaucoup plus efficace.
2. Dissocier les données :
Si vous associez étroitement les données à l’application, elles ne trouveront pas un bon accueil dans le cloud. Les cloud privés et publics sont des systèmes distribués complexes qui fonctionnent mieux avec les architectures d’application qui décomposent le traitement et les données en composants séparés.
Vous dissociez les données pour la même raison que vous souhaitez créer l’application à partir de services. Une fois dissocié, vous avez la possibilité de stocker et de traiter les données sur n’importe quelle instance de cloud public ou privé. Par exemple, de nombreuses entreprises insistent pour que leurs données restent sur les serveurs locaux, mais souhaitent tirer parti des instances de la machine virtuelle dans un cloud public.
Toutefois, vous devez considérer la performance. La lecture et l’écriture des bases de données sur Internet ouvert peuvent entraîner une latence et les communications de la base de données peuvent déterminer à quel point vos données sont proches des services et des applications qui doivent en tirer profit.
Envisagez également d’utiliser des systèmes de mise en cache. Ceux-ci fournissent des performances supplémentaires à la base de données en stockant localement des données communément accédées, réduisant ainsi toutes les demandes de lecture de la base de données à la base de données physique. Toutefois, ceux-ci sont mieux intégrés dans l’application et ils doivent être testés avec les données de l’application pour déterminer l’efficacité du cache. Les systèmes qui lisent constamment de nouvelles données ne bénéficient pas autant des caches de la base de données
3. Considérer les communications entre les composants de l’application

Le découplage des applications, à la fois des données et des services, ne signifie pas que votre application est correctement architecturée pour le cloud. Les composants de l’application bavarde qui communiquent constamment entre eux réduisent les performances de l’application globale, étant donné qu’ils sont généralement distribués sur un réseau ou sur Internet ouvert, où la tolérance pour une latence élevée est souhaitable.
Mettre l’accent sur la conception des applications qui optimisent les communications entre les composants de l’application. Par exemple, combinez les communications en un seul flux de données ou un groupe de messages, plutôt que de communiquer en permanence comme si les composants de l’application résidaient sur une plate-forme unique.
4.	Modèle et design pour la performance et la mise à l’échelle
Élargir les considérations sur la manière dont les composants de l’application communiquent pour inclure également les performances globales. Cela comprend la compréhension de la manière dont l’application sera mise à l’échelle sous une charge croissante.
Concevoir pour la performance signifie d’abord construire un modèle qui représente la manière dont l’application se comporte sous une charge croissante. Par exemple, si 1 000 utilisateurs ou plus se connectent en même temps, comment l’application traitera-t-elle le trafic accru sur le réseau, la charge accrue sur les serveurs d’applications et la charge placée sur les bases de données principales ? Vous devez comprendre comment les composants d’application gèrent la charge lorsque le nombre d’utilisateurs augmente jusqu’à 1 000 utilisateurs ou plus.
Cet exemple peut augmenter la charge sur les serveurs d’applications de 80%, la charge sur le réseau de 10% et la charge sur la base de données de 40%. Par conséquent, l’ajout de 1 000 utilisateurs supplémentaires risque de saturer les serveurs d’applications que vous avez configurés et vous devrez générer davantage d’instances de serveur d’applications. La capacité du réseau peut rester la même, mais le nombre d’instances de la base de données doit être augmenté pour gérer toute charge supplémentaire.
Grâce à ce modèle, vous pouvez trouver la meilleure façon de mettre à l’échelle l’application en faisant tourner automatiquement les instances de ressources nécessaires. Dans certains cas, les fournisseurs de services cloud offrent des fonctionnalités de mise à l’échelle automatique où le provisionnement est automatique. La manière la plus efficace consiste cependant à comprendre le profil de la charge de travail de l’application et à définir les étapes de la mise à l’échelle de l’application, ainsi qu’à mettre en place des mécanismes pour garantir qu’elle sera réellement mise à l’échelle.
Enfin, surveillez les performances globales des applications à l’aide des outils de surveillance des performances sensibles aux applications et créez des interfaces au sein de l’application afin de faciliter la surveillance des performances. La façon dont l’application provisionne et dé-provisionne les ressources doit être également innée à l’application.
5.	Adopter la sécurité systémique au sein de l’application
Pour la plupart des personnes qui créent des applications, la sécurité est généralement une réflexion après coup. Toutefois, lorsque vous hébergez une application dans le cloud, la sécurité doit être une priorité. L’architecture de votre application basée sur le cloud devrait permettre la sécurité systémique à l’application. En d’autres termes, celle-ci devrait être conçue et intégrée dans l’architecture de l’application.

Avant de créer votre application, adoptez une approche et une technologie de sécurité qui sera efficace pour le type d’application que vous utilisez et qui répondra à toute question de conformité ou à d’autres problèmes de sécurité au niveau des données. Par exemple, si vous êtes dans le domaine de la santé, vous devez prendre en compte les informations personnellement identifiables ainsi que la loi américaine sur la portabilité et la responsabilité de l’assurance maladie (HIPAA). Vous devez stocker ces données d’une certaine manière, sur des cloud conformes à la norme HIPAA. De plus, l’application devra gérer les données sensibles de manière spécifique avec les niveaux de sécurité requis, tels que le chiffrement.

De manière générale, les applications basées sur le cloud doivent tirer parti de la gestion des identités et des accès (IAM). Les entreprises qui développent les fonctionnalités IAM matures peuvent réduire leurs coûts de sécurité et, plus important encore, devenir beaucoup plus agiles dans la configuration de la sécurité pour les applications basées sur le cloud. En effet, IAM fera partie de plus de 50% des applications existantes migrant vers le cloud public et près de 90% des nouvelles applications construites sur des cloud.

Qui plus est, l’utilisation d’IAM dans les déploiements des applications cloud se répercutera dans l’entreprise, car ces organisations modernisent les approches et les technologies de la sécurité pour s’aligner sur l’utilisation des cloud publics. Dans de nombreux cas, IAM sera fourni en tant que service à l’entreprise. Ce concept d’IAM livré par le cloud conduit rapidement au concept de gestion d’identité centralisée. Au fur et à mesure que vous développez d’autres applications basées sur le cloud en utilisant IAM, chaque application devrait devenir beaucoup plus sûre et plus rentable.

Votre objectif principal est de concevoir la sécurité dans l’application et de tirer parti des fonctionnalités natives du cloud et du système IAM que vous utilisez. Cependant, chaque application a ses propres exigences basées sur les besoins de l’entreprise, et la sécurité diffère toujours d’une entreprise à l’autre.

Construire une architecture d’application prête pour le cloud nécessite de prêter attention à quelques nouvelles choses, mais la plupart des concepts traditionnels sont toujours importants, tels que la conception sonore, les tests et l’apprentissage de vos erreurs. La plupart des développeurs qui déploient des applications sur des plates-formes cloud public ou privé feront des erreurs, mais tant qu’ils reconnaîtront, corrigeront et apprendront de ces erreurs, ils seront sur la bonne voie pour trouver un moyen plus efficace afin de construire des applications dans le cloud.

2. conception 
Ideé de base basé sur uml
Diagrame de classe et diagrame de cas d’utilisation 
![diagram](https://user-images.githubusercontent.com/44177711/48098060-e93ec700-e21b-11e8-9d28-161bb694442e.jpg)

 

3. outils :
1.eclipse 
2.openshift
 


3. my sql
 
