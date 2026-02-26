# ANTLR-CALCULADORA
### calculadora usando las instrucciones en el libro " The Definitive ANTLR 4 Reference"
---

## Requisitos

- Java JDK 8 o superior
- ANTLR 4.13.1

---

## Instalación

### 1. Instalar Java

```bash
sudo apt update
sudo apt install default-jdk
java -version
```
### 2. Descargar ANTLR 
```
cd /usr/local/lib
sudo wget https://www.antlr.org/download/antlr-4.13.1-complete.jar
```

### 3. Configurar alias
```
alias antlr4='java -jar /usr/local/lib/antlr-4.13.1-complete.jar'
alias grun='java -jar /usr/local/lib/antlr-4.13.1-complete.jar org.antlr.v4.gui.TestRig'
```

### 4. Generar el Analizador
A partir de la gramática:
```
antlr4 -visitor Calc.g4
```
Archivos generados automáticamente:
<br>
- CalcLexer.java
- CalcParser.java
- CalcVisitor.java
- CalcBaseVisitor.java
- Archivos .tokens y .interp
- Clases .class correspondientes

### 5. Compilación
```
javac -cp ".:/usr/local/lib/antlr-4.13.1-complete.jar" *.java
```
### 6. Ejecución
Pueden modificar el `input.txt` como les parezca.
```
java -cp ".:/usr/local/lib/antlr-4.13.1-complete.jar" Calc < input.txt
```

# Capturas tomadas haciendo la prueba
