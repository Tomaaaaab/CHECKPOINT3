Exercice 1 - VM Windows

Partie 1 - Gestion des utilisateurs

Q.1.1.1
![1](https://github.com/user-attachments/assets/83c70b6f-acbd-43fc-ba82-0e1fe6948a18)

![2](https://github.com/user-attachments/assets/1bf0cae7-f4c4-4418-b437-3654fcd4175a) 

![3](https://github.com/user-attachments/assets/9f59c498-99f8-4df6-b6c7-935944a60e49)

![4](https://github.com/user-attachments/assets/67e92aa2-a042-4835-8ef1-7075156f2f01)

![5](https://github.com/user-attachments/assets/52128e05-d78a-4c11-b31b-13812ba5309c)

![6](https://github.com/user-attachments/assets/240366c0-3d0d-49cb-ac4e-a3fca162a203)


Attribuer un mot de passe par défaut pour une première connexion

![Attribuer un mot de passe par défaut pour une première connection](https://github.com/user-attachments/assets/9e2438d6-32ae-418f-b0b2-fe4c93da851b)




Copie des attributs
![Copier les attributs ](https://github.com/user-attachments/assets/2ff4ae8b-251d-44a6-9da6-55c4b8a77ed5)


Désactivation du compte sortant 
![Désactiver le copte de Kelly](https://github.com/user-attachments/assets/2dc754c1-06d8-47c3-b72a-e5e0e9ab60c1)


Modification du titre
![Modification du titre](https://github.com/user-attachments/assets/267e1ae4-ad4e-4e3c-bf2a-137e951552c8)


Renseigner les champs
![Renseigner les champs](https://github.com/user-attachments/assets/865ed69c-f02a-4dd9-b075-86ae26ee2436)


Résumé de la création d'utilisateur avec copie des attributs
![Résumé de la création d'utilisateur avec copie des attributs](https://github.com/user-attachments/assets/d8210997-625d-4c10-8008-38fd0206ed89)





Q.1.1.2 
Création d'une OU
![Création d'une OU](https://github.com/user-attachments/assets/eeba8aa9-bb23-46b9-bab4-18f77e5598b8)

Déplacer utilisatur désactivé


![Déplacer utilisateur désactivé](https://github.com/user-attachments/assets/6c32cb11-bf9f-4aa0-9b7d-f5439b2a5805)


Q.1.1.3 
Création dossier perso et ajout mention d'archivage
![Création dossier lionel et achivage dossier kelly](https://github.com/user-attachments/assets/0e173f8c-2172-4610-9afc-7eee1d6ae6c2)

Modification des droits si besoin

![Modification des droits si besoin](https://github.com/user-attachments/assets/bc50983d-9ee7-4c33-bf98-ca24c1154151)



Q.1.1.4 

Modification du groupe 

![Modification du groupe](https://github.com/user-attachments/assets/5dd73ddf-aa42-44d7-bdec-7498018006d6)


Partie 2 - Restriction utilisateurs

Q.1.2.1 

Restriction horaire utilisateur
![Capture d’écran 2025-03-07 103857](https://github.com/user-attachments/assets/598e9daa-98a5-4738-9f43-2ae69598ac1d)
![Modif des horaires](https://github.com/user-attachments/assets/7f04d84a-6e0b-4479-b1ec-5825c1bbe7e7)
![Recherche de l'usilisateur](https://github.com/user-attachments/assets/adbc3398-b039-448f-bd1b-1cc02d069be3)



Q.1.2.2 

Restriction ordinateur

![Restriction ordinateur](https://github.com/user-attachments/assets/e2ff69e7-11f7-442a-9c84-58e5fdb400da)


Q.1.2.3 

Durcissement mot de passe

![Durcissement de la stragégie de mot de passe](https://github.com/user-attachments/assets/3fdc8a4c-3e18-4e1f-8609-d2a6325affdd)
![stratégie de mot de passe](https://github.com/user-attachments/assets/db637248-ee30-473c-83c4-f30985c94051)


Partie 3 - Lecteurs réseaux


Q.1.3.1 

Mappage lecteurs

![Drive mount](https://github.com/user-attachments/assets/618ebef7-cdd2-491f-bcbd-1fe72a659f50)

![Lecteur E](https://github.com/user-attachments/assets/307f9e19-bcd5-4882-93c1-3eed98ae605e)

![Lecteurs mappés](https://github.com/user-attachments/assets/ea6e6b19-fb1f-4857-9a8c-c08b42ab25c4)

![Lien de la GPO](https://github.com/user-attachments/assets/784987fa-2ed1-4575-98fc-cbda95610240)

![Mappage](https://github.com/user-attachments/assets/9f5d728b-0b5e-4082-b204-d024c87632bd)

Exercice 2 - VM Linux

Partie 1 - Gestion des utilisateurs

Q.2.1.1: Se connecter directement en root sur la machine et utiliser la commande useradd -m mon_nom, si on est pas en root, utiliser la commande sudo préalablement installée.
Q.2.1.2: Définir un mot de passe fort a l'aire de la commande: passwd mon_nom.
Limiter le compte à son unique champ d'utilisation.
Etablir des droits d'accès minimaux. S'assurer que l'utilisateurs créé n'est pas dans les sudoers.

Partie 2 - Configuration de SSH

Q.2.2.1: Modifier le fichier /etc/ssh/sshd_config et écrire no à la ligne PermitRootLogin.
Redémarrer le SSH avec la commande: systemctl restart sshd
Q.2.2.2 Dans même fichier de configuration sshd_config, ajouter la ligne AllowUsers mon_nom, puis redémarrer le SSH avec systemctl restart sshd
Q.2.2.3 Il faut créer une clef publique SSH avec ssh-keyen puis il faut retourner dans le fichier de configuration sshd_config pour désactiver l'authentification par mot de passe avec la ligne PassworkAuthentification no
Redémarrer le SSH avec systemctl restart sshd

Partie 3 - Analyse du stockage

Q.2.3.1: À partir de la sortie de lsblk, nous voyons les points de montage suivants :

    /boot sur md0p1 (probablement en ext4 ou xfs).
    / (racine) sur cp3--vg-root (LVM, probablement formaté en ext4 ou xfs).
    Partition SWAP sur cp3--vg-swap_1. 
Q.2.3.2:  RAID 1 (mirroring) : md0 est un volume RAID 1 avec sda1.
LVM (Logical Volume Manager) : utilisé pour la partition principale (/) et la SWAP.
Partition standard pour /boot, séparée de LVM.

Q.2.3.3 et Q.2.3.4

![2 3 4](https://github.com/user-attachments/assets/db3426b4-4b19-4065-9c54-1f26719ed53d)


Q.2.3.5 

![2 3 5](https://github.com/user-attachments/assets/84b98722-354b-417f-ac70-1d87248bf24b)

Partie 4 - Sauvegardes

Q.2.4.1: Director = Gestion des tâches de sauvegarde et restauration.
Storage Daemon = Responsable du stockage des sauvegardes.
File Daemon = Agent de sauvegarde sur les machines à protéger. 

Partie 5 - Filtrage et analyse réseau

Q.2.5.1 

![2 5 1](https://github.com/user-attachments/assets/a638aa0f-a8ab-4a46-ad61-784a19a981e0)

Q.2.5.2

![2 5 2](https://github.com/user-attachments/assets/e16eac00-15a8-4a55-bf38-4b5abff6cd88)

Q.2.5.3: ct state invalid drop=tous les paquets ayant un état de connexion considéré comme "invalid" seront bloqués.

Q.2.5.4 

![2 5 4](https://github.com/user-attachments/assets/623152c9-c702-4659-8eb1-9be86c80f0bf)

Partie 6 - Analyse de logs

Q.2.6.1 

![2 6 1](https://github.com/user-attachments/assets/51fb9115-fc97-4d4b-8fd5-d46ea55dcb32)





ok : /24
nr : 
faux : 
