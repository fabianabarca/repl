## Requerimientos:
Crear un sistema parecido a REPL.it que permita a usuarios del TCU Tropicalización de la Tecnología correr el lenguaje python y la biblioteca de DJANGO (con la opción de descargar e instalar otras bibliotecas auxiliares en el REPL que permitan el desarrollo de los proyectos del TCU).

## Análisis:
Un 'REPL' consiste en una máquina virtual generada dinámicamente que viene con un shell de linux y algunos lenguajes (C, C++, python, etc) preinstalados. El lenguaje para desarrollo en dicha máquina virtual es seleccionado durante el proceso de generación, para evitar instalar lenguajes que no serán utilizados y aprovechar el espacio. Se desconoce si en el modelo de REPL son varias máquinas virtuales por servidor, aunque lo más probable es que un servidor sirva para correr N máquinas hasta que llegue a su límite de utilización de recursos, donde se despliega otro servidor para correr más máquinas, y así sucesivamente.

### Opciones propuestas (a consultar viabilidad de cada una con el profesor):
1) Sistema de N servidores locales: la cantidad de máquinas virtuales por servidor depende del hardware de cada uno. 
Servicios para construir el sistema buscados:

    -Bitnami ofrece un servicio de máquinas virtuales que contienen la biblioteca de Django preinstalada, ya sea para correrlas en un servidor propio o en un servidor dado por la empresa: https://bitnami.com/stack/django/virtual-machine

    -Mozilla provee una documentación para configurar un ambiente de desarrollo para Django: https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/development_environment

    -Vagrant (https://www.vagrantup.com/) es un servicio gratis que permite la creación de un ambiente de desarrollo en django, en la siguiente documentacion se explica paso por paso como se construye: https://linuxtut.com/en/6fd9991c6fcba00c4c71/

    -Sunscrapers explica en este artículo como montar el ambiente de desarrollo de django ya sea en Linux o en Windows: https://sunscrapers.com/blog/setting-up-django-environment/




2) Sistema de N servidores pago usando un servicio externo: 
Generalmente se le pueden dar los requerimientos de procesamiento al servicio para que las máquinas virtuales tengan una cantidad apropiada de recursos para correr las herramientas de desarrollo (VSCode, git) y las bibliotecas.
Se buscaron opciones para las máquinas virtuales:

    -Bitnami ofrece una opción paga para correr las máquinas virtuales en la nube de la empresa: https://bitnami.com/stack/django/cloud

    -DigitalOcean ofrece una opción paga para corre N máquinas virtuales, ofrece diferentes planes de pago dependiendo de la cantidad de CPUs y memoria solicitadas, además permite escoger el sistema operativo que se desea tener en las máquinas: https://try.digitalocean.com/virtualmachines/

