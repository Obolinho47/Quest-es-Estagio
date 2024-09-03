1)indice = 13
Soma = 0
k = 0
while k<indice:
  Soma = Soma+k
  k = k+1
print(Soma)
#Saida = 78
----------------------------------------
def fibo(numero):
    a, b = 0, 1
    if numero == a or numero == b:
        return True
    while b < numero:
        a, b = b, a + b
    return numero == b

Numero= int(input("Informe um número : "))
if fibo(Numero):
    print(f"O número {Numero} pertence à sequência de Fibonacci.")
else:
    print(f"O número {Numero} não pertence à sequência de Fibonacci.")
-------------------------------------------
import json

with open('dados.json') as f:
    faturamento = json.load(f)

faturamento_filtrado = [dia['valor'] for dia in faturamento if dia['valor'] > 0]

menor = min(faturamento_filtrado)
maior = max(faturamento_filtrado)
media_mensal = sum(faturamento_filtrado) / len(faturamento_filtrado)
dias = len([valor for valor in faturamento_filtrado if valor > media_mensal])

print(f"Menor valor de faturamento: R$ {menor:.2f}")
print(f"Maior valor de faturamento: R$ {maior:.2f}")
print(f"Número de dias com faturamento acima da média mensal: {dias}")
-----------------------------------------------------------------------------------------
sp = 67836.43
rj = 36678.66
mg = 29229.88
es = 27165.48
outros = 19849.53

total = sp + rj + mg + es + outros

percentual_sp = (sp / total) * 100
percentual_rj = (rj / total) * 100
percentual_mg = (mg / total) * 100
percentual_es = (es / total) * 100
percentual_outros = (outros / total) * 100

print(f"SP: {percentual_sp:.2f}%")
print(f"RJ: {percentual_rj:.2f}%")
print(f"MG: {percentual_mg:.2f}%")
print(f"ES: {percentual_es:.2f}%")
print(f"Outros: {percentual_outros:.2f}%")
-----------------------------------------------------------------------------------------
entrada = input("Informe uma string: ")

reversão = ""
for i in range(len(entrada) - 1, -1, -1):
    reversão += entrada[i]

print(f"String invertida: {reversão}")
