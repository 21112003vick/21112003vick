<programa> ::= "Algoritmo" <nombre> <declaraciones> <cuerpo> "Fin"

<nombre> ::= <identificador>

<declaraciones> ::= {<declaracion>}

<declaracion> ::= <tipo_dato> ":" <identificador> ";"
                | "Constantes" ":" {<identificador> "=" <valor> ";"}

<tipo_dato> ::= "Entero" | "Real" | "Logico" | "Caracter" | "Cadena"

<identificador> ::= <letra> {<letra> | <digito>}

<letra> ::= "a" | ... | "z" | "A" | ... | "Z"
<digito> ::= "0" | ... | "9"

<cuerpo> ::= "Inicio" {<instruccion>} "Fin"

<instruccion> ::= <asignacion> 
                | <estructura_control> 
                | <entrada_salida>

<asignacion> ::= <identificador> "=" <expresion> ";"

<estructura_control> ::= "Si" <condicion> "Entonces" <instruccion> {"Sino" <instruccion>} "FSi"
                      | "Para" <identificador> "=" <expresion> "Hasta" <expresion> "Hacer" <instruccion> "FPara"
                      | "Mientras" <condicion> "Hacer" <instruccion> "FMientras"

<condicion> ::= <expresion> <operador_logico> <expresion>
<operador_logico> ::= "==" | "!=" | "<" | ">" | "<=" | ">=" | "&&" | "||"

<expresion> ::= <termino> {<operador> <termino>}
<termino> ::= <identificador> | <valor> | "(" <expresion> ")"
<operador> ::= "+" | "-" | "*" | "/"

<valor> ::= <numero> | <cadena>
<numero> ::= <digito> {<digito>} ["." <digito> {<digito>}]
<cadena> ::= '"' {<caracter>} '"'
<caracter> ::= <letra> | <digito> | " " | ... 

<entrada_salida> ::= "Escribir" "(" <cadena> ")" ";"
                   | "Leer" "(" <identificador> ")" ";"

