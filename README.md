//Rosilaine
// Função soma
function soma(a, b) {
    return a + b;
}

// Função subtração
function subtracao(a, b) {
    return a - b;
}

// Função multiplicação
function multiplicacao(a, b) {
    return a * b;
}

// Função divisão
function divisao(a, b) {
    if (b === 0) {
        return "Erro: divisão por zero não é permitida.";
    } else {
        return a / b;
    }
}

// Função para solicitar e processar a operação
function calcular() {
    // Solicitar os números e a operação ao usuário
    const num1 = parseFloat(prompt("Digite o primeiro número:"));
    const num2 = parseFloat(prompt("Digite o segundo número:"));
    const operacao = prompt("Digite a operação (+, -, *, /):");

    // Verificar qual operação foi escolhida e chamar a função correspondente
    let resultado;
    if (operacao === "+") {
        resultado = soma(num1, num2);
    } else if (operacao === "-") {
        resultado = subtracao(num1, num2);
    } else if (operacao === "*") {
        resultado = multiplicacao(num1, num2);
    } else if (operacao === "/") {
        resultado = divisao(num1, num2);
    } else {
        resultado = "Operação inválida!";
    }

    // Exibir o resultado no console
    console.log("Resultado: " + resultado);
}

// Chamar a função calcular para iniciar o programa
calcular();
