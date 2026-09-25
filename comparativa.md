# Comparativa y Selección de ERP/CRM

## 1. Datos
- **Propietario:** JorgeMorenoRivero
- **Empresa:** Caso 11 - Constructora "Edifica Levante"
- **Palabra del día:** - Compañero

## 2. Licencias y modelos
### Diferencias entre software libre (FSF), código abierto (OSI) y propietario
Para entender bien qué nos conviene en Edifica Levante, lo primero que he hecho ha sido revisar las diferencias clave entre cada tipo de software:

- **Software Libre (FSF):** Se enfoca ante todo en dar libertad al usuario. Nos garantiza 4 puntos clave: usar el programa para lo que queramos, inspeccionar su código, modificarlo si nos hace falta y distribuir copias libremente.
- **Código Abierto (OSI):** Es un enfoque más pragmático. No se mete tanto en temas filosóficos, sino en las ventajas técnicas de tener un código abierto para que la comunidad colabore y encuentre fallos rápido.
- **Software Propietario:** Es el modelo cerrado de toda la vida. No podemos ver ni tocar el código interno. Al pagar, solo obtenemos un derecho de uso bajo las reglas y limitaciones que imponga el fabricante.

### Por qué "libre" no significa "gratuito"
Un error común es pensar que software libre implica coste cero. Libre se refiere a la libertad de adaptar el código, no a que no nos vaya a costar ni un euro. Aunque nos ahorremos las licencias de entrada, en una empresa real como la nuestra hay que pagar la infraestructura (servidores), la configuración inicial, formar al personal de obra y contar con soporte técnico si hay algún problema grave.

### Implicaciones de la edición Community frente a Enterpris
- **Community:** Es la versión que mantiene la comunidad, gratuita e instalable por nuestra cuenta. El código es abierto pero no tenemos soporte directo del fabricante y algunas funciones avanzadas no vienen incluidas.
- **Enterprise:** Es la versión comercial. Se paga una cuota periódica pero a cambio incluye soporte técnico directo, actualizaciones garantizadas, alojamiento en la nube y módulos más complejos listos para usar.

## 3. Fichas técnicas

Buscando solucionar el descontrol con los gremios y las obras en Edifica Levante, he analizado estas 4 opciones:

### Odoo Community (ERP Libre)
Es un ERP bastante completo que funciona por módulos. Esta edición va con licencia **GNU LGPLv3**. Su servidor corre sobre **Python** y necesita sí o sí una base de datos **PostgreSQL**. Se puede montar en local o en un VPS con Linux (por ejemplo Ubuntu con unos 4 GB de RAM mínimo). Para nuestro caso con la versión 18.0, veo imprescindibles los módulos de Proyectos, Compras, Facturación y Partes de horas para los operarios.
- *Fuente oficial:* https://www.odoo.com/es_ES (Consulta: 24/09/2026)

### Microsoft Dynamics 365 (ERP Propietario)
La apuesta de Microsoft para empresas grandes. Es 100% en la nube (SaaS) y con licencia propietaria de pago por usuario. Su núcleo está desarrollado en **C# y AL** dentro del ecosistema .NET, tirando de **SQL Server / Azure SQL Database**. Al ir por web solo hace falta un navegador decente y buena conexión. Su versión actual (Release 2026 Wave 2) viene muy potente en la parte de Project Operations y finanzas.
- *Fuente oficial:* https://dynamics.microsoft.com/es-es/ (Consulta: 24/09/2026)

### SuiteCRM (CRM Libre)
Un CRM bastante conocido en el mundo del código abierto, bajo licencia **GNU AGPLv3**. Está hecho en **PHP (8.2+)** y se puede conectar a **MySQL, MariaDB o PostgreSQL**. Lo podemos desplegar en un servidor Apache o Nginx propio. En su versión 8.9 nos serviría para llevar el control de Oportunidades, contactos de subcontratas, calendarios del equipo y tareas de proyectos.
- *Fuente oficial:* https://suitecrm.com/ (Consulta: 24/09/2026)

### Salesforce Sales Cloud (CRM Propietario)
Seguramente el CRM en la nube más utilizado del mercado. Es un servicio SaaS con licencia comercial por usuario. Todo su motor corre sobre su propio lenguaje (**Apex**) y una base de datos interna gestionada por ellos. En la versión Summer '26 destaca por sus funciones de Field Service (muy útil si hay gente desplazada en obras), gestión de clientes y cuadros de mando.
- *Fuente oficial:* https://www.salesforce.com/es/ (Consulta: 24/09/2026)

## 4. Fe de erratas

Revisando el material del tema sobre los sistemas CRM, me he fijado en un par de apuntes sobre SuiteCRM que no terminan de cuadrar con el estado actual del programa:

Por un lado, la presentación dice que SuiteCRM fue "Desarrollado por la comunidad SugarCRM". Si investigamos un poco el origen de la herramienta, se ve que en realidad nació como un fork independiente impulsado por la empresa SalesAgility por 2013, justo cuando los creadores de SugarCRM decidieron cerrar el código de sus versiones libres.

Por otro lado, el temario señala que es compatible con "MySQL, MariaDB y SQL Server". Si entramos hoy en día a la matriz de compatibilidad de sus versiones modernas (las de la rama SuiteCRM 8.x en https://docs.suitecrm.com/admin/compatibility-matrix/), se comprueba que el soporte para Microsoft SQL Server se fue retirando a medida que reestructuraron todo el motor sobre Symfony, dejando el soporte oficial enfocado en MariaDB y MySQL sobre entornos Linux.

## 5. Matriz de decisión y recomendación

### Matriz de decisión

| Criterio | Peso | Odoo Community | Microsoft Dynamics 365 | SuiteCRM |
|---|---|---|---|---|
| Coste de licencias | 20% | 5 | 1 | 5 |
| Gestión de proyectos y obras | 20% | 5 | 5 | 3 |
| Flexibilidad y adaptabilidad | 15% | 4 | 3 | 4 |
| Facilidad de implantación | 15% | 3 | 4 | 4 |
| Soporte y comunidad | 15% | 4 | 5 | 3 |
| Escalabilidad y crecimiento futuro | 15% | 4 | 5 | 3 |
| **Total ponderado** | **100%** | **4.25** | **3.75** | **3.70** |

### Justificación de las puntuaciones

El criterio con más peso, junto con gestión de proyectos, es el coste de licencias (20%), porque en una constructora es donde más dinero se puede ir sin darte cuenta. Odoo Community y SuiteCRM puntúan 5 al ser open source y no cobrar por usuario. Dynamics 365 se queda en 1: cobra una cuota mensual por cada persona que usa el sistema, y en Edifica Levante hay jefes de obra, encargados y subcontratas entrando y saliendo constantemente — eso multiplicado por doce meses da un número que no cuadra con el presupuesto que manejan.

En gestión de proyectos y obras Odoo y Dynamics empatan con un 5 porque ambos traen módulos ya hechos para partes de horas y seguimiento de costes por proyecto. SuiteCRM se queda en 3 porque, al final, nació como CRM y no como herramienta de gestión de obra, así que habría que retocarlo bastante para que sirviera igual de bien.

Para flexibilidad le puse un 4 tanto a Odoo como a SuiteCRM (los dos permiten tocar el código si hace falta) y un 3 a Dynamics, que aunque tiene sus opciones de personalización, casi siempre necesitas un desarrollador certificado de Microsoft para ir más allá de lo básico, y eso ya es otro coste que no está en la licencia.

Facilidad de implantación es donde Odoo sale peor parado (3 sobre 5): hay que montar servidor propio y base de datos PostgreSQL, lo cual no es imposible pero sí requiere a alguien con conocimientos técnicos. Dynamics y SuiteCRM llevan un proceso de puesta en marcha algo más guiado, de ahí el 4 en ambos.

Soporte y comunidad: aquí Dynamics gana claramente (5) porque tiene detrás todo el soporte oficial de Microsoft, con SLA y garantías. Odoo se queda en 4 — tiene una comunidad grande y mucha documentación, pero el soporte "de verdad" hay que pagarlo aparte. SuiteCRM tiene un 3 porque su comunidad es bastante más pequeña que la de Odoo.

Por último, en escalabilidad le doy un 5 a Dynamics (pensado para crecer sin límite, aunque el precio también crece), un 4 a Odoo (se pueden ir añadiendo módulos según haga falta) y un 3 a SuiteCRM, que últimamente tiene menos desarrollo activo que las otras dos opciones.

### Riesgos por opción

**Odoo Community.** El ahorro en licencias es real, pero no es gratis del todo: hay que contar con lo que cuesta implantarlo y mantenerlo (servidor, copias de seguridad, alguien que sepa manejarlo). La dependencia del proveedor es baja porque es código abierto, y si algún día quieres cambiar de sistema, migrar no debería ser un drama porque usa PostgreSQL, que es un formato bastante estándar.

**Microsoft Dynamics 365.** El coste total es el más alto de los tres, y encima va subiendo según se añaden usuarios o módulos nuevos. Además te ata bastante al ecosistema de Microsoft, así que salirte de ahí en el futuro no sería sencillo. A cambio, es probablemente la opción más fiable en cuanto a soporte y continuidad.

**SuiteCRM.** Licencia barata, como Odoo, pero el riesgo está en el soporte a largo plazo — su comunidad es más pequeña y eso preocupa si algo falla y necesitas ayuda rápido. Migrar a otro sistema en el futuro es viable al ser open source, aunque tiene menos herramientas para exportar datos que las otras dos opciones.

### Recomendación final

Con todo esto, la opción que mejor encaja para Edifica Levante es **Odoo Community**. El motivo de peso es el ahorro en licencias: con tanta gente rotando por las obras, pagar por usuario al mes como hace Dynamics se dispararía rápido. Además el módulo de proyectos les vendría bien para llevar el control de horas y costes de obra sin pagar de más. El punto flojo es que la implantación exige algo de conocimiento técnico que igual no tienen ahora mismo en la empresa, pero a medio plazo el ahorro en licencias debería compensar ese esfuerzo inicial.