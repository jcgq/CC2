# Información sobre la práctica 1
## Nombre del alumno y grupo de prácticas
Juan Carlos González Quesada y Grupo 1 (19:00-20:30)

## Perfil de GitHub asociado
@jcgq
## Descripción de la práctica y problema a resolver
Para el desarrollo de la práctica teníamos que unir varios servicios que se interconectaran entre ellos, en donde utilizaremos:
- Grafana: nos permitirá la visualización, evoluciñon y formato de datos métricos.
- Prometheus: que lo utilizaremos para registrar las unidades métricas y permite la supervisión y alerta de eventos.
- Node-Exporter: es un nodo de Prometheus para métricas a nivel de servidor y de sistema operativo con colectores de métricas configurables. Será de donde obtangamos las métricas que vamos a visualizar.
¿Qué utilizaremos para la distribución de las cragas? Un balanceador de cargas:
- HAProxy: que proporciona un equilibrador de cargas de alta disponibilidad que distribuye solicitudes entre varios servidores.

## Servicios desplegados y su configuración. (Incluye todos los detalles necesarios)
- Grafana: es el servicio que más requisitos necesita.
    - Será necesario crear su carpeta grafana, donde se alojará la carpeta provisioning y dentro de ella dos carpetas:
        - Dashboard: donde tendremos el panel que queremos automatizar para la visualización de las métricas (De esta forma evitaremos que se tenga que crear cada vez que se levanten los servicios) Aquí tenemos el panel en formato [json](https://github.com/jcgq/CC2/blob/main/P1/grafana/provisioning/dashboards/node-exporter-full_rev26.json), que se puede descargar desde [aqui](https://grafana.com/grafana/dashboards/) y [un archivo de configuración](https://github.com/jcgq/CC2/blob/main/P1/grafana/provisioning/dashboards/dashboard.yml), en donde se indicará la ruta de donde se obtiene el panel.
        - Datasources: será la carpeta donde se indique en un [archivo de configuracion](https://github.com/jcgq/CC2/blob/main/P1/grafana/provisioning/datasources/datasource.yml), de que ruta se obtienen los datos para la visualización. Este archivo lo podemos encontrar (Sin nuestras modificaciones para el proyecto), en la [web oficial de Grafana](https://grafana.com/docs/grafana/latest/administration/provisioning/#example-data-source-config-file)
- - 
## Conclusiones

## Referencias bibliográficas y recursos utilizados

## Práctica y archivos

## Material auxiliar (imágenes para la documentación, ficheros de configuración, etc.)