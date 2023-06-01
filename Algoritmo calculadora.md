# Algoritmo Calculadora
## Participantes: 
### Erwin Alberto Ramirez Racancoj
### Dariell Anthony De Leon Torres 
### Emilia Elizabeth Ramirez Tobias


Algoritmo calculadora
	tipo = ' '      // declaramos variables
	Limpiar Pantalla
	Mopcion = 0
	menu() // definimos la funcion menu
	Definir cantidad, i, j Como Entero 
	Definir a,b,n Como Entero
FinAlgoritmo

Funcion menu
	Repetir
		Limpiar Pantalla
		Escribir ' * SUPER CALCULATOR *'
		Escribir '1. Suma'
		Escribir '2. Resta'
		Escribir '3. Multiplicacion'
		Escribir '4. Division'
		Escribir '5. Suma Matriz'            //Menu de opciones
		Escribir '6. Resta Matriz'
		Escribir '7. Triangulo'
		Escribir '8. Cuadrado'
		Escribir '11. Salir'
		Escribir 'Seleccione Mopcion ->' 
		Leer Mopcion            // Se almacenan los datos ingresados a la variable Mopcion 
		Si Mopcion = 1 Entonces
			tipo = 'Suma'
		FinSi
		Si Mopcion = 2 Entonces
			tipo = 'Resta'
		FinSi
		Si Mopcion = 3 Entonces
			tipo = 'Multiplicacion'      //Basicamente se traduce si Mopcion es igual a 3 entonces
		FinSi                              // asignar a la variable tipo Multiplicacion
		Si Mopcion = 4 Entonces
			tipo = 'Division'
		FinSi
		Si Mopcion = 5 Entonces
			totalsm
		FinSi
		Si Mopcion = 6 Entonces
			totalrm
		FinSi
		
		Si Mopcion = 7 Entonces     // en este apartado de aqui comenzamos a hacer el uso de las 
			triangulo             //funciones, traduciendoce a que si Mopcion es igual 
		FinSi                       
		
		Si Mopcion = 8 Entonces
			cuadrado
		FinSi
		
		Si Mopcion = 11 Entonces
			tipo = 'Adios amigo...'    // Esta opcion nos ayuda a finalizar con la ejecucion
		FinSi                             // del programa
		Si Mopcion < 5 Entonces	
			Escribir tipo
			Escribir 'Ingrese el primer numero'         //Esta opcion es sola y unicamente cuando
			Leer num1                                   // la Mopcion es menor a 5 porque
			Escribir 'Ingrese el segundo numero'        // de 5 para abajo son las opciones 			Leer num2                                         // artimeticas
		FinSi
		segun Mopcion hacer
			1: resultado = num1+num2
			2: resultado = num1-num2
			3: resultado = num1*num2           // asignamos a resultado las operaciones
			4: resultado = num1/num2           // aritmeticas segun la opcion seleccionada en 
			//5: totalsm                      // Mopcion 
			//6: //totalrm()
		FinSegun
		si Mopcion < 5 Entonces
			Escribir 'El resultado es :'
			Escribir resultado
			Escribir 'Presione cualquier tecla para continuar...'  // Esto funciona par moestrar
			Leer tecla                                             // el resultado de mejor manera
		FinSi
	Hasta Que Mopcion = 11
FinFuncion

funcion totalsm
	// Dimensionar la matriz (filas,columnas)
	Gsuma = 0    // asignamos el valor de 0 a Gsuma
	Escribir 'Cuantas filas'
	leer nfilas      //obtenemos los datos y los guardamos en nfias
	Escribir 'Cuantas columnas'
	leer ncol          //lo mismo con ncol
	Dimension sumat[nfilas,ncol]   // iniciamos el dimensionamiento 
	Para cfilas = 0 hasta nfilas-1 Hacer   //hacemos el uso de las sentencias de repeticion 
		Para ccol = 0 hasta ncol-1 hacer	
			Escribir 'Ingrese valor'
			Escribir 'fila ',cfilas,'columna ',ccol
			Leer sumat[cfilas,ccol]
			gsuma = gsuma + sumat[cfilas,ccol]
		FinPara
	FinPara
	Escribir 'Suma de la matriz :', gsuma
	esperar tecla
	menu
FinFuncion

funcion totalrm
	// Dimensionar la matriz (filas,columnas)
	Gresta = 0
	Escribir 'Cuantas filas'
	leer nfilas
	Escribir 'Cuantas columnas'
	leer ncol
	Dimension sumat[nfilas,ncol]
	Para cfilas = 0 hasta nfilas-1 Hacer
		Para ccol = 0 hasta ncol-1 hacer	
			Escribir 'Ingrese valor'
			Escribir 'fila ',cfilas,'columna ',ccol   //Este es basicamente el mismo proceso 
			Leer sumat[cfilas,ccol]                    // en resta 
			gresta = gresta - sumat[cfilas,ccol]
		FinPara
	FinPara
	Escribir 'Suma de la matriz :', gresta
	esperar tecla
	menu
FinFuncion

Funcion triangulo
	Escribir "ingrese un numero entero: ";
	Leer cantidad;
	Para i = 0 Hasta cantidad - 1 Con Paso 1 Hacer
		Para j = 0 Hasta i Con Paso 1 Hacer        // en este ciclo podemos observar como es que 
			Escribir Sin Saltar "* ";          // imprime los asteriscos para de igual forma 
		FinPara                                  // imprimir los espacios segun lo visto en clase
		Escribir "";
		Esperar Tecla
	FinPara
FinFuncion

// la funcion del cuadrado, le dejo el siguiente recurso para que pueda ver en que me base para hacerlo
// https://www.youtube.com/watch?v=1NgtRTj0w68
Funcion cuadrado 
	Escribir "ingrese un numero entero"
	leer n 
	para a = 1 hasta n hacer 
		para b = 1 hasta n hacer
			si a >1 y a < n y b > 1 y b < n entonces      
				Escribir "  " Sin Saltar
			SiNo
				Escribir "* " Sin Saltar
			FinSi
		FinPara
		Escribir ""
		Esperar tecla
	FinPara
FinFuncion