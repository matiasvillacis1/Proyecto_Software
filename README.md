# Proyecto_Software

# Sistema de Gestión de Turnos para Centros Médicos

![Logo o imagen representativa del proyecto](docs/img/Arquitectura.png) *(Reemplaza con una imagen si tienes)*

## Integrantes
- Matías Villacís
- Michael Palacios
- Pablo Solís
- Ricardo López

---

## Problema
Muchos centros médicos pequeños y medianos manejan el agendamiento de citas de forma manual o por teléfono, lo que provoca:
- Largas filas y tiempos de espera.
- Confusiones en el orden de atención.
- Mala experiencia para pacientes.
- Ineficiencia administrativa.

## Objetivo
Desarrollar una **aplicación web** que permita:
- Agendar turnos en línea.
- Gestionar estados de atención (*esperando, en atención, atendido, cancelado*).
- Generar reportes de productividad.

---

## Diagramas del Sistema

### 1. Diagrama de Procesos
![Diagrama de Procesos](docs/diagramas/Diagrama_de_Proceso.png)  
*Flujo: Usuario → Sistema de generación de turnos → Supervisor.*

### 2. Arquitectura del Sistema
![Arquitectura](docs/diagramas/Arquitectura.png)  
*Arquitectura en capas y componentes internos.*

### 3. Diagramas UML
#### Diagrama de Casos de Uso
![Casos de Uso](docs/diagramas/Diagrama_Caso_de_Uso.png)  

| **Caso de Uso**       | **Descripción**                                                                 |
|------------------------|---------------------------------------------------------------------------------|
| **CU-01 Registrar Turno** | Paciente selecciona servicio y fecha/hora. Sistema valida disponibilidad.       |
| **CU-02 Validar Estado**  | Sistema verifica estado del turno para atender/cancelar.                        |
| **CU-03 Actualizar Estado** | Médico cambia estado del turno (ej: "Atendido").                               |
| **CU-04 Atender Turno**    | Médico gestiona la consulta y genera registro.                                  |
| **CU-05 Generar Reporte**  | Supervisor obtiene reporte post-atencion.                                      |

### 4. Diagrama de Clases
![Diagrama de Clases](docs/diagramas/Diagrama_de_Clase.png)  
*Clases principales: `Usuario`, `Turno`, `Médico`, `Reporte`.*

### 5. Diagrama de Secuencia
![Diagrama de Secuencia](docs/diagramas/Diagrama_Secuencia_Corregido.drawio.png)  
*Interacción entre Usuario, Aplicación y Base de Datos.*

### 6. Diagrama de Componentes
![Diagrama de Componentes](docs/diagramas/Diagrama_Componentes.drawio.png)  
*Módulos: App Web, Gestión de Turnos, Base de Datos.*

### 7. Diagrama de Despliegue
![Diagrama de Despliegue](docs/diagramas/Diagrama_de_Despliegue.drawio.png)  
*Nodos: Cliente, Servidor, Base de Datos.*

### 8. Diagrama de Estados
![Diagrama de Estados](docs/diagramas/Diagrama_Estado.drawio.png)  
*Estados de un turno: `Generado` → `En atención` → `Atendido`/`Cancelado`.*

### 9. Diagrama de Actividades
![Diagrama de Actividades](docs/diagramas/Diagrama_Actividades.drawio.png)  
*Flujo completo del ciclo de vida del turno.*
