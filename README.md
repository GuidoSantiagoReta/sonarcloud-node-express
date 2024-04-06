
# Configuración de SonarCloud en un proyecto Node con Express:

- Este proyecto utiliza SonarCloud para realizar análisis de código estático y mejorar la calidad del código. A continuación, se detallan los pasos para configurar SonarCloud en tu proyecto.

## Requisitos:

- Tener una cuenta en SonarCloud.
- Un token de SonarCloud generado desde la página de seguridad de tu cuenta en SonarCloud.
- Un token de GitHub generado desde la configuración de tu repositorio en GitHub.

## Pasos para configurar SonarCloud:

1. **Crear una organización en SonarCloud**:
   - Ir a [SonarCloud](https://sonarcloud.io/) y crear una nueva organización.

2. **Generar tokens de SonarCloud y GitHub**:
   - En SonarCloud, ir a la página de seguridad y genera un nuevo token. Este token será utilizado para autenticar el acceso a SonarCloud desde GitHub Actions.
   - En GitHub, ir a la configuración de tu repositorio, busca la sección de "Secrets" y crea un nuevo secret con el token de SonarCloud generado.
   - Genera un token de GitHub desde la configuración de tu cuenta en GitHub y añádelo como un nuevo secret en la configuración de tu repositorio en GitHub.

3. **Configurar el pipeline de SonarCloud en GitHub Actions**:
   - Crea un nuevo archivo en tu repositorio en la ruta `.github/workflows/sonarcloud-scan.yml` con el siguiente contenido:


4. **Ejecutar el pipeline**:
   - Una vez configurado el pipeline, cada vez que se haga push a la rama `main`, se ejecutará automáticamente el análisis de SonarCloud.

## Adicionales:

- Asegurate de reemplazar `GH_TOKEN` y `SONAR_TOKEN` en el archivo de configuración del pipeline con los nombres de los secrets que has creado en GitHub.
- Este pipeline está configurado para ejecutarse en la rama `main`. Si tu rama principal tiene un nombre diferente, asegurate de actualizar el archivo de configuración del pipeline.



## Capturas:

