# Lista Estrutura de Decisão- Python 
Python exercicios.

#-1
##faça um programa que peça dois numeros e imprima o maior deles.

n1 = float(input("digite um número: "))

n2 = float(input("digite um numero: "))

if n1 > n2: print("O maior numero é ", n1)

elif n2 > n1: print("O maior numero é", n2)

else: print("Os numeros são iguais")

_____________________________________________________________________________________________
#-2
#Faça um Programa que peça um valor e mostre na tela se o valor é positivo ou negativo.

valor = float(input("Digite um valor: "))

if valor < 0: print("O valor é negativo")
else: print("O valor é positivo")

_____________________________________________________________________________________________
#-3
#Faça um programa que verifique se uma letra diigtada é "F" ou "M". Conforme a letra escrever: F- Femenino, M- Masculino, Sexo inválido.

sexo = input("Digite seu sexo [F, M]: ")

if sexo == 'F' or sexo == 'f': print("Seu sexo é Femenino")
elif sexo == 'M' or sexo == 'm': print("Seu sexo é Masculino")
else: print("Sexo Inválido")

______________________________________________________________________________________________
#-4
#Faça um Programa que verifique se uma letra digitada é vogal ou consoante.

letra = input("Digite uma letra: ")
vogais = ['a', 'e', 'i', 'o', 'u']

if letra in vocais: print('VOCAL')
else: print('CONSONANTE')

______________________________________________________________________________________________
#-5
#Faça um programa para a leitura de duas notas parciais de um aluno.
#O programa deve calcular a média alcançada por aluno e apresentar:

#A mensagem "Aprovado", se a média alcançada for maior ou igual a sete;
#A mensagem "Reprovado", se a média for menor do que sete;
#A mensagem "Aprovado com Distinção", se a média for igual a dez.


nota1 = float(input("Digite a primeira nota: "))
nota2 = float(input("Digite a segunda nota: "))

media = (nota1 + nota2) / 2

if media >= 7 and media < 10: print("APROVADO")
elif media < 7: print("REPROVADO")
else: print("APROVADO com DISTINÇÃO")

_____________________________________________________________________________________________
#-6
#Faça um Programa que leia três números e mostre o maior deles.

valor1 = float(input("Digite o primeiro valor: "))
valor2 = float(input("Digite o segundo valor: "))
valor3 = float(input("Digite o terceiro valor: "))

valores = [valor1, valor2, valor3]

print(f'O maior número é {max(valores)}')

_____________________________________________________________________________________________
#-7
#Faça um Programa que leia três números e mostre o maior e o menor deles.

valor1 = float(input("Digite o primeiro valor: "))
valor2 = float(input("Digite o segundo valor: "))
valor3 = float(input("Digite o terceiro valor: "))

lista = [valor1, valor2, valor3]

print("Menor valor: ", min(lista), "\nMaior valor: ", max(lista))


_____________________________________________________________________________________________
#-8
#Faça um programa que pergunte o preço de três produtos e informe qual produto você deve comprar, sabendo que a decisão é sempre pelo mais barato.

preco1 = float(input("Digite o primeiro preço: "))
preco2 = float(input("Digite o segundo preço: "))
preco3 = float(input("Digite o terceiro preço: "))

lista = [preco1, preco2, preco3]

print("O produto que deve ser comprado é o que custa ", min(lista))


_____________________________________________________________________________________________
#-9
#Faça um Programa que leia três números e mostre-os em ordem decrescente.

n1 = float(input("Digite o primeiro número: "))
n2 = float(input("Digite o segundo número: "))
n3 = float(input("Digite o terceiro número: "))

lista = [n1, n2, n3]

lista.sort(key=float, reverse=True)

print("decrescente: ", lista)


_____________________________________________________________________________________________
#-10
#Faça um Programa que pergunte em que turno você estuda. Peça para digitar M-matutino ou V-Vespertino ou N- Noturno. Imprima a mensagem "Bom Dia!", "Boa Tarde!" ou "Boa Noite!" ou "Valor Inválido!", conforme o caso.


horario = input("Digite [M, V, N]: ").upper()

if horario == 'M': print("Bom Dia")
elif horario == 'V': print("Boa Tarde")
elif horario == 'N': print("Boa Noite")
else: print("Valor Inválido")


_____________________________________________________________________________________________
#-11
#As Organizações Tabajara resolveram dar um aumento de salário aos seus colaboradores e lhe contraram para desenvolver o programa que calculará os reajustes.
#Faça um programa que recebe o salário de um colaborador e o reajuste segundo o seguinte critério, baseado no salário atual:
#salários até R$ 280,00 (incluindo) : aumento de 20%
#salários entre R$ 280,00 e R$ 700,00 : aumento de 15%
#salários entre R$ 700,00 e R$ 1500,00 : aumento de 10%
#salários de R$ 1500,00 em diante : aumento de 5% Após o aumento ser realizado, informe na tela:
#o salário antes do reajuste;
#o percentual de aumento aplicado;
#o valor do aumento;
#o novo salário, após o aumento.

salario = float(input("Digite o seu salário: "))

valor_baixo = salario * 0.20
baixo = salario * 1.20
valor_medio = salario * 0.15
medio = salario * 1.15
valor_alto = salario * 0.10
alto = salario * 1.10
valor_altissimo = salario * 0.05
altissimo = salario * 1.05

print("Antes Reajuste: ", salario)

if salario <= 280: print("Aumento: 20%\nValor: ", valor_baixo, "\nFinal: ", baixo)
elif salario > 200 and salario <= 700: print("Aumento: 15%\nValor: ", valor_medio, "\nFinal: ", medio)
elif salario > 700 and salario <= 1500: print("Aumento: 10%\nValor: ", valor_alto, "\nFinal: ", alto)
else: print("Aumento: 5%\nValor: ", valor_altissimo, "\nFinal: ", altissimo)


_______________________________________________________________________________________________
#-12
#Faça um programa para o cálculo de uma folha de pagamento, sabendo que os descontos são do Imposto de Renda, que depende do salário bruto (conforme tabela abaixo) e 3% para o Sindicato e que o FGTS corresponde a 11% do Salário Bruto, mas não é descontado (é a empresa que deposita). O Salário Líquido corresponde ao Salário Bruto menos os descontos. O programa deverá pedir ao usuário o valor da sua hora e a quantidade de horas trabalhadas no mês.
#Desconto do IR:
#Salário Bruto até 900 (inclusive) - isento
#Salário Bruto até 1500 (inclusive) - desconto de 5%
#Salário Bruto até 2500 (inclusive) - desconto de 10%
#Salário Bruto acima de 2500 - desconto de 20% Imprima na tela as informações, dispostas conforme o exemplo abaixo. No exemplo o valor da hora é 5 e a quantidade de hora é 220.
#        Salário Bruto: (5 * 220)        : R$ 1100,00
#        (-) IR (5%)                     : R$   55,00  
#        (-) INSS ( 10%)                 : R$  110,00
#        FGTS (11%)                      : R$  121,00
#        Total de descontos              : R$  165,00
#        Salário Liquido                 : R$  935,00

valor_hora = float(input("Quanto você ganha por hora? "))
horas_mes = int(input("Quantas horas você trabalha no mês? "))
salario_bruto = horas_mes * valor_hora

ir1500 = salario_bruto * 0.05
ir2500 = salario_bruto * 0.10
irmaior = salario_bruto * 0.20

inss = salario_bruto * 0.10
fgts = salario_bruto * 0.11

print("salario Bruto: ", salario_bruto)

if salario_bruto <= 900:
    print("Seu salario permanecerá o mesmo")
else:
    print("INSS: ", inss, "\nFGTS: ", fgts)

if salario_bruto > 900 and salario_bruto <= 1500:
    salario_liquido = float(salario_bruto) - float(ir1500) - float(inss)
    print("IR: ", ir1500, "\nSalario Liquido: ", salario_liquido)

elif salario_bruto > 1500 and salario_bruto <= 2500:
    salario_liquido = float(salario_bruto) - float(ir2500) - float(inss)
    print("IR: ", ir2500, "\nSalario Liquido: ", salario_liquido)

else:
    salario_liquido = float(salario_bruto) - float(irmaior) - float(inss)
    print("IR: ", iralto, "\nSalario Liquido: ", salario_liquido)
______________________________________________________________________________________________
#-13
#Faça um Programa que leia um número e exiba o dia correspondente da semana. (1-Domingo, 2- Segunda, etc.), se digitar outro valor deve aparecer valor inválido.

dia = int(input("Digite um número de 1 a 7: "))

if dia == 1:
    print("Domingo")
elif dia == 2:
    print("Segunda")
elif dia == 3:
    print("Terça")
elif dia == 4:
    print("Quarta")
elif dia == 5:
    print("Quinta")
elif dia == 6:
    print("Sexta")
elif dia == 7:
    print("Sababo")
else:
    print("Valor Inválido")
    
______________________________________________________________________________________________
#-14
#Faça um programa que lê as duas notas parciais obtidas por um aluno numa disciplina ao longo de um semestre, e calcule a sua média. A atribuição de conceitos obedece à tabela abaixo:
#  Média de Aproveitamento  Conceito
#  Entre 9.0 e 10.0        A
#  Entre 7.5 e 9.0         B
#  Entre 6.0 e 7.5         C
#  Entre 4.0 e 6.0         D
#  Entre 4.0 e zero        E
#O algoritmo deve mostrar na tela as notas, a média, o conceito correspondente e a mensagem “APROVADO” se o conceito for A, B ou C ou “REPROVADO” se o conceito for D ou E.


nota1 = float(input("Digite a nota1: "))
nota2 = float(input("Digite a nota2: "))
media = (nota1 + nota2) / 2

if media >= 0 and media <= 4:
    print("E")
elif media > 4 and media <= 6:
    print("D")
elif media > 6 and media <= 7.5:
    print("C")
elif media > 7.5 and media <= 9:
    print("B")
else:
    print("A")
______________________________________________________________________________________________
#-15
#Faça um Programa que peça os 3 lados de um triângulo. O programa deverá informar se os valores podem ser um triângulo. Indique, caso os lados formem um triângulo, se o mesmo é: equilátero, isósceles ou escaleno.
#Dicas:
#Três lados formam um triângulo quando a soma de quaisquer dois lados for maior que o terceiro;
#Triângulo Equilátero: três lados iguais;
#Triângulo Isósceles: quaisquer dois lados iguais;
#Triângulo Escaleno: três lados diferentes;


lado1 = float(input("Lado 1: "))
lado2 = float(input("Lado 2: "))
lado3 = float(input("Lado 3: "))

if lado1 + lado2 > lado3 or lado1 + lado3 > lado2 or lado2 + lado3 > lado1:
    print("É UM TRINGULO")
    if lado1 == lado2 and lado1 == lado3:
        print("Equilatero")
    elif lado1 == lado2 or lado2 == lado3 or lado3 == lado1:
        print("Isóceles")
    else:
        print("Escaleno")
else:
    print("Não é um TRINGULO")







