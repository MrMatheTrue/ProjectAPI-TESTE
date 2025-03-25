Algoritmo "ProjetoApi"
var
   op : Real
   x,i, quantidade_numeros_primos, numero_atual, contador_primos, divisor, eh_primo: inteiro //eh_primo 1 para verdadeiro, 0 para falso




Inicio
   x<- 1

   Enquanto (x = 1) faca //Estrutura de repetição para o menu aparecer várias vezes

      // Exibe o menu inicial
      escreval("===================================")
      escreval("         MENU - SEQUÊNCIAS MATEMÁTICAS         ")
      escreval("===================================")
      escreval("1 | Números Triangulares")
      escreval("2 | Sequência de Números Primos")
      escreval("3 | Sequência Fatorial")
      escreval("===================================")

      Leia(op)

      Enquanto (op > 3) ou (op < 1) faca  //Limitar a escolha das opções

         Escreval("De 1 a 3 apenas")
         Leia(op)

      Fimenquanto

      Se (op = 1) entao //Condição para a primeira operação

         Escreval("Numeros Trinagulares")

      Fimse

      Se (op = 2) entao //Condição para a segunda operação
         escreval("===================================")
         escreval("     SEQUÊNCIA DE NÚMEROS PRIMOS   ")
         escreval("===================================")

         // Solicita ao usuário a quantidade de números primos desejados
         escreva("Digite a quantidade de números primos que deseja gerar: ")
         leia(quantidade_numeros_primos)

         numero_atual <- 2  // Primeiro número a ser testado
         contador_primos <- 0 // Conta quantos primos já foram encontrados

         // Loop para encontrar os números primos
         enquanto contador_primos < quantidade_numeros_primos faca
            eh_primo <- 1 // Assume que o número é primo

            // Verifica se o número atual é primo
            para i de 2 ate numero_atual - 1 faca
               se (numero_atual mod i = 0) entao
                  eh_primo <- 0 // O número não é primo
               fimse
            fimpara

            // Se for primo, exibe e incrementa o contador
            se eh_primo = 1 entao
               escreva(numero_atual, " ")
               contador_primos <- contador_primos + 1
            fimse

            numero_atual <- numero_atual + 1 // Testa o próximo número
         fimenquanto
         escreval("=====================================")
         escreval("     FIM DA SEQUÊNCIA DE PRIMOS   ")
         escreval("===================================")

      Fimse

      Se (op = 3) entao  //Condição para a terceira operação

         Escreval("Sequencia Fatorial ")

      Fimse


      repita  //Estrutura de repetição para continuar ou não o programa

         Escreval("Deseja continuar ? (0 para não ou 1 para sim)")
         leia(x)

      ate(x = 0) ou (x = 1)

      Limpatela

   Fimenquanto
fimalgoritmo