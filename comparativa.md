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