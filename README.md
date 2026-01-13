function calcularSaldo(vitorias, derrotas) {
    const saldo = vitorias - derrotas;
    let nivel = "";

    if (saldo <= 10) {
    nivel = "Ferro";
    } else if (saldo <= 20) {
    nivel = "Bronze";
    } else if (saldo <= 50) {
    nivel = "Prata";
    } else if (saldo <= 80) {
    nivel = "Ouro";
    } else if (saldo <= 90) {
    nivel = "Diamante";
    } else if (saldo <= 100) {
    nivel = "Lendário";
    } else {
    nivel = "Imortal";
    }

    return { saldo, nivel };
}

const resultado = calcularSaldo(35, 10); //exemplo com valores 35 (vitórias) e 10 (derrotas)
console.log(`O herói tem saldo de ${resultado.saldo} e está no nível ${resultado.nivel}.`); 
//Saída: O herói tem saldo de 25 e está no nível Prata
