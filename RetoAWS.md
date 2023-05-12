# Reto: Infraestructura AWS 

## Construcción de una aplicación Web Serverless con *AWS Lambda, Amazon API Gateway, AWS Amplify, Amazon DynamoDB y Amazon Cognito.* 

### *Pasos a seguir:* 

1. Alojamiento de una página web estática 

2. Gestión de usuarios 

3. Construcción de un backend serverless 

4. Despliegue de una API Restful  
 

Nota: El paso a paso puede ser consultado en el siguiente sitio: [Build a Serverless Web Application](https://aws.amazon.com/es/getting-started/hands-on/build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito/). 

 
### *Alojamiento de una página web estática* 

1. Selección de región [img 1.]: Para la práctica se seleccionó la región de Norte de Virginia.  

2. Creación del repositorio (GIT) 

- Configuración del repositorio (Nombre, descripción y etiqueta) [img 2]. 

- Creación de las credenciales del repositorio en IAM [img 3]. 

- Identificación de la URL del repositorio [img 4]. 

- Posteriormente se clona el repositorio en la máquina local. Se requiere usar las credenciales antes creadas [img 5].  

- Verificar la clonación del repositorio [img 6]. 

3. Copiar los archivos del programa alojados en el bucket s3, hacia la carpeta del repositorio local. Se utilizó la siguiente línea (aws s3 cp s3://wildrydes-us-east-1/WebApplication/1_StaticWebHosting/website ./ --recursive)[img 7]. 

*Nota:* Antes de hacer el paso 3, se requiere haber instalados *AWS CLI, e ingresar las credenciales en la terminal usando el comando *aws config. 

4. Se suben los cambios del repositorio local, al repositorio remoto [img8] [img9] [img10].  

5. Se crea una nueva aplicación en AWS Amplify [img 11]. 

6. Se selecciona el repositorio y la rama [img 12]. 

7. Se configura la compilación, y se permite que se construya automáticamente [img 13]. 

8. Se espera que se aprovisione, se compile y se implemente la aplicación [img 14]. 

9. Se valida que la aplicación se haya desplegado [img 15]. 

10. Se modifica el archivo index.html, en este caso se cambia el valor del title [img 16]. 

11. Una vez se haya implementado los cambios, se valida la modificación [img 17]. 
 

## Autenticación de Usuarios con AWS Cognito 

1. Se crea un pool de usuarios en Amazon Cognito. 

2. En opciones de inicio sesión se deja seleccionado "Nombre de usuario" [img 18]. 

3. Se selecciona valores predeterminados de Cognito [img 19]. 

4. En este caso se seleccionó autenticación sin MFA [img 20]. 

 
Nota: Antes de continuar se debe crear una identidad en Amazon SES (En este caso con el correo corporativo) [img 21]. 


5. Se finaliza con la creación del servicio en Cognito. 

6. Se ingresa los valores generados por el servicio Cognito, en el archivo config.js [img 22]. 

7. En la página de la app se hace un registro con un correo ficticio y se evidencia que sale un popout [img 23]. 

8. En el servicio de Cognito se valida la creación del usuario, y posteriormente se confirma la creación [img 24] [img 25]. 

9. Se hace un inicio de sesión con el usuario registrado, y se valida la autenticación mediante el popout [img 26].
