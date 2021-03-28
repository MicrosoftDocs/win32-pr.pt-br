---
title: 'Função WavePrefixSum '
description: Retorna a soma de todos os valores nas pistas ativas com índices menores do que este.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- HLSL da função WavePrefixSum
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/31/2021
ms.locfileid: "104968258"
---
# <a name="waveprefixsum-function"></a>Função WavePrefixSum 

Retorna a soma de todos os valores nas pistas ativas com índices menores do que este.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Parâmetros

*value* 

O valor a ser somado.

## <a name="return-value"></a>Retornar valor

A soma dos valores.

## <a name="remarks"></a>Comentários

A ordem das operações nessa rotina não pode ser garantida. Portanto, efetivamente, o \[ \] sinalizador preciso é ignorado dentro dele.

Uma soma de sufixo pode ser calculada adicionando a soma de prefixo ao valor da raia atual.

Observe que a pista ativa com o índice mais baixo sempre receberá um 0 para sua soma de prefixo.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 

## <a name="examples"></a>Exemplos

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

Em um computador com um tamanho de onda de 8 e todas as pistas ativas, exceto pistas 0 e 4, os valores a seguir seriam retornados de WavePrefixSum.

| índice de Lane | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inativos | N/D           |
| 1          | ativo   | = 0           |
| 2          | ativo   | = 0 + 2         |
| 3          | ativo   | = 0 + 2 + 2       |
| 4          | inativos | N/D           |
| 5          | ativo   | = 0 + 2 + 2 + 2     |
| 6          | ativo   | = 0 + 2 + 2 + 2 + 2   |
| 7          | ativo   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>Confira também

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modelo do sombreador 6](shader-model-6-0.md)
