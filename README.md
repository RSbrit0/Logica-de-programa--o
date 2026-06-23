# Logica de programação
 curso de logica
Calculadora em Python
 Como executar
Opção 1 — Diretamente com Python
Certifique-se de ter o Python 3 instalado, então execute:

python3 calculadora.py
Opção 2 — Usando o arquivo .sh (Linux/Mac)
O arquivo executar.sh automatiza a execução. Siga os passos:

1. Dê permissão de execução ao script:

chmod +x executar.sh

2. Execute o script:

./executar.sh

O script executar.sh verifica automaticamente se o Python 3 está instalado antes de rodar a calculadora. Se não estiver, exibe uma mensagem de erro com o link para download.


 Explicação do código Python
Estrutura geral
O programa inteiro está dentro de uma função chamada calculadora(), que roda em um loop infinito (while True) — ou seja, continua pedindo novos cálculos até o usuário escolher sair.
Passo a passo do código
def calculadora():

    while True:

Define a função e inicia o loop. O programa só para quando o usuário digitar a opção 5.



        try:

            num1 = float(input("Digite o primeiro número: "))

            num2 = float(input("Digite o segundo número: "))

Pede dois números ao usuário. O float() permite aceitar números decimais (ex: 3.5). O bloco try captura erros caso o usuário digite algo que não seja número.



            print("Escolha a operação:")

            print("1. Soma (+)")

            print("2. Subtração (-)")

            print("3. Multiplicação (*)")

            print("4. Divisão (/)")

            print("5. Sair")

            opcao = int(input("Digite o número da operação: "))

Exibe o menu de opções e lê a escolha do usuário como número inteiro (int).



            if opcao == 1:

                resultado = num1 + num2

                print("Resultado da soma:", resultado)

            elif opcao == 2:

                resultado = num1 - num2

                print("Resultado da subtração:", resultado)

            elif opcao == 3:

                resultado = num1 * num2

                print("Resultado da multiplicação:", resultado)

            elif opcao == 4:

                if num2 == 0:

                    print("Divisão por zero não é permitida.")

                else:

                    resultado = num1 / num2

                    print("Resultado da divisão:", resultado)

Executa a operação correspondente à escolha. Na divisão, há uma verificação especial: se num2 for zero, exibe um aviso em vez de causar um erro.



            elif opcao == 5:

                print("Saindo...")

                break

            else:

                print("Opção inválida. Tente novamente.")

A opção 5 encerra o loop com break. Qualquer outro número exibe uma mensagem de opção inválida e o loop recomeça.



        except ValueError:

            print("Entrada inválida. Por favor, digite apenas números.")

Se o usuário digitar uma letra ou texto onde era esperado um número, o except ValueError captura o erro e exibe uma mensagem amigável — sem travar o programa.



calculadora()

Chama a função para iniciar o programa.

