# Webhook Deploy

_Despliegue automático._

## Requerimientos

* El servidor requiere tener `git` y `rsync` para la ejecución correcta del Script.
* El usuario PHP que ejecute el script, deberá tener los permisos necesarios para el Directorio Temporal (Ejemplo: `/tmp`) y el directorio destino (Ejemplo: `/var/www/html/project1`.
* If the Git repository you wish to deploy is private, the system user running PHP
  also needs to have the right SSH keys to access the remote repository.

## Uso

 * Edite los parametros que se encuentran en el archivo `settings.xml` de acuerdo a los valores suministrados por su proveedor.
 * Configure su repositorio con la url que ejecutara el script:

### GitHub

 1. _((Este paso solo es necesario para los repositorios privados)_ Vaya a `https://github.com/USERNAME/REPOSITORY/settings/keys` y agregue su clave SSH del servidor.
 1. Vaya a `https://github.com/USERNAME/REPOSITORY/settings/hooks`.
 1. Haga click en **Agregar webhook** en el panel **Webhooks**.
 1. Introduzca la **URL** de carga para su script de implementación, ejemplo: `http://example.com/deploy.php?sat=YourSecretAccessTokenFromDeployFile`.
 1. Opcional Elija los eventos que deben desencadenar la implementación.
 1. Asegúrese de que la casilla de verificación **Activado** está marcada.
 1. Haga clic en **Agregar webhook**.

### Bitbucket

 1. _(Este paso solo es necesario para repositorios privados)_ Vaya a
    `https://bitbucket.org/USERNAME/REPOSITORY/admin/deploy-keys` y agregue su clave SSH del servidor.
 1. Vaya a `https://bitbucket.org/USERNAME/REPOSITORY/admin/`.
 1. En la parte de **Flujo de trabajo** haga click en **Webhooks**
 1. Agregar nuevo **webhook**.
 1. Ingrese la **URL** de de su script Ejemplo: `http://example.com/deploy.php?sat=access_token`.
 1. Click **Guardar**.


## Creditos

El creador del Deploy es markomarkovic en su repositorio encontraran las nuevas versiones y más información hacerca del funcionamiento: `https://github.com/markomarkovic/simple-php-git-deploy`.
```Este solo es una adecuación para lo que básicamente necesitabamos.```
