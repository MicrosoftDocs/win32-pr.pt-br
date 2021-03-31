---
description: As colunas armazenadas no índice de conteúdo podem ter vários valores e as colunas com múltiplos valores podem ser comparadas usando o predicado de comparação de matriz.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Comparações de vários valores (matriz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646868"
---
# <a name="multi-valued-array-comparisons"></a>Comparações de vários valores (matriz)

As colunas armazenadas no índice de conteúdo podem ter vários valores e as colunas com múltiplos valores podem ser comparadas usando o predicado de comparação de matriz.

O predicado de comparação de matriz tem a seguinte sintaxe:


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Um erro será retornado se a referência de coluna não for uma coluna com valores de multivalor. O tipo de dados da coluna deve ser compatível com os elementos da lista de comparação. Se necessário, a referência de coluna pode ser [convertida](-search-sql-castingdatacolumntype.md) como outro tipo de dados.

O operador de comparação ( \_ op comp) pode ser qualquer um dos operadores de comparação normais. Em uma comparação de vários valores, os operadores de comparação têm significados um pouco diferentes dependendo se um quantificador é usado. Quantificadores identificam se uma comparação deve ser feita em relação a todos ou a alguns dos valores na lista de comparação. As funções dos operadores de comparação são dadas nas tabelas que descrevem cada quantificador (todos e alguns) posteriormente neste documento.

O valor após o operador especifica um valor literal único que é comparado com todos os elementos da coluna com valores de multivalor. Se qualquer elemento corresponder ao valor, o predicado será true.

A lista de comparação especifica uma matriz de valores literais que são comparados com a coluna com várias valores. A sintaxe da lista de comparação é a seguinte:


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Lembre-se da sintaxe da lista de comparação. O grupo de literais que compõem a lista de comparação deve estar entre colchetes. Não coloque elementos individuais da lista de comparação por colchetes. Portanto, a matriz 1 \[ \] e a matriz \[ 1, 2, 3 \] são válidas, mas a matriz \[ 1 \[ , 2 \] \[ , 3 \] \] não é.

 

O método usado para determinar se a comparação de valores multivalor retorna true ou false é especificado pelo quantificador opcional. As seções a seguir descrevem cada quantificador e como cada operador de comparação funciona quando o quantificador é usado.

## <a name="absent-quantifier"></a>Quantificador ausente

Se nenhum quantificador for especificado, cada elemento no lado esquerdo da comparação será comparado ao elemento na mesma posição no lado direito. A comparação começa com o primeiro elemento nas matrizes e progride pelo último elemento. Se todos os elementos no lado esquerdo forem equivalentes aos elementos correspondentes no lado direito, o número de elementos da matriz será usado para determinar qual matriz é maior.

A tabela a seguir mostra a operação dos operadores de comparação quando nenhum quantificador é especificado e fornece uma breve descrição de cada um.



| Operador       | Descrição                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Equals ' retorna true quando cada elemento do lado esquerdo tem o mesmo valor que o elemento do lado direito correspondente e ambas as matrizes têm o mesmo número de elementos.                                                                                                                                                                                                                     |
| ! = ou <> | ' Not igual a ' retorna true quando um ou mais elementos do lado esquerdo têm valores que diferem dos elementos correspondentes do lado direito, ou quando as matrizes do lado esquerdo e do lado direito não têm o mesmo número de elementos.                                                                                                                                                              |
| >           | ' Maior que ' retorna true quando o valor de cada elemento do lado esquerdo é maior que o valor do elemento do lado direito correspondente. Se todos os valores de elemento do lado esquerdo corresponderem exatamente aos elementos correspondentes do lado direito e a matriz do lado esquerdo tiver mais elementos do que a matriz do lado direito, ' maior que ' retornará true.                                                     |
| >=          | ' Maior que ou igual a ' retorna true quando o valor de cada elemento do lado esquerdo é maior ou igual ao valor do elemento do lado direito correspondente. Se todos os valores de elemento do lado esquerdo forem iguais ou maiores que os elementos correspondentes do lado direito, e a matriz do lado esquerdo tiver os mesmos ou mais elementos do que a matriz do lado direito, ' maior que ' retornará true. |
| <           | ' Less than ' retorna true quando o valor de cada elemento do lado esquerdo é menor que o valor do elemento do lado direito correspondente. ' Menor que ' também retorna true quando o lado esquerdo tem menos elementos do que o lado direito.                                                                                                                                                  |
| <=          | ' Menor que ou igual a ' retorna true quando o valor de cada elemento do lado esquerdo é menor ou igual ao valor do elemento do lado direito correspondente. Se todos os valores de elemento do lado esquerdo forem iguais ou menores que os elementos correspondentes do lado direito e a matriz do lado esquerdo tiver os mesmos elementos ou menos do que a matriz do lado direito, ' maior que ' retornará true.         |



 

## <a name="all-quantifier"></a>Todos os quantificadores

O quantificador ALL especifica que cada elemento no lado esquerdo é comparado a todos os elementos do lado direito. Para retornar true, a comparação deve ser verdadeira para cada elemento no lado esquerdo quando comparado a todos os elementos do lado direito. O número de elementos nos lados da matriz esquerda e direita não tem nenhum efeito sobre o resultado.

A tabela a seguir mostra como cada operador de comparação funciona com o quantificador ALL.



| Operador       | Descrição                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Equals ' retorna true quando cada valor de elemento do lado esquerdo é igual a todos os valores de elemento do lado direito.                              |
| ! = ou <> | ' Diferente de ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é diferente de qualquer um dos valores de elemento do lado direito. |
| >           | ' Maior que ' retorna true quando cada valor de elemento do lado esquerdo é maior que cada valor de elemento do lado direito.                         |
| >=          | ' Maior que ou igual a ' retorna true quando cada valor de elemento do lado esquerdo é maior ou igual a cada valor de elemento do lado direito. |
| <           | ' Less than ' retorna true quando cada valor de elemento do lado esquerdo é menor que todo o valor do elemento do lado direito.                               |
| <=          | ' Menor que ou igual a ' retorna true quando cada valor de elemento do lado esquerdo é menor ou igual a cada valor de elemento do lado direito.       |



 

## <a name="some-or-any-quantifier"></a>ALGUM quantificador (ou qualquer)

O quantificador e o quantificador ANY podem ser usados de forma intercambiável. Como o quantificador ALL, o quantificador especifica que cada elemento no lado esquerdo é comparado com todos os elementos do lado direito. Para retornar true, a comparação deve ser verdadeira para pelo menos um dos elementos no lado esquerdo quando comparado a qualquer elemento no lado direito. O número de elementos nas matrizes esquerda e direita não tem nenhum efeito sobre o resultado.

A tabela a seguir mostra como cada operador de comparação funciona com um quantificador.



| Operador       | Descrição                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | ' Equals ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é o mesmo que qualquer um dos valores de elemento do lado direito.                                  |
| ! = ou <> | ' Not igual a ' retorna true quando nenhum dos valores de elemento do lado esquerdo é o mesmo que qualquer um dos valores de elemento do lado direito.                                      |
| >           | ' Maior que ' retorna true quando pelo menos um dos valores de elementos do lado esquerdo é maior que qualquer um dos valores de elemento do lado direito.                         |
| >=          | ' Maior que ou igual a ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é maior ou igual a qualquer um dos valores de elemento do lado direito. |
| <           | ' Less than ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é menor que qualquer um dos valores de elemento do lado direito.                               |
| <=          | ' Menor que ou igual a ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é menor ou igual a qualquer um dos valores de elemento do lado direito.       |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir verifica se os documentos estão nas categorias "Finance" ou "Planning":


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



Todas as comparações a seguir são avaliadas como true. Lembre-se de que, em uso real, a sintaxe da consulta de pesquisa exige que o lado esquerdo seja uma propriedade, não um valor literal.


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado LIKE](-search-sql-like.md)
</dt> <dt>

[Comparação de valor literal](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Predicado nulo](-search-sql-null.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



