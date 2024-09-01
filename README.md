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
[
    {"dia": 1, "valor": 22174.1664},
    {"dia": 2, "valor": 24537.6698},
    {"dia": 3, "valor": 26139.6134},
    {"dia": 4, "valor": 0.0},
    {"dia": 5, "valor": 0.0},
    {"dia": 6, "valor": 26742.6612},
    {"dia": 7, "valor": 0.0},
    {"dia": 8, "valor": 42889.2258},
    {"dia": 9, "valor": 46251.174},
    {"dia": 10, "valor": 11191.4722},
    {"dia": 11, "valor": 0.0},
    {"dia": 12, "valor": 0.0},
    {"dia": 13, "valor": 3847.4823},
    {"dia": 14, "valor": 373.7838},
    {"dia": 15, "valor": 2659.7563},
    {"dia": 16, "valor": 48924.2448},
    {"dia": 17, "valor": 18419.2614},
    {"dia": 18, "valor": 0.0},
    {"dia": 19, "valor": 0.0},
    {"dia": 20, "valor": 35240.1826},
    {"dia": 21, "valor": 43829.1667},
    {"dia": 22, "valor": 18235.6852},
    {"dia": 23, "valor": 4355.0662},
    {"dia": 24, "valor": 13327.1025},
    {"dia": 25, "valor": 0.0},
    {"dia": 26, "valor": 0.0},
    {"dia": 27, "valor": 25681.8318},
    {"dia": 28, "valor": 1718.1221},
    {"dia": 29, "valor": 13220.495},
    {"dia": 30, "valor": 8414.61}
]
GERADO PRO IA OS DADOS
import json

with open('faturamento.json') as f:
    faturamento = json.load(f)

faturamento_filtrado = [dia['valor'] for dia in faturamento if dia['valor'] > 0]

menor_valor = min(faturamento_filtrado)
maior_valor = max(faturamento_filtrado)
media_mensal = sum(faturamento_filtrado) / len(faturamento_filtrado)
dias_acima_da_media = len([valor for valor in faturamento_filtrado if valor > media_mensal])

print(f"Menor valor de faturamento: R$ {menor_valor:.2f}")
print(f"Maior valor de faturamento: R$ {maior_valor:.2f}")
print(f"Número de dias com faturamento acima da média mensal: {dias_acima_da_media}")
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
