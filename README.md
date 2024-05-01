# kubernetes-nora

## **k8s**

Se presenta una aplicación en kubernetes montada con wordpress y mysql.

Dentro de la carpeta se encuentran los archivos correspondientes para el despliegue tanto de la aplicación como de la base de datos. Podemos ver los siguientes:
- Deployments
- Services
- Statefulsets
- Volumes
- Configmap
- Secret

Para ejecutar los archivos anteriormente mencionados se debe usar el siguiente comando.

    kubectl apply -f .

*Nota: Si utilizas la aplicación con minikube el tendrás que abrir el puerto que te dará el siguiente comando:

>minikube service wordpress-service --url

## **Charts**

En este caso se trata de una aplicación wordpress y mariadb, creada con 'helm'.

Mediante el arvhivo value.yaml podemos configurarla y añadir los valores que se consideren.

Para su instalación dentro de la carpeta charts lanzaremos el siguiente comando.

    helm install mywordpress ./mywordpress

Para eliminar los paquetes que hemos creado:

    helm uninstall mywordpress


*Nota: Si utilizas la aplicación con minikube tendrás que abrir el puerto que te dará el siguiente comando:

>minikube service mywordpress --url