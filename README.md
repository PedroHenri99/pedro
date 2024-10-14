function pertenceAFibonacci(numero) {
    // Inicializa os dois primeiros números da sequência
    let a = 0, b = 1;

    
    if (numero === a || numero === b) {
        return true;
    }

    // Calcula a sequência de Fibonacci
    while (b <= numero) {
        let proximo = a + b; 
        a = b; 
        b = proximo; 

        // Verifica se o número pertence à sequência
        if (b === numero) {
            return true;
        }
    }

    // Se não encontrou o número na sequência
    return false;
}

// Função para usar a entrada do usuário
function verificarFibonacci() {
    const numero = parseInt(prompt("Informe um número: "), 10);

    if (isNaN(numero)) {
        alert("Por favor, insira um número válido.");
        return;
    }

    const pertence = pertenceAFibonacci(numero);
    if (pertence) {
        alert(`O número ${numero} pertence à sequência de Fibonacci.`);
    } else {
        alert(`O número ${numero} não pertence à sequência de Fibonacci.`);
    }
}

// Chama a função para verificar o número
verificarFibonacci();
