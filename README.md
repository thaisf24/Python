# Python
Thais Fernandes RA:201310430

1 Defina a função soma_nat que recebe como argumento um número natural n e devolve a soma de todos os números naturais até n.

In [4]:def r_soma_nat(n):
               if n == 1:
                   return 1
               else:
                   return n + r_soma_nat(n-1)
       print(r_soma_nat(5))
       15

2 Defina a função div que recebe como argumentos dois números naturais m e n e devolve o resultado da divisão inteira de m por n. Neste exercício você não pode recorrer às operações aritméticas de multiplicação, divisão e resto da divisão inteira.

In [3]:def r_div(m,n):
               if m < n:
                   return 0
               else:
                   return 1 + r_div(m-n,n)
       print(r_div(7,2))
       3

3 Defina a função prim_alg que recebe como argumento um número natural e devolve o primeiro algarismo (o mais significativo) na representação decimal de n.

In [4]:def prim_alg(n):
           return print(n[0])
       prim_alg("5649")
       prim_alg("7")
       5
       7

4 Defina a função prod_lista que recebe como argumento uma lista de inteiros e devolve o produto dos seus elementos.

In [1]:def prod_lista(lista):
           return lista[len(lista) - 1] * prod_lista(lista[:-1]) if len(lista) > 0 else 1
       print(prod_lista([1,2,3,4,5,6]))
       720

5 Defina a função contem_parQ que recebe como argumento uma lista de números inteiros w e devolve True se w contém um número par e False em caso contrário.

In [19]:def r_contem_parQ(w):
                if len(w) == 0:
                     return False
                else:
                    a = w.pop()
                    if a%2 == 0:
                        return True
                    else:
                        return r_contem_parQ(w)
        print(r_contem_parQ([2,3,1,2,3,4]))
        print(r_contem_parQ([1,3,5,7]))
        True
        False

6 Defina a função todos_imparesQ que recebe como argumento uma lista de números inteiros w e devolve True se w contém apenas números ímpares e False em caso contrário.

In [3]:def r_todos_imparesQ(w):
             if len(w) == 0:
                 return True
             else:
                 a = w.pop()
                 if a %2 == 0:
                      return False
                 else:
                      return r_todos_imparesQ(w)
       print(r_todos_imparesQ([2,3,1,2,3,4]))
       print(r_todos_imparesQ([1,3,5,7]))
       False
       True
