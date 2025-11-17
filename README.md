 atividade_-poo- Relatório Técnico – Programação Orientada a Objetos (POO)

 Introdução

A **Programação Orientada a Objetos (POO)** é um paradigma de programação que organiza o código em **objetos**, que representam entidades do mundo real e possuem **atributos** (características) e **métodos** (comportamentos). Esse modelo ajuda a tornar o software mais organizado, reutilizável e fácil de manter.

A POO surgiu como uma resposta às dificuldades encontradas em paradigmas anteriores, como a programação estruturada, que se tornava complexa e difícil de manter conforme os programas cresciam. Com a POO, o foco deixa de ser apenas funções e passa a ser a modelagem de objetos que interagem entre si, aproximando o código do modo como pensamos o mundo real.

---

 Os Quatro Pilares da POO

 1. **Abstração**

A abstração consiste em representar conceitos complexos da forma mais simples possível, mostrando ao usuário apenas o que é necessário. Em vez de expor todos os detalhes internos, criamos modelos claros e compreensíveis.

 Exemplo (Python)

```python
class Carro:
    def __init__(self, modelo, ano):
        self.modelo = modelo
        self.ano = ano

    def ligar(self):
        print("O carro está ligando...")

carro = Carro("Onix", 2020)
carro.ligar()
```

---

 2. **Encapsulamento**

O encapsulamento protege os dados internos de uma classe, permitindo acessar e modificar informações apenas através de métodos próprios. Isso evita alterações indevidas e mantém o controle do funcionamento interno.

 Exemplo (Python)

```python
class ContaBancaria:
    def __init__(self, saldo):
        self.__saldo = saldo  # atributo privado

    def depositar(self, valor):
        self.__saldo += valor

    def ver_saldo(self):
        return self.__saldo

conta = ContaBancaria(100)
conta.depositar(50)
print(conta.ver_saldo())  # 150
```

---

 3. **Herança**

Herança permite que uma classe (classe filha) reutilize atributos e métodos de outra classe (classe pai). Isso evita repetição de código e facilita a extensibilidade.

 Exemplo (Python)

```python
class Animal:
    def comer(self):
        print("O animal está comendo.")

class Cachorro(Animal):
    def latir(self):
        print("Au au!")

cachorro = Cachorro()
cachorro.comer()  # herdado\ ncachorro.latir()
```

---

 4. **Polimorfismo**

Polimorfismo permite que métodos com o mesmo nome se comportem de maneiras diferentes dependendo do objeto que os utiliza.

 Exemplo (Python)

```python
class Animal:
    def fazer_som(self):
        print("O animal faz um som.")

class Gato(Animal):
    def fazer_som(self):
        print("Miau!")

class Vaca(Animal):
    def fazer_som(self):
        print("Muuu!")

for animal in [Animal(), Gato(), Vaca()]:
    animal.fazer_som()
``
