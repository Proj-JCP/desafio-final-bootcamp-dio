﻿# desafio-final-bootcamp-dio
class Jogador:
    def __init__(self, nome, idade, tipo):
        self.nome = nome
        self.idade = idade
        self.tipo = tipo

class Mago(Jogador):
    def __init__(self, nome, idade):
        super().__init__(nome, idade, "Mago")

class Guerreiro(Jogador):
    def __init__(self, nome, idade):
        super().__init__(nome, idade, "Guerreiro")

class Monja(Jogador):
    def __init__(self, nome, idade):
        super().__init__(nome, idade, "Monja")

class Ninja(Jogador):
    def __init__(self, nome, idade):
        super().__init__(nome, idade, "Ninja")

nome_jogador = input("Digite o nome do jogador: ")
idade_jogador = input("Digite a idade do jogador: ")
tipo_jogador = int(input("""Digite o tipo de seu jogador: 
                         1 - Mago, 
                         2 - Guerreiro, 
                         3 - Monje
                         4 - Ninja
                         Faça sua escolha: """))

jogador = None

if tipo_jogador == 1:
    jogador = Mago(nome_jogador, idade_jogador)
    print(f"""Nome do Jogador: {jogador.nome}, 
Idade do Jogador: {jogador.idade}, 
Tipo: {jogador.tipo}, 
Seu ataque é a Magia""")
    
elif tipo_jogador == 2:
    jogador = Guerreiro(nome_jogador, idade_jogador)
    print(f"""Nome do Jogador: {jogador.nome}, 
Idade do Jogador: {jogador.idade}, 
Tipo: {jogador.tipo}, 
No seu ataque voce usa a Espada""")
    
elif tipo_jogador == 3:
    jogador = Monja(nome_jogador, idade_jogador)
    print(f"""Nome do Jogador: {jogador.nome}, 
Idade do Jogador: {jogador.idade}, 
Tipo: {jogador.tipo}, 
No seu ataque voce usa a artes marciais""")
    
elif tipo_jogador == 4:
    jogador = Ninja(nome_jogador, idade_jogador)
    print(f"""Nome do Jogador: {jogador.nome}, 
Idade do Jogador: {jogador.idade}, 
Tipo: {jogador.tipo}, 
No seu ataque voce usa a shuriken""")
else:
    print("Tipo de jogador inválido")

