# Classe do nó da lista encadeada
class No:
    def __init__(self, dado):
        self.dado = dado
        self.proximo = None


# Classe da lista encadeada
class ListaEncadeada:
    def __init__(self):
        self.cabeca = None

    # Inserir no final da lista
    def inserir(self, dado):
        novo_no = No(dado)

        if self.cabeca is None:
            self.cabeca = novo_no
            return

        atual = self.cabeca
        while atual.proximo:
            atual = atual.proximo

        atual.proximo = novo_no

    # Mostrar a lista
    def mostrar(self):
        atual = self.cabeca
        while atual:
            print(atual.dado)
            atual = atual.proximo


# Criando a lista
lista_carnes = ListaEncadeada()

# 5 carnes mais consumidas no mundo
lista_carnes.inserir("Frango")
lista_carnes.inserir("Porco")
lista_carnes.inserir("Carne Bovina")
lista_carnes.inserir("Peixe")
lista_carnes.inserir("Cordeiro")

# Exibindo a lista
print("Lista de carnes mais consumidas:")
lista_carnes.mostrar()
