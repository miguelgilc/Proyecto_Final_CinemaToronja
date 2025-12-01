# Manual de Usuario
En este documento recopilaremos el uso del programa

## Introducción
**Cinema Toronja** es un sistema de gestión de reservas cinematográficas desarrollada por estudiantes de la Universidad de Antioquia. Este programa le va a permitir a la comuniad universitaria reservar asientos para las funciones de cine los **fines de semana**.

### ¿Que puede hacer con este programa?

**Usuario Regular**
1. Registrarse en el sistema
2. Consultar películas disponibles
3. Reservar asientos
4. Cancelar reservas
5. Ver facturas de sus comprar

**Administradores**
1. Ver las ventas
2. Exportar datos a archivos CSV
3. Consultar la información de los usuarios
4. Consultar el total de reservas registradas, pagos y tiquetes vendidos
5. Ver estadisticas de ventas
6. Lista de Usuarios

## Requisitos del Sistema

### Requisitos Funcionales

El sistema debe cumplir con las siguientes capacidades:

1. **Registro de usuarios** con validación de datos
2. **Autenticación** mediante usuario y contraseña
3. **Gestión de reservas** (crear y cancelar)
4. **Visualización de asientos** disponibles y ocupados
5. **Generación de facturas** automáticas
6. **Reportes administrativos** y estadísticas
7. **Exportación de datos** a formato CSV

### Requisitos Técnicos

- **Sistema Operativo:** Windows, macOS, o Linux
- **Python:** Versión 3.6 o superior
- **Espacio en disco:** Mínimo 10 MB
- **Memoria RAM:** Mínimo 512 MB

## Funcionalidades para Usuarios

### 1. Registro de Nuevo Usuario

**Paso a paso:**

1. Seleccione la opción `1. Registrarme` en el menú principal
2. Ingrese sus datos personales siguiendo las indicaciones:

#### a) Nombre
- Debe tener mínimo 3 letras
- Solo se permiten letras (sin números ni caracteres especiales)

#### b) Apellido
- Debe tener mínimo 3 letras
- Solo se permiten letras

#### c) Documento
- Debe tener entre 3 y 15 dígitos
- Solo números (sin letras ni puntos)

#### d) Tipo de Vínculo

Seleccione según su categoría:

```
Selecciona tu tipo de vínculo:
1. Estudiante  $7500
2. Docente  $10000
3. Administrativo  $8500
4. Oficial interno  $7000
5. Público externo  $15000
```

**Precios según tipo de usuario:**
- Estudiantes: $7,500
- Docentes: $10,000
- Administrativos: $8,500
- Oficiales internos: $7,000
- Público externo: $15,000

#### e) Usuario y Contraseña

Cree sus credenciales de acceso:

```
crear su usuario ----> soloverde
crear su contraseña ---> 777
```

**Confirmación:** Verá un mensaje indicando que su usuario fue creado exitosamente.

---

### 2. Iniciar Sesión

**Paso a paso:**

1. Seleccione `2. Iniciar sesión` en el menú principal
2. Ingrese su usuario y contraseña

```
------------------------------
 MENÚ DE INICIAR SESIÓN
---------------------------------------
ingrese su usuario----> soloverde
ingresar su contraseña---> 777
```

**Acceso exitoso:** Verá el mensaje `¡Bienvenido soloverde!` y accederá al menú principal de usuario.

---

### 3. Consultar Funciones del Fin de Semana

Esta opción muestra todas las películas disponibles.

**En el menú principal de usuario, seleccione:** `1. Consultar funciones del fin de semana`

**Información mostrada:**
- Número de película (para seleccionar)
- Nombre de la película
- Día de la función (Sábado o Domingo)
- Hora de la función
- Cantidad de sillas disponibles

**Ejemplo de salida:**

```
--- PELÍCULAS DEL FIN DE SEMANA ---
1. La estrategia del caracol - Sábado 14:00 - Sillas disponibles: 121
2. El abrazo de la serpiente - Sábado 17:00 - Sillas disponibles: 121
3. María, llena eres de gracia - Domingo 13:00 - Sillas disponibles: 121
4. Rodrigo D: No futuro - Domingo 18:00 - Sillas disponibles: 121
5. La vendedora de rosas - Domingo 20:00 - Sillas disponibles: 121
```

---

### 4. Registrar Reserva

**Paso a paso:**

1. En el menú principal de usuario, seleccione `2. Registrar reserva`
2. Se mostrarán todas las películas disponibles
3. Elija el número de la película que desea ver

```
Elige el número de la película que deseas ver: 1
```

4. Se mostrará la película seleccionada con sus detalles

5. Verá un mapa visual de los asientos:

```
--- LISTA DE ASIENTOS ---
O = Disponible | X = Ocupado

  1    2    3    4    5    6    7    8    9   10   11
  O    O    O    O    O    O    O    O    O    O    O

 12   13   14   15   16   17   18   19   20   21   22
  O    O    O    O    O    O    O    O    O    O    O

[... continúa hasta el asiento 121]
```

6. Seleccione el número del asiento que desea (1-121):

```
Ingresa el número de asiento que deseas (1-121): 45
```

7. El sistema procesará su reserva y mostrará la factura:

```
------------------FACTURA - CINEMA TORONJA---------------------------
Usuario: soloverde
Tipo de vínculo: estudiante
Película: La estrategia del caracol
Asiento: 45
Precio base: $7,500
Total a pagar: $7,500
==================================================
Disfruta la función.

Reserva registrada
```

**Importante:**
- Solo puede reservar **UN asiento** por vez
- El asiento quedará marcado como ocupado (X)
- Guarde su factura para referencia

---

### 5. Cancelar Reserva

**Paso a paso:**

1. En el menú principal de usuario, seleccione `3. Cancelar reserva`

2. Si tiene reservas activas, verá una lista:

```
--- TUS RESERVAS ---
1. La estrategia del caracol - Asiento 45 - $7,500
2. El abrazo de la serpiente - Asiento 60 - $7,500
```

3. Ingrese el número de la reserva que desea cancelar:

```
¿Qué reserva deseas cancelar? (número): 1
```

4. El sistema confirmará la cancelación:

```
Reserva cancelada
Película: La estrategia del caracol
Asiento: 45
Monto reembolsado: $7,500
```

**Importante:**
- El asiento quedará disponible nuevamente (O)
- La reserva se eliminará de su historial
- Las estadísticas del sistema se actualizarán

**Si no tiene reservas:**
```
No tienes reservas activas para cancelar.
```

---

### 6. Cerrar Sesión

Para salir de su cuenta:

1. En el menú principal de usuario, seleccione `4. Cerrar sesión`
2. Volverá al menú principal del programa

---

## Funcionalidades para Administradores

### Acceso Administrativo

**Credenciales predeterminadas:**
- Usuario: `admin1`
- Contraseña: `1234`

**Para acceder:**
1. Seleccione `2. Iniciar sesión` en el menú principal
2. Ingrese las credenciales de administrador
3. Verá el mensaje: `Bienvenido administrador`

---

### Menú de Administración

```
---------------MENÚ ADMIN----------------
1. Total de reservas registradas
2. Total de tiquetes vendidos
3. Total de reservas realizadas
4. Total pago realizado
5. Promedio por venta diario del cine
6. Lista de usuarios
7. Usuario con mayor y menor cantidad de reservas
8. Generar CSV con todas las reservas
9. Cerrar sesión
```

---

### 1. Total de Reservas Registradas

Muestra el número total de reservas activas en el sistema.

**Salida de ejemplo:**
```
Total de reservas registradas: 15
```

---

### 2. Total de Tiquetes Vendidos

Muestra la cantidad total de tiquetes vendidos (equivalente al total de reservas).

**Salida de ejemplo:**
```
Total de tiquetes vendidos: 15
```

---

### 3. Total de Reservas Realizadas

Muestra el total acumulado de reservas (incluye las activas).

**Salida de ejemplo:**
```
Total de reservas realizadas: 15
```

---

### 4. Total Pago Realizado

Muestra la suma total de dinero recaudado por todas las reservas.

**Salida de ejemplo:**
```
Total pago realizado: $112,500
```

---

### 5. Promedio por Venta Diario

Calcula el promedio de ventas por día (dividiendo el total entre 2 días: sábado y domingo).

**Salida de ejemplo:**
```
Promedio por venta diario: $56,250
```

**Si no hay ventas:**
```
No hay ventas registradas aún.
```

---

### 6. Lista de Usuarios

Muestra todos los usuarios registrados (excepto administradores) con su información.

**Salida de ejemplo:**
```
--- LISTA DE USUARIOS ---
Usuario: soloverde | Tipo: estudiante | Reservas: 2
Usuario: juliangrisales | Tipo: docente | Reservas: 1
Usuario: zelda_2 | Tipo: administrativo | Reservas: 0
```

---

### 7. Usuario con Mayor y Menor Cantidad de Reservas

Identifica qué usuario tiene más reservas y cuál tiene menos.

**Salida de ejemplo:**
```
Usuario con mayor cantidad de reservas:
  soloverde con 2 reservas

Usuario con menor cantidad de reservas:
  juliangrisales con 0 reservas
```

**Si no hay usuarios:**
```
No hay usuarios registrados aún.
```

---

### 8. Generar CSV con Todas las Reservas

Exporta todas las reservas activas a un archivo CSV.

**Proceso:**
1. Seleccione la opción `8`
2. El sistema generará el archivo `Reservas_Completas.csv` en la misma carpeta del programa

**Salida de ejemplo:**
```
✓ CSV generado exitosamente: Reservas_Completas.csv
  Total de registros: 15
```

**Estructura del archivo CSV:**
```csv
documento,nombre,apellido,vinculo,valor,pelicula,asiento
DOC0001,soloverde,apellido,estudiante,7500,La estrategia del caracol,45
DOC0002,juliangrisales,apellido,estudiante,7500,El abrazo de la serpiente,60
DOC0003,zelda_2,apellido,docente,10000,María llena eres de gracia,30
```

**Si no hay reservas:**
```
No hay reservas para exportar.
```

---

### 9. Cerrar Sesión de Administrador

Para salir del modo administrador:

1. Seleccione `9. Cerrar sesión`
2. Volverá al menú principal del programa

---

## Preguntas Frecuentes

### ¿Cuántos asientos tiene el cinema?
El cinema tiene una capacidad de **121 asientos** organizados en una matriz de 11x11.

### ¿Cuántas reservas puedo hacer?
Puede hacer múltiples reservas, pero solo **una reserva por vez**. Después de completar una reserva, puede hacer otra.

### ¿Puedo cambiar mi asiento después de reservar?
No directamente. Debe **cancelar la reserva** actual y luego hacer una nueva reserva con el asiento deseado.

### ¿Qué películas están disponibles?
Las películas disponibles son:
1. La estrategia del caracol (Sábado 14:00)
2. El abrazo de la serpiente (Sábado 17:00)
3. María, llena eres de gracia (Domingo 13:00)
4. Rodrigo D: No futuro (Domingo 18:00)
5. La vendedora de rosas (Domingo 20:00)

### ¿Cómo sé qué asientos están disponibles?
Al momento de hacer una reserva, verá un mapa visual donde:
- **O** = Asiento disponible
- **X** = Asiento ocupado

### ¿Puedo recuperar mi contraseña si la olvido?
Actualmente el sistema **no tiene función de recuperación de contraseña**. Contacte al administrador del sistema.

### ¿El sistema guarda mis datos automáticamente?
Los datos se guardan en memoria durante la ejecución del programa. Para guardar permanentemente, el administrador debe usar la opción de **generar CSV**.

### ¿Cómo exporto los datos?
Solo los administradores pueden exportar datos usando la opción `8. Generar CSV con todas las reservas` en el menú administrativo.

---

## Solución de Problemas

### Error: "Algo salió mal, contraseña o usuario incorrecto"

**Causa:** Las credenciales ingresadas no son correctas.

**Solución:**
- Verifique que escribió correctamente su usuario y contraseña
- Recuerde que son sensibles a mayúsculas y minúsculas
- Si olvidó su contraseña, contacte al administrador

---

### Error: "este usuario ya existe"

**Causa:** El nombre de usuario que intenta crear ya está registrado.

**Solución:**
- Elija un nombre de usuario diferente
- Agregue números o caracteres adicionales (ej: `juanp_2024` en vez de `juanp`)

---

### Error: "Error: el nombre debe tener al menos 3 letras"

**Causa:** El nombre ingresado es muy corto o contiene números.

**Solución:**
- Ingrese un nombre con mínimo 3 letras
- Use solo letras, sin números ni caracteres especiales
- Ejemplo válido: `Juan`

---

### Error: "Error: ese asiento ya está ocupado"

**Causa:** El asiento que seleccionó ya fue reservado por otro usuario.

**Solución:**
- Elija otro número de asiento disponible (marcado con "O")
- Consulte el mapa visual de asientos antes de seleccionar

---

### Error: "No tienes reservas activas para cancelar"

**Causa:** Intentó cancelar una reserva pero no tiene ninguna activa.

**Solución:**
- Primero haga una reserva
- Luego podrá cancelarla si lo desea

---

### El programa no inicia

**Posibles causas y soluciones:**

1. **Python no está instalado:**
   - Instale Python 3.6 o superior desde python.org

2. **Ruta incorrecta:**
   - Asegúrese de estar en la carpeta correcta (`src/`)
   - Use `cd` para navegar a la carpeta correcta

3. **Nombre de archivo incorrecto:**
   - Verifique el nombre exacto del archivo `.py`
   - Use el comando correcto: `python nombre_archivo.py`

---

## Soporte Técnico

Para reportar problemas o solicitar ayuda:

**Jefe de los Jefes**
- Julián Andrés Castillo: *jandres.castillo@udea.edu.co*
  
**Administradores**
- Sara Trujillo Berrocal: *sara.tberrocal@udea.edu.co*
- Miguel Angel Gil Ciro: *miguel.gilc@udea.edu.co*
- Mario Fernando Chaparra Falla: *mario.chaparro1@udea.edu.co*

---

**Versión del manual:** 1.0  
**Última actualización:** 30 de Noviembre 2025 
**Programa:** Cinema Toronja - Sistema de Gestión de Reservas Cinematográficas  
**Universidad de Antioquia - Facultad de Ingeniería**


