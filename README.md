# Realice el seguimiento de las donaciones con Blockchain
Cree, configure e interactúe con IBM Blockchain Platform a través de Hyperledger Composer Playground y del servidor REST de Hyperledger Composer

## Summary

Imagine lo que podría ocurrir si cada ciudadano tuviera la confianza de que se están honrando los compromisos filantrópicos para ayudar a las problemáticas sociales y que los recursos estuviesen llegando a las personas que tienen mas necesidades. Que se puedan asegurar de que todos los dólares que donan estén causando un impacto real. ¿Un sistema más transparente no motivaría a las personas para que fuesen más propensas a defender causas que merecen la pena? O, aun mejor ¿que las inspirarse a donar más?

Blockchain puede proporcionar la transparencia y la responsabilidad que exigen los ciudadanos. Complete este Code Pattern para utilizar IBM Blockchain Platform para construir una red de tres miembros en la que los compromisos específicos para una causa y las transferencias de fondos se realicen por el gobierno, se registren por las organizaciones de ayuda y sean validas por Global Citizen

## Requisitos Previos
 
1. Cuenta gratuita en [IBM Cloud](https://www.ibm.com/cloud/)

2. [NPM](https://www.npmjs.com/) y Node instalado (node version 8.10.0)

3. Si ha usado otras versiones de composer-cli, o ha implementado un archivo .bna antes, ejecute estos comandos
```
npm uninstall -g composer-cli
npm uninstall -g composer-rest-server
rm -rf ~/.composer
rm *.card
rm -rf credentials/
```

4. Instalar composer-cli
```bash
npm install -g composer-cli@0.20
```
## Flujo
![](images/flow.png)

1. Crear y enviar una propuesta de compromiso a la organización Global Citizen para su revisión

2. Enviar la propuesta de compromiso a la organización gubernamental por los fondos

3. Actualizar la propuesta de compromiso con las especificaciones de financiación

4. Transferir fondos de acuerdo a la propuesta de compromiso.

## Steps

1. [Generar el archivo de red de negocios (BNA)](#1)

2. [Crear Servicio Blockchain](#2)

3. [Obtener el secreto](#3)

4. [Use el secreto para obtener certificados de la autoridad de certificación](#4)

5. [Use el archivo admin-pub.pem para agregar certificados a los miembros](#5)

6. [Crear tarjeta de red de negocios de administración](#6)

7. [Instalar runtime e iniciar la red.](#7)

8. [Crear una nueva tarjeta de red de negocios.](#8)

9. [Interactuar con la red de negocios](#9)


