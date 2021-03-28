---
title: 'Função WavePrefixProduct '
description: Retorna o produto de todos os valores nas pistas ativas nesta onda com índices menores que esta raia.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- HLSL da função WavePrefixProduct
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366923"
---
# <a name="waveprefixproduct-function"></a>Função WavePrefixProduct 

Retorna o produto de todos os valores nas pistas ativas nesta onda com índices menores que esta raia.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Parâmetros

*value* 

O valor a ser multiplicado.

## <a name="return-value"></a>Retornar valor

O produto de todos os valores.

## <a name="remarks"></a>Comentários

A ordem das operações nessa rotina não pode ser garantida. Portanto, efetivamente, o \[ \] sinalizador preciso é ignorado dentro dele.

Um produto de sufixo pode ser calculado multiplicando o prefixo do produto pelo valor da raia atual.

Observe que a pista ativa com o índice mais baixo sempre receberá um 1 para seu prefixo de produto.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 

## <a name="examples"></a>Exemplos

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

Em um computador com um tamanho de onda de 8 e todas as pistas ativas, exceto pistas 0 e 4, os valores a seguir seriam retornados de WavePrefixProduct.

| índice de Lane | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inativos | N/D           |
| 1          | ativo   | = 1           |
| 2          | ativo   | = 1 \* 2        |
| 3          | ativo   | = 1 \* 2 \* 2     |
| 4          | inativos | N/D           |
| 5          | ativo   | = 1 \* 2 \* 2 2 \*       |
| 6          | ativo   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | ativo   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>Confira também

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modelo do sombreador 6](shader-model-6-0.md)
