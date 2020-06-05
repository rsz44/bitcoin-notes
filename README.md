---
title: Bitcoin - Limites & Vulnérabilités - EN COURS D'ECRITURE
created: '2020-06-05T17:54:58.670Z'
modified: '2020-06-05T18:00:11.312Z'
---

# Bitcoin - Limites & Vulnérabilités - EN COURS D'ECRITURE

Bitcoin est novateur, c'est une solution hybride qui s'inscrit dans notre modèle économique et technologique globalisé. On a tendance par son [effet waouh](https://www.definitions-marketing.com/definition/effet-waouh-ou-wow/) à lui attribuer plus de propriétés qu'il en a réellement. Effectivement, il s'agit d'une nouvelle technologie et les vertus qu'on peut lui donner doivent être modérés. Son utilisation et son concept doivent être entierrement remis en question pour pouvoir en apprécier une quelquonque valeur ajouté. Les suivantes sections relèvent des problématiques et/ou des débats autour de son système. A la manière de la _retro ingéniérie_, je tente ici une approche de _deboguage_ du système bitcoin, en listant premièrement les failles et vulnérabilités connues. Il est impossible, a mon sens, d'être exhaustif sur toutes les problématiques que le bitcoin soulève, le risque étant de se perdre dans trop de technicité et de manquer de rigueur dans des domaines que je ne maitrise pas.

> On parle ici de secte, de technocratie, de système monétaire déflationniste,

## Nouveaux entrants

__Complexité et hermétisme__

Le _whitepaper bitcoin_ tient en 12 sections sur 9 pages. A première vu, l'explication du bitcoin parait simple. Mais le problème auquelle ce papier répond est très complexe et fait appel à beaucoup de connaissances. Ce papier hérite de beaucoup d'autres papiers du même genre. Y trouver des failles exploitables est donc un véritable casse-tête. Toute personne s'intéressant au bitcoin se heurtera à une masse de connaissances qu'il lui faudra acquérir pour répondre à ses intérrogations légitimes. La phase d'apprentissage est donc très délicate. Pour comprendre le fonctionnement global, il faut pouvoir s'armer de connaissances pointues dans les domaines de la technologie, de l'économie et de la sociologie-politique pour éviter un mindfuck total. C'est un pont interdisciplinaire qui amène l'intéressé sur des pistes semés d'embuches le rendant à la fois très intéressant et dangereux.

Pour qu'un individu puisse accumuler l'ensemble des ces connaissances requises, il lui faudrait investir énormément de temps. De plus qu'expérimenter son fonctionnement est couteux. Si l'on considère alors que la majorité des individus n'investissent qu'une petite partie de leur temp à approfondir ces sujets, alors chacun des participants sont en partie obligés de faire confiance en son fonctionnement et ses acteurs.

Heureusement, beaucoup de débats, de confrontations d'idées, existent autour du bitcoin. Ceux-ci sont plus ou moins hermétiques, intéressants et participent à construire un réseau solide. Le débat fait corp au bitcoin par le système de concensus qui est essentiel a son fonctionnement. En effet, Bitcoin est avant tout un protocole de communication auquel ses participants adhèrent ou non. L'intérêt de ces participants à participer aux débats relève de son intérêt particulier a recevoir une rémunération pour sa participation. Son créateur _Satoshi Nakamoto_ a créé le forum BitcoinTalk après la publication du whitepaper dans l'objectif de créé une première communauté et de permettre les échanges autour de bitcoin.

Au départ avec toute la complexité a laquelle l'utilisateur doit faire face, s'interesser à cette _nouvelle fonctionnalité de notre monde_, la suivre, y engager du temps pour apprendre, c'est quand même un peu comme entrer dans une secte où :
- on adhére a une doctrine;
- il y a un créateur, des signes, un langage, une histoire spécifique;
- on y trouve une communauté contenant beaucoup de gourous, de mentors et de soldats qui en font l'éloge;
- les adhérants y trouvent leur interêt particulier et sont rémunérés pour leur choix;

Ce qui facilite son acceptation au départ c'est que chaque utilisateur y trouve son compte et/ou une utilité particulière. Mais on peut considérer que chacun l'utilise à sa manière, avec sa propre interprétation, ses propres certitudes. Tout cela sans savoir finalement si le système qui subsiste résoud réellement un problème de fond et à l'inverse sans savoir si ce système peut porter préjudice au futur. Bitcoin est un aglomérat de problèmes complexes dont la difficulté est de savoir les balayer en gardant une cohérance et une neutralité sans faille.

> Pour casser en partie cette idée, il est a mon sens très important pour un néophyte de s'assurer de bien connaitre [les interêts de la Blockchain](Les interêts de la Blockchain.md) et le role de ses acteurs qui permet d'apprécier la technologie hors du point de vue de la rémunération. Pour limiter l'effort, l'investissement en temps pour les nouveux entrants et faire accepter cette technologie c'est la pédagogie, la trasmission et la vulguarisation qui prend le relais. Et ce qui parait totallement paradoxal c'est parce qu'on parle ici d'un système qui solutionne une problèmatique de tiers de confiance auquel l'initié faira appel a des tiers confiances, l'intérêt parait donc nul.

> __Ressources__
> 
> - [Les règles de gouvernance de Bitcoin et des protocoles qui s'en inspirent, tel Ethereum](https://bitconseil.fr/hard-fork-soft-fork-et-regles-de-consensus/), par _Benoit Huguet, BitConseil_
> - [La Blockchain, une philosophie crypto-anarchiste](https://iphilo.fr/2019/03/10/derriere-la-blockchain-une-philosophie-cryptoanarchiste-thibaut-gress/), par _Thibaut Gress_
> - [YouTube - Meetup Bordeaux 31 mai 2018](https://www.youtube.com/watch?time_continue=1689&v=4LyMb_2hn8c&feature=emb_title), _Les crypto-monnaies: système de Ponzi ou pas?_ par _Marc Artzrouni_
> - [Bitcoin Obituaries](https://99bitcoins.com/bitcoin-obituaries/), par _99bitcoins.com_


## Dépendance à la clé privé

Ce qui semble être "gênant" avec le Bitcoin, c'est la dépendance unique à la clé privé. On sait qu'il est impossible avec les moyens actuels de trouver la clé privée à partir de la clé publique. Le seul détenteur de la clé privé permet la signature de transactions et donc la légitimité par l'authentification de dépenser les bitcoins d'une clé publique ou adresse.

__Perte de la clé privé__

L'exemple de James Howells dont la clé d'un crédit de [7,500 bitcoins a été perdue](https://cointelegraph.com/news/infamous-discarded-hard-drive-holding-7500-bitcoins-would-be-worth-80-million-today) après la disparition de son disque dur est plutôt parlant. Effectivement, ce dernier aurait par mégarde lors d'un ménage de printemps jeté le disque dur contenant la clé privé d'un compte sur lequel il aurait accummulé 7500 bitcoins minés depuis les débuts de la blockchain.

La somme que représente cette perte est parlante, l'intéressé aurait été jusqu'à vouloir creuser la décharge locale pour retrouver son bien. Il y a aussi l'[histoire similaire](https://news.bitcoin.com/australian-tells-story-of-throwing-away-hard-drive-hosting-1400-bitcoins/) de Campbell Simpson qui aurait perdu 1400 Bitcoin. Ces histoires sont connues pour ce que représente les sommes perdues et l'empathie que l'on éprouve à cet égard.

C'est un défaut notable totallement en dehors du principe de sécurisation du réseau. Une faille semble être présente dans le système de signature: on est ici trop dépendant de "l'utilisateur", de son environnement, de ses propres précautions et il n'y a pas d'instance de référence pour rattraper les incidents utilisateur.

> __Notes__
> 
> - Le bloc contenant les premières transactions originales de James Howells serait le [block 4334](https://www.blockchain.com/btc/block/4334), selon le descriptif du [compte twitter de ce dernier](https://twitter.com/howelzy) (_"Bitcoin since #4334"_). Ce qui permet en regardant le block sur un explorer de remonter à l'adresse [198aMn6ZYAczwrE5NvNTUMyJ5qkfy4g3Hi](blockchain.com/btc/address/198aMn6ZYAczwrE5NvNTUMyJ5qkfy4g3Hi) dont la première transaction reçue au 22/02/2009 est de 400 BTC pour un crédit accumulé de 8000 BTC jusqu'au 26/04/2009 (avec une dernière transaction reçue de 650 BTC). Cette adresse n'aurait jamais émise de transactions.
>
> - Le disque dur perdu contiendrait l'IP de Satoshi Nakamoto, _Ceci n'est pas vérifié_.


__Sécurisation de la clé privée__

![Ouroboros](@attachment/Clipboard_2020-05-01-18-42-38.png)

La sécurité du crédit accumulé sur un compte repose sur la clé privé que seul l'ayant droit a en sa possesion. Il parait donc très important de prendre toutes les précautions nécessaires pour la sauvegarde de sa clé afin de prévenir toute perte. Il reste risqué d'en multiplier les sauvegardes car cela augmente les possibilités d'interception de la clé privé par un autre utilisateur.

Un point qui pourrait paraitre résolu lorsque l'on fait confiance à un tiers qui interface entierrement le fonctionnement du portefeuille et de l'adresse bitcoin en générant et sécurisant les clés privés d'utilisateurs de manière totallement insensible avec des moyens professionnels. C'est le cas de toutes les sociétées d'échanges comme Coinbase, Kraken, Bitstamp, CEX.io, Coinama (et beaucoup d'autres) qui utilisent le réseau bitcoin mais interfacent entierrement l'authentification sur le réseaux et le système de transactions. Ces sociétés peuvent intervenir en support à l'utilisateur dans certains cas comme par exemple pour la perte de son mot de passe de la plateforme, c'est un confort d'utilisation non négligeable pour l'utilisateur et qui leur valent une place de choix pour les premiers achats. Le problème semble aussi résolue lorsque l'on utilise des wallets sécurisés comme Ledger qui permet de stocker et générer plusieurs clés privés à partir d'un support externe et qui interprète cette dernière par le biais d'une puce intégrée et d'un logiciel tiers lors des transactions.

Dans ces schémas on induit une surcouche de sécurisation pour 'colmater' cette dépendance à la clé privé qui fait appel à un tiers sur lequel l'utilisateur doit avoir confiance. On en revient alors au problème initiallement soulevé dans l'introduction du whitepaper bitcoin qui est qu'_aucun mécanisme n’existe pour faire des paiements à travers un canal de communication sans un tiers de confiance_. La sécurisation de la clé privé devient très vite un casse tête pour l'utilisateur sans ces tiers.

__Masse monétaire dormante__

Les cas de James Howells et de Campbell Simpson sont des erreurs utilisateurs sur un réseau naissant. Beaucoup d'autres cas comme ceux-ci sont à relevés et continuent à arriver à différentes échelles. Aussi, il est possible qu'un utilisateur perde ou détruise volontairement la clé privé de son portefeuille, même si ce problème semble incomber au seul détenteur il reste un problème : tous les bitcoin envoyés à cette adresse seraient alors de fait bloqués, créant alors de véritables adresses poubelles à cash. Si ces erreurs ont éxistés, on peut considérer naturellement que d'autres suiviendront et que la somme de bitcoin perdues ne fait qu'augmenter.

![Serge Gainsbourg brulle un billet](@attachment/Clipboard_2020-05-01-18-58-49.png)

Sans une "copie" de la clé, les bitcoins "existent" sur le réseau, mais sont de fait définitivement verrouillés car ils ne sont plus échangeables. Le problème étant c'est que cette masse dormante est définitivement perdue tant que la clé privé n'est pas retrouvé. Le nombre de bitcoin étant prévu fixe, il y a un donc un écart entre la masse monétaire existante et celle en pratique accessible, sur le cas unique de James Howells c'est une différence de 0,03%.

Nous pouvons avoir un premier indicateur du nombres de bitcoin dormants en explorant la blockchain et en déterminant plusieurs paramètres. Le site [Bitinfocharts](https://bitinfocharts.com/top-100-dormant_8y-bitcoin-addresses.html) ou encore ce [Spreadsheets](https://docs.google.com/spreadsheets/d/1xTROekDerP1TPOB3SOD_1bbQr580BPqbhF3YHdO96pw/edit?usp=sharing) ([.xlsx au 4 mai 2020](@attachment/Dormant Bitcoin Addresses with a balance of 25btc or more.xlsx)) qualifient ces potentielles adresses vérouillés. Pour faire l'hypothèse d'une somme dormante il faut regarder plusieurs choses :
- La date de première utilisation de l'adresse
- La date de la dernière transaction émise sur l'adresse
- La date de la dernière transaction reçue sur l'adresse
- La somme de bitcoin qu'elle contient à date

![Somme des bitcoins 'dormants' sur 8 ans du 1 main 2012 au 1er mai 2020](@attachment/Clipboard_2020-05-04-13-35-59.png)

Si l'on utilise la classification de BitInfoCharts, la masse dormante en mai 2020 pour 8 ans d'inactivité et + serait de 2,46 millions de BTC. A cette même date le nombre de [bitcoin en circulation](https://www.blockchain.com/charts/total-bitcoins) est de 18,36 millions. En effectuant un pourcentage $(100*2,46)/18,36=13,40$ il y aurait 13,40 % de bitcoins 'dormants' du nombre totale de bitcoin en circulation. Si l'on augmente la date de dernière activité (en émission ou réception) cette part tant a augmenter. Par exemple, si on l'augmente ljusqu'à il y a 1 an, alors le nombre de bitcoins considérés dormants est de 17,51 millions, soit 95,37 % de la masse circulante. Cette __indicateur est totallement imparfait__ car il ne prend pas en compte le __temps de détention__ qui est inconnu. Ce que calcul l'indicateur ce sont les liquidités qui ne sont pas utilisés et qui ne le seront peut-être jamais si l'on reprend le cas de la perte de la clé privée. Mais rien n'indique vraiment que ces bitcoins ne sont pas simplement du pure _holding_. Ce dernier point est important pour modérer l'interprétention que l'on peut en faire. Cela permet seulement de faire une première estimation de bitcoins potentiellement innaccessibles ou inutilisés mais ne représente en aucun cas le nombre réel de bitcoin innaccessibles car c'est indéterminable. Le Spreadsheet contient un _score zombie_ qui classifie en ce sens et reprend, par image, l'idée que l'adresse peut être morte et/ou vivante.

En conclusion et transition, si il s'avère que ce nombre de bitcoin innaccessibles augmente ce phénomène réduit le nombre réel de bitcoin en circulation et ce qui pourrait créer de la déflation.

__Pédagogie, transmission et vulguarisation__

(_REDACTION EN COURS_)

__Technocratie et Bitcoin Core__

(_REDACTION EN COURS_)

> __Sources__
>
> - [Infamous Discarded Hard Drive Holding 7,500 Bitcoins Would be Worth $80 Million Today](https://cointelegraph.com/news/infamous-discarded-hard-drive-holding-7500-bitcoins-would-be-worth-80-million-today), par _CoinTelegraph_
> - [Australian Tells Story of Throwing Away Hard Drive With 1400 Bitcoins](https://news.bitcoin.com/australian-tells-story-of-throwing-away-hard-drive-hosting-1400-bitcoins/), par _Bitcoin.com_
> - [Dormant Bitoin](https://bitinfocharts.com/top-100-dormant_8y-bitcoin-addresses.html), par _BitInfoCharts_

## Preuve de travail, Proof of Work

Sur bien des points la preuve de travail est le concensus qui parait le plus évident. C'est le choix idéal qui permet permet d'attacher une valeur concrète au Bitcoin et rendant possible son existance dans notre modèle économique. Les débats et les alternatives décritent ci-dessous se sont présentés après la mise en lumière de ce concensus.

__Problème 'écologique' de la preuve de travail__

(_REDACTION EN COURS_)

## Economie

(_REDACTION EN COURS_)

__La valeur du bitcoin__
__Système monétaire déflationniste__
__Spéculation et volatilité__
__Compétitivité et duplication__
