from math import sqrt
from math import pi
from decimal import Decimal, getcontext
getcontext().prec = 20
#Valores usados: 10 20 100

def Gera_x(n):
  if n == 1:
    return (Decimal(1/Decimal(sqrt(2))))
  x = Decimal(Decimal(0.5)*(Decimal(sqrt(Decimal(Gera_x(n-1))))+Decimal(1)/Decimal(sqrt(Decimal(Gera_x(n-1))))))
  return x

def Gera_y(n):
  if n == 1:
    return (0)
  y = Decimal((Gera_y(n-1)*Decimal(sqrt(Gera_x(n-1)))+1/Decimal(sqrt(Gera_x(n-1))))/(Gera_y(n-1)+1))
  return y

def Gera_π(n):
  if n == 1:
    return (2)
  π = Decimal((Gera_x(n-1)+1)*Gera_π(n-1)/(Gera_y(n-1)+1))
  return π

print('Bem-vindo ao programa Gerador do Número π.\nDigite um número natural para determinar a precisão.\nQuanto maior o número, maior a precisão.\nPara encerrar o programa, digite "fim".')

while True:
  try:
    n = input("\nDigite o valor:")
    if n == 'fim':
      print('Programa encerrado.')
      break
    elif int(n) > 0:
      n = int(n)
      print("π:", Decimal(Gera_π(n)))
      print("π_calculado - π_real :", abs(Decimal(Gera_π(n)) - Decimal(pi)))
    else:
      print('Digite um número natural maior que zero.')
  except ValueError:
    print('Digite um número natural maior que zero.')
