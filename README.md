# Exercice-01-Packet-Tracer
 MiniLab Réseau Cisco – VLANs, DHCP et Routage Inter-VLAN

## Objectif du projet
Mettre en place un **réseau d’entreprise segmenté par VLANs** avec un **routeur Cisco 1941** servant de :
- Routeur inter-VLAN (Router-on-a-Stick),
- Serveur DHCP,

Le projet permet de tester :
- La communication entre VLANs,
- L’attribution dynamique d’adresses IP (DHCP),
- La connectivité complète entre les différents bureaux.

---

## Équipements utilisés
| Type d’équipement | Quantité | Rôle |
|-------------------|-----------|------|
| Routeur Cisco 1941 | 1 | Routage inter-VLAN, DHCP, NAT |
| Switch PT | 3 | Gestion VLAN et trunk |
| **Modules PT-SWITCH-NM-1CFE** | **6** | Ajoutés pour augmenter le nombre de ports disponibles sur les switches |
| Point d’accès Wi-Fi PT-AC | 3 | Accès sans fil (VLAN 20) |
| PC portables | 3 | Clients Wi-Fi |
| PC fixes | 6 | Clients filaires (VLAN 10) |
| Téléphones IP Cisco 7960 | 3 | VLAN VoIP (VLAN 1) |

 *Chaque switch a été étendu avec deux modules PT-SWITCH-NM-1CFE afin de disposer de suffisamment de ports pour les connexions réseau, les liens trunk et les équipements des bureaux.*


---

##  Architecture du réseau

### Topologie simplifiée

          +----------------+
          |   Routeur 1941 |
          | Fa0/1 (TRUNK)  |
          +----------------+
                 |
               [SW1]
               	 |
               [SW2]
		             |
	             [SW3]
