<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Logica para ingenieros</title>
<style>

body{
    background-color: black;
}


.contenedor {
  display: flex;
  width: 100%;
  height: 100vh; /* O la altura que necesites */
}

.izquierda, .derecha {
  flex: 1; /* Ambas mitades ocupan el mismo espacio */
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 20px;
  color: white;
}

.izquierda {
  background-image: url("https://www.google.com/url?sa=i&url=https%3A%2F%2Fz101digital.com%2Fjapon-accedera-a-dispositivos-privados-para-encuesta-de-ciberseguridad%2F&psig=AOvVaw34PSdv0hpQ7cyLlrB_KSKG&ust=1741238823202000&source=images&cd=vfe&opi=89978449&ved=0CBUQjRxqFwoTCLCkrJ6a8osDFQAAAAAdAAAAABBA");
}

.derecha {
  background-color: black;
  text-align: left;
}


.tabla {
  width: 200px; /* Ajusta el ancho según necesites */
  border-collapse: collapse;
  text-align: center;
  font-size: 18px;
}


.tabla2 {
  width: 600px; /* Ajusta el ancho según necesites */
  border-collapse: collapse;
  text-align: center;
  font-size: 18px;
  border-color: #545454;
}



</style>

</head>
<body>


<div class="contenedor">

    <div class="izquierda">

        
        <table class="tabla">
            <tr><td><img src="https://www.imagenesanimadas.net/Mecanica/Sirenas/Sirena-15.gif" alt="Descripción de la imagen"></td></tr>
            <tr><td><h1><label> EVALUACION DE RIESGOS </label></h1></td></tr>
            <tr><td><h3><label>Digite el nivel de riesgo del 1 al 10 que considere que este presentando</label></h3></td></tr>
            <tr><td><input type="number" id="numero"  min="1" max="10"  placeholder="Escribe aquí el nivel de riesgo del 1 al 10"></td></tr>
            <tr><td><button onclick="mostrarMensaje()">Evaluar</button></td></tr>
          
          </table>







</div>


    <div class="derecha">
        <table class="tabla2" border="1">

            <tr>
                <td></td>
                <td>Nivel</td>
                <td>Riesgo</td>
                <td>Descripcion</td>                
            </tr>

            <tr bgcolor="Green">
                <td>1.</td>
                <td>Muy bajo</td>
                <td>Errores de configuración</td>
                <td>Ajustes débiles en software o sistemas</td>
            </tr>
            <tr bgcolor="Green">
                <td>2.</td>
                <td>Bajo</td>
                <td>Contraseñas débiles</td>
                <td>Claves fáciles de adivinar permiten accesos no autorizados</td>
            </tr>
            <tr bgcolor="Green">
                <td>3.</td>
                <td>Bajo</td>
                <td>Falta de actualizaciones</td>
                <td>Software desactualizado con vulnerabilidades explotables</td>
            </tr>
            <tr bgcolor="#879203">
                <td>4.</td>
                <td>Moderado</td>
                <td>Phishing</td>
                <td>Engaños mediante correos o sitios web falsos</td>
            </tr>
            <tr bgcolor="#879203">
                <td>5.</td>
                <td>Moderado</td>
                <td>Uso de redes inseguras</td>
                <td>Wi-Fi público permite la interceptación de datos</td>
            </tr>
            <tr bgcolor="red">
                <td>6.</td>
                <td>Alto</td>
                <td>Malware y Ransomware</td>
                <td>Software malicioso roba o cifra datos para pedir rescate</td>
            </tr>
            <tr bgcolor="red">
                <td>7.</td>
                <td>Alto</td>
                <td>Ingeniería social</td>
                <td>Engaño psicológico para obtener información confidencial</td>
            </tr>
            <tr bgcolor="ae0404">
                <td>8.</td>
                <td>Muy alto</td>
                <td>Ataques de fuerza bruta</td>
                <td>Pruebas automáticas de contraseñas para acceder a cuentas</td>
            </tr>
            <tr bgcolor="7b0707">
                <td>9.</td>
                <td>Critico</td>
                <td>Ataques DDoS</td>
                <td>Sobrecarga de servidores para hacerlos inaccesibles</td>
            </tr>
            <tr bgcolor="530505">
                <td>10.</td>
                <td>Extremo </td>
                <td>Robo de datos y filtraciones</td>
                <td>Acceso no autorizado a información sensible</td>
            </tr>
            <tr>
                <td><p>Mitigación</p></td>
                <td></td>
                <td></td>
                <td><p id="mensaje"></p></td>

            </tr>
        </table>
        
        
    </div>












<script>
    function mostrarMensaje() {
        let numero = document.getElementById("numero").value;
        let mensaje = document.getElementById("mensaje");

        if (numero == 1) {
            mensaje.innerHTML = "Revisar y corregir configuraciones regularmente";
        } else if (numero == 2) {
            mensaje.innerHTML = "Usar contraseñas seguras y autenticación en dos pasos.";
        } else if (numero == 3) {
            mensaje.innerHTML = "Aplicar parches de seguridad con frecuencia.";
        } else if (numero == 4) {
            mensaje.innerHTML = "Capacitación y uso de filtros anti-phishing.";
        } else if (numero == 5) {
            mensaje.innerHTML = "Usar VPN y evitar conexiones no seguras.";
        } else if (numero == 6) {
            mensaje.innerHTML = "Antivirus, copias de seguridad y precaución con archivos desconocidos.";
        } else if (numero == 7) {
            mensaje.innerHTML = "Capacitación y verificación de identidad antes de compartir datos.";
        } else if (numero == 8) {
            mensaje.innerHTML = "Autenticación multifactor y bloqueo de intentos fallidos.";
        } else if (numero == 9) {
            mensaje.innerHTML = "Mitigación DDoS y refuerzo de infraestructura de red.";
        } else {
            mensaje.innerHTML = "Cifrado, control de accesos y monitoreo constante.";
        }
    }
</script>

</body>
</html>
