---
title: 'Função WavePrefixSum '
description: Retorna a soma de todos os valores nas faixas ativas com índices menores do que este.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Função WavePrefixSum HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbb9ced3fbf7e150cbe3b9bca7eb176e61cf6c8881def22a977ae37a2dbf4b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671086"
---
# <a name="waveprefixsum-function"></a>Função WavePrefixSum 

Retorna a soma de todos os valores nas faixas ativas com índices menores do que este.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Parâmetros

*value* 

O valor a ser somdo.

## <a name="return-value"></a>Valor retornado

A soma dos valores.

## <a name="remarks"></a>Comentários

A ordem das operações nessa rotina não pode ser garantida. Portanto, efetivamente, \[ o sinalizador preciso é ignorado dentro \] dele.

Uma soma de pós-sufixo pode ser calculada adicionando a soma do prefixo ao valor da faixa atual.

Observe que a faixa ativa com o índice mais baixo sempre receberá um 0 para sua soma de prefixo.

Essa função tem suporte do modelo de sombreador 6.0 em todos os estágios do sombreador. 

## <a name="examples"></a>Exemplos

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

Em um computador com um tamanho de onda de 8 e todas as faixas ativas, exceto as faixas 0 e 4, os valores a seguir seriam retornados de WavePrefixSum.

| índice lane | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inativos | N/D           |
| 1          | ativo   | = 0           |
| 2          | ativo   | = 0+2         |
| 3          | ativo   | = 0+2+2       |
| 4          | inativos | n/d           |
| 5          | ativo   | = 0+2+2+2+2     |
| 6          | ativo   | = 0+2+2+2+2+2   |
| 7          | ativo   | = 0+2+2+2+2+2+2 |

## <a name="see-also"></a>Confira também

[Visão geral do Modelo de Sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modelo de sombreador 6](shader-model-6-0.md)
