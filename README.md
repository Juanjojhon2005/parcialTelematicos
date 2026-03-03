vagrant@cliente:~$ curl -I http://parcial.juanjosesantacruz.com HTTP/1.1 200 OK Date: Mon, 02 Mar 2026 23:16:48 GMT Server: Apache/2.4.52 (Ubuntu) Last-Modified: Mon, 02 Mar 2026 23:06:01 GMT ETag: "13e-64c12a170720e" Accept-Ranges: bytes Content-Length: 318 Vary: Accept-Encoding Content-Type: text/html vagrant@cliente:~$ curl -H "Accept-Encoding: gzip" -I http://parcial.juanjosesantacruz.com HTTP/1.1 200 OK Date: Mon, 02 Mar 2026 23:16:55 GMT Server: Apache/2.4.52 (Ubuntu) Last-Modified: Mon, 02 Mar 2026 23:06:01 GMT ETag: "13e-64c12a170720e-gzip" Accept-Ranges: bytes Vary: Accept-Encoding Content-Encoding: gzip Content-Length: 235 Content-Type: text/html

 Sin compresión: 318 bytes
Con compresión: 235 bytes
Ahorro(%)=(318-235)/318×100
Ahorro(%)=83/318×100
Ahorro(%)≈26.1%


Prueba	Content-Length (bytes)	Content-Encoding	Observación
Sin compresión	318	No	Archivo enviado sin compresión
Con compresión	235	gzip	Archivo comprimido con mod_deflate
Reducción obtenida	83 bytes	 	26.1% menos tráfico

Al habilitar el módulo mod_deflate en Apache, el tamaño del archivo HTML disminuyó de 318 bytes a 235 bytes, lo que representa una reducción del 26.1% en el tráfico transmitido. Esto demuestra que la compresión gzip optimiza el uso del ancho de banda y mejora el rendimiento en la entrega de contenido textual. No obstante, la compresión implica un ligero incremento en el uso de CPU del servidor al procesar los datos antes de enviarlos.
