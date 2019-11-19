# Practica03-Javascript

# DESARROLO 
•	Diseñar una interfaz en HTML que permita ingresar los siguientes campos en un formulario: cedula, nombres, apellidos, dirección, teléfono, fecha de nacimiento, correo electrónico y contraseña. Luego, usando funciones de JavaScript se pide validar que todos los campos han sido ingresados, 
además; que los valores ingresados en cada campo del formulario sean correctos

 ![sesion](https://user-images.githubusercontent.com/56410422/69182569-4a5fd280-0adf-11ea-91ce-5fb2a5c19396.JPG)

•	Se debe validar qué, en el campo de la cedula, se ingrese sólo números y que
la misma sea correcta, en base, al último dígito verificador.

![sesion2](https://user-images.githubusercontent.com/56410422/69182633-69f6fb00-0adf-11ea-9f29-adfb1ead8d99.JPG)

•	Se debe validar qué, en el campo del nombres, ingrese mínimo un nombre y que permita ingresar sólo letras y 
•	Se debe validar qué, en el campo del apellidos, ingrese mínimo un apellido y que permita ingresar sólo letras. 


![SESION5](https://user-images.githubusercontent.com/56410422/69182861-dd990800-0adf-11ea-8a62-f42ff8870c71.jpg)

•	Se debe validar qué, en el campo del teléfono, permita ingresar sólo números y un máximo de 10.

En este campo se valida, que el numero solo sea un maximo de 10 numeros.

![TELEFON](https://user-images.githubusercontent.com/56410422/69183010-1d5fef80-0ae0-11ea-9847-9b1d8bd2e71b.jpg)


•	Se debe validar que la fecha de nacimiento ingrese en el formato dd/mm/yyyy.

Aqui Podemos  ver que la fecha esta incorrecta ya que no hay mes 13 

![SESION 7 ](https://user-images.githubusercontent.com/56410422/69182899-eb4e8d80-0adf-11ea-9171-45e098f47d7e.jpg)

•	Se debe validar qué, en el campo correo electrónico, permita ingresar un correo válido. Se considera un correo válido, cuando comienza por tres o más valores alfanuméricos, luego un @, 
seguido por la extensión “ups.edu.ec” o “est.ups.edu.ec”.

![SESION8](https://user-images.githubusercontent.com/56410422/69182897-eb4e8d80-0adf-11ea-880a-96e70a836a93.jpg)

•	Se debe validar que la contraseña ingresada tenga mínimo 8 caracteres, además, debe incluir al menos: una letra mayúscula, 
una letra minúscula y un carácter especial (@, _, $)

![SESION9](https://user-images.githubusercontent.com/56410422/69182898-eb4e8d80-0adf-11ea-88c4-968ca44ef3a2.jpg)

### Se creo la pagina php que nos dirigia que hemos pasado todas las validaciones que nos presenta

![sesion10](https://user-images.githubusercontent.com/56410422/69184192-6153f400-0ae2-11ea-8106-c42c6cca51dc.JPG)


## PRACTICA FOTOS ALEATORIAS

•	 Diseñar una interfaz en html que tenga tres botones que diga “Anterior”“Iniciar”, “Siguiente”, y una imagen. Luego, desde javascript se debe controlar para al hacer clic sobre uno de los botones realice una acción relacionada a una galería de imágenes
Cuando entramos a la pagina nos muesta asi bloqueado el anterior por que es la primera imagen  :

![foto1](https://user-images.githubusercontent.com/56410422/69183606-446af100-0ae1-11ea-9acc-e030e6e6f688.jpg)

Cuando damos click al siguiente imagen ahí si se me habilita el anterior por que si hay una imagen atrás 

![foto2](https://user-images.githubusercontent.com/56410422/69183607-446af100-0ae1-11ea-9132-77c0f67d43ee.jpg)


Cuando estamos en la ultima imagen damos clic en anterior, pero no se nos da ya que no tenemos mas por que solo son 5 imágenes.

![foto3](https://user-images.githubusercontent.com/56410422/69183605-446af100-0ae1-11ea-8a6a-210eccfffb73.jpg)

### CODIGO HTML QUE ESTA CON CSS

```

<!DOCTYPE html>
<html>
<head>

        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" /> 

        <link rel="stylesheet" type="text/css" href="css/formulario.css">
         <script type = "text/javascript" src = "validaciones.js"></script> 
        
        

<title>INICAR SESION</title>


<center>
<h1> INICIAR SESION</h1>

<h3>LLENE LOS CAMPOS</h3>
</center>

<body>
    
<header class="titulo3" >
     
        <form id="formulario01" method="POST" action="usuariocreado.php"
        onsubmit="return validarCamposObligatorios()">
        <label for="cedula">Cedula(*)</label>
        <input type="text" id="cedula" name="cedula" value="" placeholder="Ingrese el número de cedula... " onkeyup=" return valNumeros(this)"/>
        <span id="mensajeCedula" class="error"> </span>
        <br>
        <label for="nombres">Nombres (*)</label>
        <input type="text" id="nombres" name="nombres" value="" placeholder="Ingrese sus dos nombres..."
            onkeyup="valLetras(this)" />
        <span id="mensajeNombres" class="error"></span>
        <br>
        <label for="apellidos">Apelidos (*)</label>
        <input type="text" id="apellidos" name="apellidos" value="" placeholder="Ingrese sus dos apellidos..."
            onkeyup="valLetras(this)" />
        <span id="mensajeApellidos" class="error"></span>
        <br>
        <label for="direccion">Dirección (*)</label>
        <input type="text" id="direccion" name="direccion" value="" placeholder="Ingrese su dirección ..." />
        <span id="mensajeDireccion" class="error"></span>
        <br>
        <label for="telefono">Teléfono (*)</label>
        <input type="text" id="telefono" name="telefono" value="" placeholder="Ingrese su número telefónico..."
            onkeyup="valNumeros(this)" />
        <span id="mensajeTelefono" class="error"></span>
        <br>
        <label for="fecha">Fecha Nacimiento dd/mm/yyyy (*)</label>
        <input type="text" id="fechaNacimiento" name="fechaNacimiento" value=""
            placeholder="Ingrese su fecha de nacimiento ..." onkeyup=" return valFecha(this)" />
        <span id="mensajeFechaNacimiento" class="error"></span>
        <br>
        <label for="correo">Correo electrónico (*)</label>
        <input type="text" id="correo" name="correo" value="" placeholder="Ingrese su correo electrónico..." />
        <span id="mensajeCorreo" class="error"></span>
        <br>
        <label for="contrasena">Contraseña(*)</label>
        <input type="password" id="contrasena" name="contrasena" value="" placeholder="Ingrese su contraseña..."
        onkeyup=" return valContra(this)"/>
        <span id="mensajeContrasena" class="error"></span>
        <br>
        <input  type="submit" id="crear" name="crear" value="   Aceptar" />
        <input type="reset" id="cancelar" name="cancelar" value="   Cancelar" />
    </form>



</header>


</body>

&nbsp;

&nbsp;

&nbsp;
&nbsp;
&nbsp;

&nbsp;
&nbsp;

&nbsp;

&nbsp;

&nbsp;

<footer class="dark">     
        <p> <strong>ESTUDIANTE: </strong> DAVID ISRAEL LEON GALLARDO</p>
        <p><strong>UNIVERSIDAD : </strong> Politecnica Salesiana </p> 
          <a href="mailto:dleong2@est.ups.edu.ec">dleong2@est.ups.edu.ec</a>
               <a href="tel:+593-984947138">0984947138</a>
            <br>© Todos los derechos reservados
           </footer>

</html>
```


