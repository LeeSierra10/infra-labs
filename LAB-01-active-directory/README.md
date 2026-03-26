# LAB 01 – Active Directory Deployment

## Objetivo
Implementar un Domain Controller utilizando Windows Server 2022 y configurar un dominio Active Directory para la gestión centralizada de usuarios.

---

## Tecnologías utilizadas

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- VirtualBox
- Windows Client (opcional para pruebas)

---

## Arquitectura del laboratorio

Infraestructura implementada:

Domain Controller  
Nombre del servidor: **DC-LAB01**

Dominio:

lab.local

Entorno virtualizado en **VirtualBox**

---

## Paso 1 – Crear la máquina virtual

Configuración utilizada:

Nombre de la VM:

DC-LAB01

Recursos asignados:

RAM: 4 GB  
CPU: 2  
Disco: 60 GB

Sistema operativo instalado:

Windows Server 2022 Standard (Desktop Experience)

---

## Paso 2 – Cambiar nombre del servidor

Abrir:

Server Manager → Local Server

Cambiar:

Computer Name → DC-LAB01

Reiniciar el servidor.

---

## Paso 3 – Instalar Active Directory Domain Services

Abrir:

Server Manager

Seleccionar:

Add Roles and Features

Instalar el rol:

Active Directory Domain Services

---

## Paso 4 – Promover el servidor a Domain Controller

Seleccionar:

Promote this server to a domain controller

Elegir:

Add a new forest

Dominio configurado:

lab.local

Definir contraseña para **Directory Services Restore Mode (DSRM)**.

Finalizar instalación y reiniciar el servidor.

---

## Paso 5 – Verificar dominio

Abrir:

Active Directory Users and Computers

Confirmar que el dominio **lab.local** está activo.

---

## Paso 6 – Crear Organizational Units

Se crearon las siguientes OU:

IT  
Usuarios

Esto permite organizar los recursos dentro del dominio.

---

## Paso 7 – Crear usuarios de prueba

Usuarios creados:

usuario1  
usuario2  
admin.lab

Estos usuarios permiten validar la gestión de identidades dentro del dominio.

---

## Evidencia

### Instalación de Windows Server

![Instalación Windows Server](screenshots/server-install.png)

---

### Active Directory instalado

![Active Directory](screenshots/ad-installed.png)

---

### Dominio creado

![Dominio](screenshots/domain-created.png)

---

### OU creadas

![OU](screenshots/ou-created.png)

---

### Usuarios creados

![Usuarios](screenshots/users-created.png)

---

## Resultados

Se implementó correctamente un entorno de dominio Active Directory que permite:

- Gestión centralizada de usuarios
- Organización mediante OU
- Administración de identidades
- Base para implementar políticas de seguridad (Group Policy)

---

## Conclusión

Este laboratorio permite comprender los fundamentos de la administración de identidades en entornos corporativos utilizando Active Directory, tecnología ampliamente utilizada en infraestructuras empresariales.
