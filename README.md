dados = []
# Lista/Ela vai guardar as informações de cada pessoa (nome, filme e nota).
for i in range(3):
# Um laço de repetição que será executado 3 vezes (para 3 pessoas).
# A variável i vai valer 0, 1 e 2 (mas o i + 1 serve para mostrar 1, 2 e 3).
    nome = input(f"\nPessoa {i + 1} - Digite o nome: ")
    filme = input("Digite o nome do filme: ")

    while True:
        try:
            nota = float(input("Nota para o filme 0 a 10: "))
            if 0 <= nota <= 10:      
                break
            print("Nota inválida. Digite entre 0 e 10.")
        except:
            print("Digite um número válido.")
    dados.append([nome, filme, nota])
# Adiciona as informações dessa pessoa como uma sublista na lista dados Exemplo: ["Ana", "Titanic", 9.5]
print(" Dados Cadastrados")
for nome, filme, nota in dados:
    print(f"Nome: {nome}, Filme: {filme}, Nota: {nota}")
#Mostra os dados de cada pessoa formatados de forma clara.