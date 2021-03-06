---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-30"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introducción a la tecnología SSL

La capa de sockets seguros (SSL) es una tecnología que cifra el tráfico entre la aplicación del cliente y la del servidor. El cifrado se logra mediante el uso de un sistema de clave pública/clave privada mediante un certificado SSL.

El certificado SSL contiene la clave pública del servidor, fechas en las cuales es válido el certificado, un nombre de host para el cual el certificado es válido y una firma de la autoridad de certificación que lo haya emitido.

## Terminología SSL

Las certificaciones SSL tienen una terminología única. Al trabajar con certificados SSL, puede encontrarse los términos siguientes.

**Tamaño de los bits:** las claves de cifrado se miden por su tamaño en bits. Por ejemplo 512 bits, 1024 bits, 2048 bits. Generalmente, una clave larga será más segura pero más lenta de utilizar. En este momento, el tamaño mínimo de las claves utilizadas en certificados SSL es de 1024 bits, aunque los certificados de validación ampliada requieren 2048 bits.

**Cadena de certificados:** normalmente los certificados SSL no se utilizan solos. En la mayoría de las implementaciones, trabajará con una cadena de certificados. Por ejemplo:

  Root > intermediate1 > server cert.

  \> Intermediate2 > server2 cert

En este ejemplo, el certificado de servidor lo firma el certificado intermedio, que, a su turno, lo firma el certificado raíz. Encadenar de este modo, puede hacer que la SSL sea más segura, ya que de esta forma el certificado raíz no se utiliza (ni se expone a riesgos) tan a menudo. Si intermediate1 estuviera en peligro, el certificado de servidor podría estar en peligro perlo del certificado de server2 estaría bien porque forman parte de cadenas diferentes.

**Solicitud de firma de certificado:** el CSR es un documento que genera en el servidor que contiene información que la autoridad de certificación utiliza para crear el certificado.

**Nombre común:** el nombre común (CN) es el nombre de host para el cual el certificado es válido (por ejemplo, www.domain.com).  

*Nota:* www.domain.com, smtp.domain.com y mail.domain.com son tres nombres de host completamente diferentes y el mismo certificado SSL no es válido para los tres (excepto si utiliza un certificado comodín, pero en este momento {{site.data.keyword.cloud}} no lo ofrece).

**Clave privada/pública:** SSL utiliza una técnica denominada criptografía de clave pública. En esta forma de criptografía, tiene dos claves: la pública y la privada. La clave pública se distribuye por todas partes. Nadie ve su clave privada. Los usuarios que deseen comunicarse de forma segura con usted, cifran sus comunicaciones con su clave pública. La criptografía de clave pública se basa en la aserción de que los bits cifrados con una determinada clave pública solo pueden ser descifrados con la correspondiente clave privada y viceversa.

**Certificado raíz:** los certificados raíz SSL son certificados que se han autofirmado y que han presentado sus respectivas Autoridades de certificación como parte superior de su cadena. Encontrará certificados raíz de Autoridades de certificación ya instaladas en el almacén de certificados de su navegador web. Esto permite que su navegador confíe en dichos certificados y forma los inicios de las cadenas de confianza que llevan al certificado que instala en su servidor.

**Firma:** la autoridad de certificación coloca una firma digital en los certificados SSL. Esta firma, una vez trazada hasta un certificado raíz de confianza, confirma la autenticidad del certificado.

## SSL en la infraestructura de IBM Cloud

{{site.data.keyword.BluSoftlayer_full}} revende tres tipos de certificados de SSL: Validación de dominio, Validación de organización, Validación ampliada. 

Los certificados de Validación de dominio (DV) son baratos y están disponibles rápidamente. La validación que realiza la Autoridad de certificación se limita a enviar un correo electrónico a una dirección de correo electrónico concreta en el dominio en cuestión y a obtener una respuesta positiva. Los certificados de Validación de organización (OV) y la Validación ampliada (EV) tardan dos días (a veces más), cuestan más y suponen más comprobaciones por parte de la Autoridad de certificación. Los certificados de EV se codifican de manera que los navegadores los reconocen como EV y normalmente muestran una barra verde como parte de la barra de direcciones. 

Los certificados SSL, igual que otros servicios de {{site.data.keyword.cloud_notm}}, se pueden gestionar a través de {{site.data.keyword.slportal}}.  Vaya al menú **Seguridad** y seleccione la opción **Certificados SSL** en la parte inferior para solicitar y gestionar certificados.  

**Nota:** los certificados SSL solicitados mediante {{site.data.keyword.cloud_notm}} no tienen que utilizarse en un servidor {{site.data.keyword.BluSoftlayer_notm}}. Además, los certificados solicitados en otro lugar se pueden utilizar en los servidores alojados aquí.

**Conclusión**

Los certificados SSL mejoran la seguridad de las transacciones que se realizan y proporcionan a los usuarios una sensación de seguridad. Además de los certificados SSL, la seguridad Daemon, la seguridad física, las prácticas de codificación y la gestión de certificados se combinan para formar el perfil de seguridad general de la solución.
