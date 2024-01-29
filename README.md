# desafio_3343_beecrowd_attack_on_gasparini
# Resolução do desafio de programação do site BeeCrowd de nível 8 (+5.0 pontos)

# Desafio https://www.beecrowd.com.br/judge/pt/problems/view/3343

n1 = input().split()
titas, muralhas = n1
titas = int(titas)
muralhas = int(muralhas)
n2 = input()
n3 = input().split()
p,m,g = n3
p = int(p)
m = int(m)
g = int(g)
aux = muralhas
valor = 1
for i in range(len(n2)):
  if n2[i] == 'P':
    muralhas -= p
  elif n2[i] == 'M':
    muralhas -= m
  elif n2[i] == 'G':
    muralhas -= g
  if muralhas < 0:
    muralhas += aux
    valor += 1
print(str(valor))
