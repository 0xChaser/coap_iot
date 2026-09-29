# Module 1

1. `2.05 Content`.
2. `2.04 Changed`.
3. `4.00 Bad Request`, car seules les valeurs `on` et `off` sont acceptées.
4. `aiocoap-client -m put -e "off" coap://localhost/led`
5. Le GET renvoie les deux entrées numérotées, horodatées et séparées par un retour à la ligne.
6. `2.02 Deleted`.

# Module 2

1. 5 notifications en 10 secondes.
2. Oui, les deux clients reçoivent les notifications.
3. Le polling produit 120 messages, soit environ 2 400 octets. L’observation produit 14 messages, soit environ 280 octets.
4. Suivre les changements de température et recevoir une alerte lors d’un changement d’humidité.
5. La méthode `updated_state()`.

# Module 3

1. 8 ressources.
2. L’attribut `;obs` indique que la ressource est observable.
3. Le payload de `/biglog` fait 1 784 octets. Il est téléchargé en 7 blocs de 256 octets au maximum.
4. Le blockwise permet de découper une image trop volumineuse pour un datagramme UDP en blocs adaptés à la MTU, puis de la reconstituer.
5. Le multicast permet d’envoyer une seule requête aux 200 capteurs au lieu de les contacter un par un.
