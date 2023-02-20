# jhei-bootcamp

Para el presente desafio, hemos subido una instancia de Jenkins sobre una instancia de EC2, la cual se levanto con la siguiente información: 

AMI: ami-08c40ec9ead489470
Instance type: t3.medium
EBS: 30gb
userdata: https://gist.github.com/roxsross/30c233e68c90ab67a3824378915ce102

Para este ejercicio ejecutamos un pipeline que actualiza nuestra página web ubicada en un bucket de S3 en AWS, esto se ejecuta cada vez que realizamos un cambio en nuestro codigo de github y a través de un webhook avisamos a jenkins para la ejecución de pipeline:

<img width="851" alt="image" src="https://user-images.githubusercontent.com/63665794/219983813-573e04b4-3701-4a14-ae11-e8a7f6f65a17.png">

