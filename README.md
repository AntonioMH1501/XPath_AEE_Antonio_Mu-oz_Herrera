LDM-Tarea-XPath-Antonio_Mu-oz_Herrera

Este repositorio contiene las misiones de auditoría de infraestructura para la red de TechNova Cloud. El objetivo es extraer datos críticos de los centros de datos de Madrid y París mediante expresiones XPath precisas. Misión 1: Mapeo de Seguridad (Francia) Objetivo: Sacar los puertos de los servicios que corren solo en París para auditar el firewall. Query: //centro_datos[@ubicacion='Paris']//servicio/@puerto Resultado: Puertos 8888, 22 y 873.

Misión 2: Auditoría de Mantenimiento Objetivo: Ver la versión del SO del servidor de base de datos (srv-db-01) para planificar updates. Query: //servidor[@id='srv-db-01']/software/so/@version Resultado: Versión 15 (Debian).

Misión 3: Inventario de Alta Capacidad Objetivo: Listar discos con capacidad igual o mayor a 8 TB (HDD o NVMe). Query: //disco[@capacidad_tb >= 8] Resultado: Nodos de 8TB y 50TB.

Misión 4: Eficiencia Energética Objetivo: Localizar el primer servidor que aparezca en el inventario con estado "apagado". Query: (//servidor[@estado='apagado'])[1] Resultado: Nodo completo de srv-backup-01.

Misión 5: Desafío Auditor Senior Objetivo: Identificar la arquitectura de CPU de las máquinas que tienen GPU (IA). Query: //servidor[hardware/gpu]/hardware/cpu/@arquitectura Resultado: x86_64.

XML: Estructura del catálogo. XPath: Navegación y filtrado.
