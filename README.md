# CalculadoraOpcao
Projeto Curso Proz Desafio Calculadora Opção de Soma
def calculadora():
    while True:
        print("Operações disponíveis:")
        print("1: Soma")
        print("2: Subtração")
        print("3: Multiplicação")
        print("4: Divisão")
        print("0: Sair")

        opcao = input("Digite o número para a operação desejada: ")

        if opcao == '0':
            print("Saindo da calculadora. Até a próxima!")
            break
        elif opcao in ('1', '2', '3', '4'):
            try:
                num1 = float(input("Digite o primeiro valor: "))
                num2 = float(input("Digite o segundo valor: "))
            except ValueError:
                print("Por favor, insira números válidos.")
                continue

            if opcao == '1':
                resultado = num1 + num2
                print("Resultado da soma: ", resultado)
            elif opcao == '2':
                resultado = num1 - num2
                print("Resultado da subtração: ", resultado)
            elif opcao == '3':
                resultado = num1 * num2
                print("Resultado da multiplicação: ", resultado)
            elif opcao == '4':
                if num2 != 0:
                    resultado = num1 / num2
                    print("Resultado da divisão: ", resultado)
                else:
                    print("Não é possível dividir por zero. Tente novamente.")
                    continue
        else:
            print("Essa opção não existe. Por favor, escolha uma opção válida.")

if __name__ == "__main__":
    calculadora()
