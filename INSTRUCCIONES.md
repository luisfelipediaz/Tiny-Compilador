# Definiciones de archivos

## Archivos de encabezados 
- ANALYZE.H (interfaz del analizador semántico)
- CGEN.H (interfaz del generador de código)
- CODE.H (interfaz para emitir código e interfaz de la TM Tiny Machine)
- GLOBALS.H (tipos y variables globales)
- PARSE.H (interfaz del analizador sintáctico)
- SCAN.H (interfaz del analizador léxico)
- SYMTAB.H (interfaz para la tabla de símbolos)
- UTIL.H (funciones de utilidad)
## Archivos de código C 
- ANALYZE.C (analizador semántico)
- CGEN.C (generador de código)
- CODE.C (utilidades de emisión de código TM)
- MAIN.C (programa principal)
- PARSE.C (analizador sintáctico)
- SCAN.C (analizador léxico)
- SYMTAB.C (tabla de símbolos)
- TM.C (Tiny Machine)
- UTIL.C (funciones de utilidad).
# Pre requisitos

Se debe contar con el CLI de visual c++ que se puede encontrar en la dirección https://www.visualstudio.com/es/thank-you-downloading-visual-studio/?sku=BuildTools&rel=15
y no estoy seguro pero creo que también es necesario tener instalado visual studio

# Instrucciones
- Primero de deben complilar los archivos .c
    >\> cl analyze.c cgen.c code.c main.c parse.c scan.c symtab.c util.c -o tiny*
- El archivo generado tiny.exe sirve para compilar el archivo que tiene el código sample.tny y genera el archivo sample.tm
    >\> tiny sample.tny
- se usa la maquina tiny para generar generar un traductor
    >\> cl tm.c -o trd
- Luego se usa el traductor para resolver las instrucciones de esamblador del archivo sample.tm
    >\> trd  sample.tm
- Se debe abrir en la linea de comando el CLI de ejecución del la instrucción del archivo sample.tm 
