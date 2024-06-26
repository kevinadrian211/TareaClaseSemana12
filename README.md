fun main() {
    println("TDD")
    if (sumaParesTest()) println("passed") else println("Failed")
    if (sumaImparePrimeroTest()) println("passed") else println("Failed")
    if (sumaImpareSegundoTest()) println("passed") else println("Failed")
    if (sumaNumerosNegativosTest()) println("passed") else println("Failed")
}

fun sumaPares(a: Int, b: Int): Int {
    // Validar que ambos números sean pares y no negativos
    if (a % 2 != 0 || b % 2 != 0 || a < 0 || b < 0) return -1
    return a + b
}

// Paso uno hacer que la prueba falle
fun sumaParesTest(): Boolean {
    val actualValue = sumaPares(2, 2)
    val expectedValue = 4
    return actualValue == expectedValue
}

fun sumaImparePrimeroTest(): Boolean {
    val actualValue = sumaPares(7, 4)
    val expectedValue = -1
    return actualValue == expectedValue
}

fun sumaImpareSegundoTest(): Boolean {
    val actualValue = sumaPares(8, 3)
    val expectedValue = -1
    return actualValue == expectedValue
}

fun sumaNumerosNegativosTest(): Boolean {
    val actualValue = sumaPares(-2, -4)
    val expectedValue = -1
    return actualValue == expectedValue
}






ejercicio 2


fun main() {
    println("Validar mayoría de edad")
    if (mayoriaDeEdadTest()) println("passed") else println("Failed")
    if (edadNegativaTest()) println("passed") else println("Failed")
}

fun validarMayoriaDeEdad(edad: Int): String {
    if (edad < 0) return "REJECTED"
    return if (edad >= 18) "ACCEPTED" else "REJECTED"
}

fun mayoriaDeEdadTest(): Boolean {
    val actualValue = validarMayoriaDeEdad(18)
    val expectedValue = "ACCEPTED"
    return actualValue == expectedValue
}

fun edadNegativaTest(): Boolean {
    val actualValue = validarMayoriaDeEdad(-1)
    val expectedValue = "REJECTED"
    return actualValue == expectedValue
}



