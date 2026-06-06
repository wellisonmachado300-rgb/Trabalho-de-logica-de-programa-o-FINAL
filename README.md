Tipos de Dados 
Questão 1 – Cadastro Simples (0,2 ponto) 
Crie um programa que armazene: 
• nome;  
• idade;  
• altura. 
Resposta 0.1 : 

# Solicita o nome do usuário .O resultado sera salvo como uma string(texto)
nome = input("digite seu nome:")

#Solicita a idade . Nota: como não foi convertida para "int" , ela sera tratada como texto . 
idade = input("digite sua idade: ")

#Solicita a altura . nota : como não foi convertido para 'float' , ela sera tratada como texto . 
altura = input("digite sua altura: " )


#Exibe as informações na tela utilizando f-strings para interpolar as variáveis . 
print(f"nome inserido:{nome}")
print(f"idade inserida :{idade}")
print(f"altura inserida :{altura}") 

—------------------------------------------------------------------------------------------------------------------------

Expressões, Operadores e Tabela Verdade 
Questão 2 – Operações Matemáticas (0,2 ponto) 
Crie um programa que leia dois números e realize: 
• soma;  
• subtração;  
• multiplicação;  
• divisão.  
Resposta 0.2 : 

# entrada de dados
valor1 = float(input("digite o primeiro valor: "))
valor2 = float(input("digite o segundo valor: "))

# area de calculos
soma = valor1 + valor2
subtracao = valor1 - valor2

# regra matematica importante
if valor2 != 0:
    divisao = valor1 / valor2
else:
    divisao = "nao e possivel dividir por zero "

multiplicaçao = valor1 * valor2

# exibiçao de resultados obtidos
print(f"\nsoma é {soma}")
print(f"\nsubtracao é {subtracao}")
print(f"\ndivisao é {divisao}")
print(f'\nmultiplicaçao é {multiplicaçao}')

 
—------------------------------------------------------------------------------------------------------------------------






Questão 3 – Verificação de Aprovação (0,3 ponto) 
Crie um programa que utilize operadores lógicos (and, or, not) para verificar se um 
aluno foi aprovado. 
Condições: 
• média maior ou igual a 7;  
• frequência maior ou igual a 75%

Resposta:   

# passo 1: coleta de dados do aluno
nota1 = float(input("digite a primeira nota :"))
nota2 = float(input("digite a segunda nota : "))
frequencia = int(input("digite a frequencia do aluno (em %): "))

# passo 2 : calculo da media
media = (nota1 + nota2) / 2

# passo 3 : verificaçao das condiçoes usando operadores logicos .
# aprovado : média >= 7 E frequencia >= 75
aprovado = (media >= 7 ) and (frequencia >= 75 )

#reprovado por falta : freqeuncia < 75
# (exemplo de uso do "not" e "or" para fins didaticos no relatorio )
reprovado_por_falta = not (frequencia >= 75 )

# passo 4 : Exibiçao do resultado
print("-" *  30)
print(f"media final : {media : .1f}")
print("-" * 30 )

if aprovado:
    print("situação: ALUNO APROVADO !!! ")
elif reprovado_por_falta or (media < 7): 
    print("Situação : ALUNO REPROVADO ")


 

 
. 

—------------------------------------------------------------------------------------------------------------------------




Comandos de Entrada e Saída 
Questão 4 – Conversor de Temperatura (0,3 ponto) 
Crie um programa que converta temperatura de Celsius para Fahrenheit.
Utilize a fórmula: 
�
� =9𝐶
5
+32

Resposta: 

# conversão de temperatura :
# solicita a temperatura em Celsius ao usuário
Celsius = float(input("digite a temperatura em Celsius :"))

# Aplica a fórmula de convesão para Fahrenheit
Fahrenheit = ((9 * Celsius) / 5) + 32

# Exibe o resultado obtido
print(f"A temoeratura em fahrenheit é : {Fahrenheit:.2f}°F")



 



—------------------------------------------------------------------------------------------------------------------------
Estruturas de Decisão 
Questão 5 – Número Positivo ou Negativo (0,3 ponto) 
Crie um programa que leia um número e informe se ele é: 
• positivo;  
• negativo;  
• ou zero.  
Resposta: 
#Lê o número digitado pelo usuario (pode ser inteiro ou com vírgula )
numero = float(input("Digite um número : "))

# Estrutura de decisão para verificar se é positivo , negativo ou zero 
if numero > 0: 
    print("O numero é positivo. ")
elif numero < 0: 
    print("O numero é negativo .")
else: 
    print("O numero é zero . ")








—------------------------------------------------------------------------------------------------------------------------
Questão 6 – Média do Aluno (0,3 ponto) Crie um programa que leia duas notas e informe: 
• aprovado;  
• recuperação;  
• reprovado.  
Considere: 
• média ≥ 7 → aprovado;  
• média entre 5 e 6,9 → recuperação;  
• média < 5 → reprovado.  

Resposta: 

# passo 1: coleta de dados do aluno
nota1 = float(input("digite a primeira nota :"))
nota2 = float(input("digite a segunda nota : "))

# Calcula a média aritmética
media = (nota1 + nota1) / 2

# Verifica a situação do aluno com base na média
if media  >= 7:
    print("Parabens aprovado !!! ")
elif media >= 5 and media < 7 :
    print(" Você deve fazer a recuperação")
else:
    print("reprovado !! ") 



—------------------------------------------------------------------------------------------------------------------------
Estruturas de Repetição 
Questão 7 – Tabuada com For (0,4 ponto) 
Crie um programa que exiba a tabuada de um número informado pelo usuário 
utilizando for. 
Resposta: 

# Solicita o número ao usuário e o converte para inteiro
numero = int(input("Digite um número para ver a sua tabuada: "))

print(f"\n--- Tabuada do {numero} ---")

# O range(1, 11) vai de 1 até 10
for i in range(1, 11):
    resultado = numero * i
    print(f"{numero} x {i:2} = {resultado}")
 

 


—------------------------------------------------------------------------------------------------------------------------






Listas 
Questão 8 – Lista de Compras (0,3 ponto) 
Crie uma lista contendo 5 itens de supermercado informados pelo usuário e exiba 
todos os itens da lista. 



lista_de_compras = []

# 2. Exibe a mensagem inicial para o usuário.
print("Quais são os 5 itens da sua lista de compras?")

# 3. Loop que vai rodar exatamente 5 vezes (de 0 a 4).
# Mudamos o nome da variável do loop para 'i' para não confundir com a lista.
for i in range(5):
    # 4. Entrada de dados corrigida.
    #  O caractere 'f' deve ficar FORA das aspas: f"Texto {variavel}"
    item = input(f"O {i + 1}º da sua lista: ")

    # 5. Adiciona o item digitado ao final da lista.
    lista_de_compras.append(item)

# 6. Linha em branco (boa prática estrutural).
print("\nAqui está sua lista de compras:")

# 7. Loop para ler e exibir cada item adicionado à lista.
for item in lista_de_compras:
    # Exibe o item com um hífen na frente.
    print(f"- {item}")

 

 

—------------------------------------------------------------------------------------------------------------------------

Dicionários 
Questão 9 – Cadastro de Aluno (0,3 ponto) 
Crie um dicionário contendo: 
• nome do aluno;  
• idade;  
• curso.  
Depois exiba todas as informações armazenadas no dicionário. 

Resposta: 

#Primeiro é preciso trazer as informações do aluno:
aluno1 = {
    "Nome": "wellison machado ",
    "Idade": 20,
    "Curso": "Engenharia Civil"
}
#Depois é preciso mostrar as informações:
print("Informações do Aluno:")
for chave, valor in aluno1.items():
    print(f"- {chave.capitalize()}: {valor}")

 

—------------------------------------------------------------------------------------------------------------------------

Vetores 
Questão 10 – Vetor de Números (0,4 ponto) 
Crie um vetor (lista) com 5 números inteiros informados pelo usuário e exiba: 
• todos os números;  
• maior número;  
• menor número.  


Resposta: 

# Cria uma lista vazia para armazenar os números que o usuário vai digitar
numeros = []

# Exibe uma mensagem inicial orientando o usuário
print("Digite 5 números inteiros")

# Cria um laço de repetição (loop) que vai rodar exatamente 5 vezes
# A variável 'n' começa em 0 e vai até 4 (0, 1, 2, 3, 4)
for n in range(5):
    # Pede o número ao usuário. 
    # O 'f' antes das aspas permite usar {n + 1} para mostrar "1° número", "2° número", etc.
    # O 'int()' converte o texto que o usuário digitou em um número inteiro
    valor = int(input(f"Digite o {n + 1}° número: "))
    
    # Pega o número guardado na variável 'valor' e o adiciona no final da lista 'numeros'
    numeros.append(valor)

# Exibe um cabeçalho para separar a entrada de dados dos resultados
print("\n RESPOSTAS")

# Exibe a lista completa com os 5 números que foram armazenados
print(f"Números digitados: {numeros}")

# A função max() analisa a lista e retorna o maior valor encontrado nela
print(f"O maior número: {max(numeros)}")

# A função min() analisa a lista e retorna o menor valor encontrado nela
print(f"O menor número: {min(numeros)}")



