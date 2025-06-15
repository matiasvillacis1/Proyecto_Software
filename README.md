# Proyecto_Software

Sistema de Gestión de Turnos para Centros Médicos
----------------------------------------------------------------------------------------------------------------------------------------------
Integrates:
-	Matías Villacís
-	Michael Palacios
-	Pablo Solís
-	Ricardo López
Problema:
Muchos centros médicos pequeños y medianos todavía manejan el agendamiento de citas y turnos de forma manual o por teléfono, lo cual provoca:
•	Largas filas y tiempos de espera.
•	Confusiones en el orden de atención.
•	Mala experiencia para los pacientes.
•	Ineficiencia administrativa.
Objetivo:
Desarrollar una aplicación web que permita a los pacientes agendar turnos en línea, y que al mismo tiempo le dé al personal médico una herramienta sencilla para gestionar los turnos, estados de atención (esperando, en atención, atendido, cancelado), y reportes de productividad.
1. Diagrama de Procesos 
Diagrama de Procesos: Usuario, Sistema de generación de turnos y Supervisor. Se aprecia el flujo desde la selección del requerimiento hasta el reporte final.
2. Arquitectura del Sistema 
Se muestra la arquitectura en capas y los componentes internos del sistema.
3.  Diagramas UML - Diagrama de Casos de Uso
   •	Documentación:
Caso de Uso	Registrar Turno	CU-01
Actores	Paciente -> Sistema
Tipo	Primario | Esencial
Referencias	CU-02	Validar Estado del Turno
PreCondición	El paciente debe estar registrado en el sistema.
PostCondición	El turno queda registrado en la base de datos con un estado inicial de “Pendiente” o “En espera”.
Autor	Matías Villacís	Fecha	21/05/2025
	Versión	2.0

Propósito
Permitir que el paciente registre un turno en línea mediante la aplicación.

Resumen
El paciente accede al sistema, selecciona el tipo de servicio y la fecha/hora deseada. El sistema valida disponibilidad y registra el turno.


Caso de Uso	Validar Estado del Turno	CU-02
Actores	Sistema -> Médico
Tipo	Secundario | Real
Referencias	CU-03	Actualizar Estado del Turno
PreCondición	El turno debe estar registrado.
PostCondición	El estado del turno es verificado y actualizado si corresponde.
Autor	Michael Palacios	Fecha	22/05/2025	Versión	2.0

Propósito
Revisar el estado actual del turno para permitir acciones como atender o cancelar.

Resumen
El sistema consulta el estado del turno y determina si se puede proceder a atenderlo o actualizarlo. Puede activar el CU-03.

Caso de Uso	Actualizar Estado del Turno	CU-03
Actores	Médico -> Sistema
Tipo	Secundario | Esencial
Referencias	CU-02	Validar Estado del Turno
PreCondición	El turno debe estar en estado “En espera” o “Atendiendo”.
PostCondición	El estado del turno cambia (por ejemplo, a “Atendido” o “Cancelado”).
Autor	Ricardo López	Fecha	24/05/2025	Versión	2.0

Propósito
Permitir al médico actualizar el estado del turno según la atención brindada.

Resumen
El médico accede al turno y selecciona el nuevo estado. El sistema registra el cambio en la base de datos.

Caso de Uso	Atender Turno	CU-04
Actores	Médico
Tipo	Primario | Real
Referencias	CU-03 	Actualizar Estado del Turno
PreCondición	El turno debe estar validado y en estado “En espera”.
PostCondición	El turno se marca como “Atendido” y se genera un registro de atención.
Autor	Pablo Solís	Fecha	23/05/2025	Versión	2.0

Propósito
Gestionar el proceso de atención médica al paciente.

Resumen
El médico inicia la atención desde su panel, realiza la consulta y finaliza la atención, actualizando el estado y vinculando un reporte. 

Caso de Uso	Generar reporte	CU-05
Actores	Supervisor 
Tipo	Opcional | Real
Referencias	CU-04 	Atender Turno
PreCondición	El turno debe estar marcado como atendido.
PostCondición	Se genera un reporte de atención disponible para consultas futuras.
Autor	Matías Villacís	Fecha	25/05/2025	Versión	2.0

Propósito
Generar un reporte automático de atención médica.

Resumen
Una vez finalizada la atención, el sistema crea un reporte con los datos del turno, diagnóstico e historial del paciente.
4. Diagrama de Clases 
Muestra las clases principales del sistema (Usuario, Ticket, Asesor, Reporte) con atributos, métodos y relaciones entre ellas.
5. Diagrama de Secuencia 
Representa la interacción entre Usuario, Aplicación, Sistema y Asesor desde la solicitud hasta la atención de la consulta.
  •	Actualizar Estado de Consulta
  •	Consultar Estado de Consulta
  •	Atender Consulta
  •	Generar Reporte
6. Diagrama de Componentes 
Ilustra los componentes del sistema, como la aplicación web, la gestión de consultas y el acceso a la base de datos.
7. Diagrama de Despliegue
Muestra la disposición física del sistema en nodos: cliente, servidor de aplicaciones y base de datos.
8. Diagrama de Estados 
Describe los estados posibles de un turno: Generado, En atención, Solucionado, Cerrado.
9. Diagrama de Actividades 
Representa el flujo general del ciclo de vida del ticket en base a decisiones, actividades y condiciones.
