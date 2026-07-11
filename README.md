## CI/CD

Este proyecto implementa un flujo de Integración y Despliegue Continuo (CI/CD) utilizando GitHub Actions para automatizar el proceso de construcción, validación y despliegue de la aplicación.

### Flujo de trabajo

1. Cada cambio enviado a las ramas de desarrollo activa automáticamente el pipeline.
2. Se instala el entorno de trabajo y las dependencias del frontend y backend.
3. Se ejecutan pruebas automatizadas para verificar el correcto funcionamiento de la aplicación.
4. Si las pruebas son exitosas, la aplicación se despliega automáticamente al entorno de **Development (DEV)** alojado en una máquina virtual Proxmox.
5. Los despliegues a **Production (PROD)** se realizan mediante un flujo controlado para garantizar la estabilidad del sistema.

### Tecnologías utilizadas

- GitHub Actions
- Node.js
- Laravel
- Composer
- Jest
- PHPUnit
- SSH
- Proxmox VE
- Git

### Arquitectura del pipeline

Push a develop / pablo-dev
            │
            ▼
 Build & Quality Checks
            │
      Frontend Tests
            │
      Backend Tests
            │
            ▼
 Deploy automático a DEV
            │
            ▼
 Validación del entorno
            │
            ▼
 Deploy controlado a Production
