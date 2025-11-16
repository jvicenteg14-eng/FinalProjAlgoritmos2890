
#include <iostream>
using namespace std;

// -------- EJERCICIO 1: FUNCIÓN VOCAL --------
bool Vocal(char c) {
    if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u' ||
        c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U') {
        return true;
    } else {
        return false;
    }
}

// -------- EJERCICIO 2: FUNCIÓN CAPICUA --------
bool EsCapicua(int n) {
    int original = n;
    int invertido = 0;

    while (n > 0) {
        int digito = n % 10;
        invertido = invertido * 10 + digito;
        n = n / 10;
    }

    return original == invertido;
}

// -------- EJERCICIO 3: INVERSO DE UN NÚMERO --------
int Inverso(int n) {
    int invertido = 0;
    while (n > 0) {
        int digito = n % 10;
        invertido = invertido * 10 + digito;
        n /= 10;
    }
    return invertido;
}

// -------- PROGRAMA PRINCIPAL --------
int main() {

    // ---- Primer ejercicio ----
    char letra;
    cout << "Ingrese un caracter: ";
    cin >> letra;

    if (Vocal(letra)) {
        cout << "Es una vocal." << endl;
    } else {
        cout << "No es una vocal." << endl;
    }

    // ---- Segundo ejercicio ----
    int numero;
    cout << "\nIngrese un numero entero: ";
    cin >> numero;

    if (EsCapicua(numero)) {
        cout << "El numero es capicua." << endl;
    } else {
        cout << "El numero NO es capicua." << endl;
    }

    // ---- Tercer ejercicio (Inverso) ----
    cout << "\nEl inverso del numero es: " << Inverso(numero) << endl;

    return 0;
}
