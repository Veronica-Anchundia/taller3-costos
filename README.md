# Taller Grupal 3: Lambdas y patrón Strategy

**Universidad:** Universidad Agraria del Ecuador  
**Asignatura:** Programación 3 · POO Avanzada  
**Semana:** 3  
**Paralelo:** C  
**Grupo:** 08  
**Docente:** Ing. Hamilton Villamar  
**Fecha:** 31 de octubre de 2026  

Calculadora de costos de producción para una finca ecuatoriana que produce banano, cacao y arroz.

## Integrantes y roles

| N.º | Apellidos y nombres | Rol |
|---:|---|---|
| 1 | Verónica Anchundia | Coordinadora |
| 2 | Narciso Galarza | Desarrollador principal |
| 3 | Brithany Rivera | Revisora de calidad |
| 4 | Alfonso Olvera | Integrante |
| 5 | Michael Caicedo | Integrante |

## Descripción

El programa calcula los costos de producción de lotes agrícolas con distintas estrategias intercambiables. Aplica el patrón **Strategy**, expresiones lambda, interfaces funcionales, una jerarquía sellada de cultivos, *pattern matching* y `Optional`.

Captura 
<img width="1910" height="1019" alt="image" src="https://github.com/user-attachments/assets/9e33f7d2-8cc4-420a-a77c-92f2c05f2a36" />

## Estrategias de cálculo

1. Costo directo de insumos.
2. Insumos más mano de obra.
3. Costo por hectárea.
4. Subsidio del 20 % a la urea.
5. Aplicación del IVA del 15 % sobre otra estrategia.

## Tecnologías y requisitos

- **Java JDK 21**
- **Apache Maven 3.9 o superior**
- **JUnit 5** para las pruebas automatizadas
- **IntelliJ IDEA** (opcional, para abrir y ejecutar el proyecto)

Verifica las instalaciones desde una terminal:

<img width="1918" height="1015" alt="image" src="https://github.com/user-attachments/assets/d1279181-d6e6-465d-8d27-0435a443b314" />

<img width="1919" height="1000" alt="image" src="https://github.com/user-attachments/assets/d15d1a59-d520-4e31-ade1-bab03f848d1e" />


```bash
java -version
mvn -version
Java debe mostrar la versión 21 y Maven la versión 3.9 o superior.
Estructura del proyecto
taller3-costos/
├── src/
│   ├── main/java/ec/uagraria/costos/
│   │   ├── Arroz.java
│   │   ├── Banano.java
│   │   ├── Cacao.java
│   │   ├── CalculadoraCostos.java
│   │   ├── Cultivo.java
│   │   ├── EstrategiaCosto.java
│   │   ├── Estrategias.java
│   │   ├── Insumo.java
│   │   ├── Lote.java
│   │   └── Main.java
│   └── test/java/ec/uagraria/costos/
│       └── CalculadoraCostosTest.java
├── pom.xml
└── README.md
Compilar el proyecto
Abre una terminal en la carpeta donde está pom.xml y ejecuta:
mvn clean compile
Ejecutar las pruebas
El proyecto incluye 14 pruebas automatizadas con JUnit 5:
mvn clean test
Si Maven termina con BUILD SUCCESS, las pruebas pasaron correctamente.
Ejecutar el programa
Para correr la clase principal:
mvn exec:java
En IntelliJ IDEA también puedes abrir Main.java y pulsar el botón verde Run. Para ejecutar las pruebas, abre CalculadoraCostosTest.java, haz clic derecho y selecciona Run.
Resultados verificados
Para un lote de banano de 4 hectáreas y uno de cacao orgánico de 2,5 hectáreas:
Caso	Resultado
Calculadora sin estrategia	Optional.empty
Costo directo del banano	USD 744,00
Insumos más mano de obra	USD 2.076,00
Costo por hectárea	USD 519,00
Subsidio del 20 % a la urea	USD 1.998,00
Costo con IVA del 15 %	USD 2.387,40
Jornales por hectárea del cacao orgánico	25
Insumos más mano de obra del cacao orgánico	USD 1.612,75


Repositorio y pull request
- Repositorio en GitHub
-https://github.com/narcisogalarza2006-boop/taller3-costos/pull/1
