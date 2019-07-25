colocarQueen(n, t)

let tableroTotal = board(t); // esta variable tendrá almacenada una matriz de objetos (posiciones y booleanos) con un ancho de t y un alto de t;

for (let i = 0; i < n; i ++)

let posicionesAmenazadas = tableroTotal.elegirMinCasillas() // este metodo itera la matriz de tableroTotal posicionando una Queen en cada casilla con estado true y cuenta cuantas casillas quedan amenazadas. 
//Para seleccionar las casillas amenazadas selecciona:
	//la propia posicion de la Queen
	//todas las casillas que compartan la misma posición x, 
	//todas las casillas que compartan la posicion y 
	//todas sus diagonales
	/*	   diagoArrDer: sumar uno a cada coordenada  hasta que una de ellas llegue a cero
		   diagoArrIzq: sumar uno a la coordenada y y restar uno a la coordenada x hasta que una de ellas 					llegue a cero
		   diagoAbaDer: sumar uno a la coordenada x y restar uno a la coordenada y hasta que una de ellas 					llegue a cero
		   diagoAbaIzq: restar uno a cada coordenada  hasta que una de ellas llegue a cero*/

//Genera un array de objetos {tablero, numeroDeCasillasAmenazadas};

let tablero = posicionesAmenazadas.find() // encuentra el objeto que su propiedad numeroDeCasillasAmenazadas sea 						     menor y me devuelva su propiedad tablero;

tableroTotal = merge(tableroTotal, tablero) // este metodo compara cada posicion de ambos tableros y genera un nuevo tablero
	// si la posicion comparada es false contra false el resultado sera: false
	// si la posicion comparada es false contra true el resultado sera: false
	// si la posicion comparada es true contra true el resultado sera: true
