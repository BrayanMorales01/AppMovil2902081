# AppMovil2902081
Aplicacion movil Brayan Morales

// Ejercicio de variables
// Primero se le pide al usuario ingresar el nombre y edad
// Se guardan los datos con "readLine"
// Si ambos son correctos muestra el mensaje de nombre y edad
// Si no son correctos se muestra el mensaje que da error
fun main() {
    print("Digite el nombre: ")
    val nombre = readLine()
    print("Digite la edad: ")
    val edad = readLine()
    
    if (nombre != null && edad != null) {
        println("Te llamas $nombre, tienes $edad años.")
    } else {
        println("Error al ingresar los datos.")
    }
}

//Constantes
//Definimos la constante , despues le damos valor al radio y con la ecuacion la definimos 
fun main() {
    val PI = 3.14159
    val radio = 5.0
    val area = PI * radio * radio
    println("El área del círculo con radio $radio es %.2f".format(area))
}


//Opcionales
// Definimos una funcion y damos un argumento que puede ser null y es opcional
// En el of se genera un saludo generico
// En el main llamamos saludar y se muestra el saludo
fun saludar(nombre: String? = null) {
    if (nombre != null) {
        println("Hola $nombre!")
    } else {
        println("Hola, ¿cómo estás?")
    }
}
fun main() {
    saludar("Juan")  
    saludar()         // Salida: Hola, ¿cómo estás?
}




//Manejo de nulos
//Dentro de la funcion se utiliza "?" para manejar los nulos de forma segura
//Se calcula la raiz y devulve como un doble
//Se imprime el resultado
  fun calcularRaizCuadrada(numero: Int?): Double? {
    return numero?.takeIf { it > 0 }?.let { Math.sqrt(it.toDouble()) }
}

fun main() {
    val num1: Int? = 16
    val num2: Int? = null

    println("Raíz cuadrada de $num1: ${calcularRaizCuadrada(num1)}") // Salida: 4.0
    println("Raíz cuadrada de $num2: ${calcularRaizCuadrada(num2)}") // Salida: null
}
 



