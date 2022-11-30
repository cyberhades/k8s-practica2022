# Práctica 2022

El objetivo de esta práctica es desplegar un Pod con la imagen tuxotron/demoapp:v1 en un espacio de nombres con seguridad restringida.

1. Crear un espacio de nombres llamado practica2022
2. Establecer en dicho espacio de nombres el perfil restrictivo de seguridad y forzado (Pod Security Admission)
3. Desplegar el siguiente pod (pod.yaml):
```
apiVersion: v1
kind: Pod
metadata:
  name: app
  namespace: practica2022
spec:
  containers:
  - image: tuxotron/demoapp:v1
    name: app
```

PD: inicialmente dicho pod no se podrá desplegar debido a las restricciones de seguridad aplicada al espacio de nombres, por lo que habrá que modificar la definición del Pod para que éste pueda ser desplegado correctamente.

La entraga de la práctica simplemente consistirá en el fichero pod.yaml modificado y los pasos con la creación del espacio de nombres con el perfil de seguridad aplicada y el despliegue de dicho Pod.