Ce programme simule la circulation de bus entre deux villes (X et Y) à travers un tunnel à voie unique, en utilisant threads pour modéliser les bus et sémaphores pour gérer l’accès au tunnel. Il respecte les règles de circulation :

Pas de croisement → Le tunnel ne contient jamais des bus allant dans des directions opposées en même temps.

Circulation groupée → Plusieurs bus allant dans un même sens peuvent l’emprunter simultanément.

Équité → Lorsqu’un groupe de bus termine son passage, l’accès est donné aux bus en attente du sens opposé.

Allers-retours → Chaque bus effectue 10 trajets aller-retour avec une durée simulée (1 à 1.5 secondes).

L’implémentation utilise un mutex pour protéger les variables partagées et garantir l’exclusion mutuelle, ainsi que deux sémaphores (sem_x et sem_y) pour faire patienter les bus lorsque le tunnel est occupé par l’autre sens.
