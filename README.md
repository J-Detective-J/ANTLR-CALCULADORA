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
![WhatsApp Image 2026-02-26 at 10 02 57 AM](https://github.com/user-attachments/assets/dd9bfdc9-a1b7-4b32-8740-4ed59e948fde)
![WhatsApp Image 2026-02-26 at 10 02 56 AM (3)](https://github.com/user-attachments/assets/e7348e24-8a67-45fd-86ea-f50b540dd309)
![WhatsApp Image 2026-02-26 at 10 02 56 AM (2)](https://github.com/user-attachments/assets/3fac6551-82ab-4e3a-b61b-19e5db7ad79a)
![WhatsApp Image 2026-02-26 at 10 02 56 AM (1)](https://github.com/user-attachments/assets/de4f79c8-d722-443f-86de-833951ee178a)
![WhatsApp Image 2026-02-26 at 10 02 56 AM](https://github.com/user-attachments/assets/5f93d24f-71ec-4984-9bae-79b53d8995b4)

