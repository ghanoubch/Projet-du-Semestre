# Projet-du-Semestre
Rapport 0 mini projet
Zakaria maouedji & Bechiri abdelghani & kouira noufel


Sommaire : 
1.	Description
2.Architecture globale de l'application (service web)
3.conception
4.Outils 

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

2.Architecture globale de l'application (service web)
Architecture d'un service Web :
Les services Web reprennent la plupart des idées et des principes du Web (HTTP, XML), et les appliquent à des interactions entre machines. Comme pour le World Wide Web, les services Web communiquent via un ensemble de technologies fondamentales qui partagent une architecture commune. Ils ont été conçus pour être réalisés sur de nombreux systèmes développés et déployés de façon indépendante. Les technologies utilisées par les services Web sont HTTP, WSDL, REST, XML-RPC, SOAP et UDDI.
REST

REST (Representational State Transfer) est une architecture de services Web. Élaborée en l'an 2000 par Roy Fiedling, l'un des créateurs du protocole HTTP, du serveur Apache HTTPd et d'autres travaux fondamentaux, REST est une manière de construire une application pour les systèmes distribués comme le World Wide Web.
XML-RPC

XML-RPC est un protocole simple utilisant XML pour effectuer des messages RPC. Les requêtes sont écrites en XML et envoyées via HTTP POST. Les requêtes sont intégrées dans le corps de la réponse HTTP. XML-RPC est indépendant de la plate-forme, ce qui lui permet de communiquer avec diverses applications. Par exemple, un client Java peut parler de XML-RPC à un PerlServer ! o_O
SOAP

SOAP (Simple object Access Protocol) est un protocole standard de communication. C'est l'épine dorsale du système d'interopérabilité. SOAP est un protocole décrit en XML et standardisé par le W3C. Il se présente comme une enveloppe pouvant être signée et pouvant contenir des données ou des pièces jointes.
Il circule sur le protocole HTTP et permet d'effectuer des appels de méthodes à distance.
WSDL

WSDL (Web Services Description Language) est un langage de description standard. C'est l'interface présentée aux utilisateurs. Il indique comment utiliser le service Web et comment interagir avec lui. WSDL est basé sur XML et permet de décrire de façon précise les détails concernant le service Web tels que les protocoles, les ports utilisés, les opérations pouvant être effectuées, les formats des messages d'entrée et de sortie et les exceptions pouvant être envoyées.
UDDI

UDDI (Universal Description, Discovery and Integration) est un annuaire de services. Il fournit l'infrastructure de base pour la publication et la découverte des services Web. UDDI permet aux fournisseurs de présenter leurs services Web aux clients.

Les informations qu'il contient peuvent être séparées en trois types :

    les pages blanches qui incluent l'adresse, le contact et les identifiants relatifs au service Web ;

    les pages jaunes qui identifient les secteurs d'affaires relatifs au service Web ;

    les pages vertes qui donnent les informations techniques.
Fonctionnement des services Web :
Le fonctionnement des services Web s'articule autour de trois acteurs principaux illustrés par le schéma suivant :

![fonctionnement des service web](https://user-images.githubusercontent.com/44177711/48481049-7d0c2680-e80c-11e8-8de9-086be5b8bbfb.jpg)



2. conception 
Ideé de base basé sur uml
 
![a](https://user-images.githubusercontent.com/44177711/49110109-d9e7f200-f28c-11e8-902b-c60ff329634b.png)


 

3. outils :
1-Spring tools Suite 4 


![b](https://user-images.githubusercontent.com/44177711/49112463-1fa7b900-f293-11e8-9b05-5a6f2c8c3bc6.jpg)


Spring Tools 4 est la nouvelle génération d’outils Spring pour votre environnement de codage préféré. Largement reconstruit à partir de zéro, il fournit un support de premier ordre pour le développement d'applications d'entreprise basées sur Spring, que vous préfériez Eclipse, Visual Studio Code ou Atom IDE




2-eclipse 
![eclips](https://user-images.githubusercontent.com/44177711/48098283-8ef23600-e21c-11e8-95bc-7e9d0950d93e.jpg)



Eclipse est un projet, décliné et organisé en un ensemble de sous-projets de développements logiciels, de la fondation Eclipse visant à développer un environnement de production de logiciels libre qui soit extensible, universel et polyvalent, en s'appuyant principalement sur Java.

Son objectif est de produire et fournir des outils pour la réalisation de logiciels, englobant les activités de programmation (notamment environnement de développement intégré et frameworks) mais aussi d'AGL recouvrant modélisation, conception, test, gestion de configuration, reporting… Son EDI, partie intégrante du projet, vise notamment à supporter tout langage de programmation à l'instar de Microsoft Visual Studio.


3-openshift
 ![openshift](https://user-images.githubusercontent.com/44177711/48098430-ff00bc00-e21c-11e8-834c-d1ca585078f1.jpg)


OpenShift est un service de plate-forme en tant que service de la société Red Hat.

Le logiciel est libre, son projet amont s'appelle OpenShift Origin3. Une version appelée OpenShift Enterprise est proposée pour l'hébergement en site propre ou en cloud computing4.

OpenShift supporte également des applications web, si elles mêmes sont supportées par Red Hat Enterprise Linux.



4-my sql
![mysql](https://user-images.githubusercontent.com/44177711/48098478-2f485a80-e21d-11e8-832d-c72bd050bae9.jpg)




Oracle SQL Developer est un environnement de développement intégré (EDI) multi-plateforme, fourni gratuitement par Oracle Corporation et utilisant la technologie Java (Java Development Kit). C'est un outil graphique permettant d'interroger des bases de données Oracle à l'aide du langage SQL.

 
