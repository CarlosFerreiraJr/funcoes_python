<b>Exemplos de funções em Python<br>
Conhecimento obtido através do curso de Ciência de Dados da UniCarioca - Prof. Sérgio Monteiro</b>

## Função que obtém o menor número de uma lista
Observações:
1. Os dados da lista são inseridos pelo usuário através da função <b>input</b>
2. Em Python, a função, a estrutura de repetição (while ou for) e a estrutura condicional Se (if) <br>
   são finalizados pelo simples fato de estarem indentadas

```
def encontrar_minimo(lista):
    minimo = int(lista[0])
    for elem in lista:
        if (int(elem) < minimo):
            minimo = int(elem)
    return minimo


numero = 0
s = ''
contador=0
while (numero != -1):
      numero = int(input("Entre com um número: "))
      s = s + str(numero) + ','

s = s[0:len(s)-4]
print(s)
lista = s.split(',')
print(lista)
menor = encontrar_minimo(lista)
print("O menor elemento da lista é:[{}]".format(menor))
```

## Função que obtém o menor número de uma lista e informa a quantidade de números pares e ímpares
Observações:
1. Os dados da lista são inseridos pelo usuário através da função <b>input</b>
2. Em Python, a função, a estrutura de repetição (while ou for) e a estrutura condicional Se (if) <br>
   são finalizados pelo simples fato de estarem indentadas
```
def encontrar_minimo(lista):
    minimo = int(lista[0])
    for elem in lista:
        if (int(elem) < minimo):
            minimo = int(elem)
    return minimo

def ehPar(n):
  r = (n%2==0)
  return r

numero = 0
s = ''
contador = 0
qtdPar = 0
qtdImpar = 0

while (numero != -1):
    try:
        numero = int(input("Digite um número: "))
        s = s + str(numero) + ','

        if (numero != -1 ):
            if (ehPar(numero)):
                qtdPar = qtdPar + 1
            else:
                qtdImpar = qtdImpar + 1

    except ValueError:
        print("Entre com um número válido.")


s = s[0:len(s)-4]
lista = s.split(',')
menor = encontrar_minimo(lista)
print("O menor elemento da lista é:[{}]".format(menor))
print("Quantidade de números pares: " + str(qtdPar))
print("Quantidade de números ímpares: " + str(qtdImpar))
```
