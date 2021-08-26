---
title: 'Função WavePrefixProduct '
description: Retorna o produto de todos os valores nas faixas ativas nessa onda com índices menores que essa faixa.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Função WavePrefixProduct HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8cb780f951433afc480c38d52c8120e086a91d32117fe9bb566657e0fcf9f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948956"
---
# <a name="waveprefixproduct-function"></a>Função WavePrefixProduct 

Retorna o produto de todos os valores nas faixas ativas nessa onda com índices menores que essa faixa.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Parâmetros

*value* 

O valor a ser multiplicado.

## <a name="return-value"></a>Valor retornado

O produto de todos os valores.

## <a name="remarks"></a>Comentários

A ordem das operações nessa rotina não pode ser garantida. Portanto, efetivamente, \[ o sinalizador preciso é ignorado dentro \] dele.

Um produto pós-sufixo pode ser calculado multiplicando o produto de prefixo pelo valor da faixa atual.

Observe que a faixa ativa com o índice mais baixo sempre receberá um 1 para seu produto de prefixo.

Essa função tem suporte do modelo de sombreador 6.0 em todos os estágios do sombreador. 

## <a name="examples"></a>Exemplos

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

Em um computador com um tamanho de onda de 8 e todas as faixas ativas, exceto as faixas 0 e 4, os valores a seguir seriam retornados de WavePrefixProduct.

| índice lane | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inativos | N/D           |
| 1          | ativo   |  = 1           |
| 2          | ativo   | = 1 \* 2        |
| 3          | ativo   | = 1 \* 2 \* 2     |
| 4          | inativos | n/d           |
| 5          | ativo   | = 1 \* 2 \* 2 \* 2       |
| 6          | ativo   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | ativo   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>Confira também

[Visão geral do Modelo de Sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modelo de sombreador 6](shader-model-6-0.md)
