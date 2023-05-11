# Subnetting
Abbiamo fatto subnetting delle due reti facendole comunicare tra di loro (abbiamo impostato la subnet mask a 255.255.255.128 per far si che le due reti differenti comunichino tra di loro).

![tabellasubnetting](https://github.com/1bianco9/Subnetting/assets/116873906/d3db5406-41ff-46f9-8253-e049573671ef)

La nostra rete è una /24 e come possiamo vedere dalla tabella la nostra rete può contenere 256 ip (tranne il primo e lultimo per network id e broadcast ip).
Quindi per dividere la rete in 2 parti dobbiamo trasformarle in due reti /25.
Come possiamo vedere dalla tabella le due reti avranno 128 ip ognuna
(escludendo come sempre network id e broadcast ip e vale per tutte e due le reti) 
Quindi dobbiamo impostare gli ip nei dispositivi in modo tale che siano divisi esattamente a metà
Gli indirizzi della prima rete dovranno andare da 192.168.0.0 a 192.168.0.127 
e la seconda da 192.168.0.128 a 192.168.0.255
Ora che abbiamo gli ip ci occorono le subnet mask:
la subnet mask di una rete /24 in binario è: 11111111.11111111.11111111.00000000
Per poterla dividere in due occorre impostare il bit 0 piu a sinitra a 1,
cosi che diventerà: 11111111.11111111.11111111.10000000
Ora basta solo calcolare da binario a decimale ceh equivale a 2^7 e quindi a 128
quindi la nostra subnet sarà: 255.255.255.128
