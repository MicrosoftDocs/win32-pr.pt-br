---
title: Função EvaluateAttributeSnapped
description: Avalia no pixel centróide com um deslocamento.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- HLSL da função EvaluateAttributeSnapped
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5408b2c8133947b948bc42eb6ff0c725584b0cf2c60ccf0731a9d584d3c898a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512013"
---
# <a name="evaluateattributesnapped-function"></a>Função EvaluateAttributeSnapped

Avalia no pixel centróide com um deslocamento.

## <a name="syntax"></a>Sintaxe

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **Atrib. numérico**

O valor de entrada.

</dd> <dt>

*deslocamento* \[ no\]
</dt> <dd>

Tipo: **Int2**

Um deslocamento 2D do centro de pixels usando uma grade de 16x16.

</dd> </dl>

## <a name="remarks"></a>Comentários

O intervalo para o parâmetro de *deslocamento* deve ser definido pelo seguinte código de byte.

Somente os 4 bits menos significativos dos primeiros dois componentes (U, V) do deslocamento de pixel são usados. A conversão do ponto fixo de 4 bits para float é a seguinte (MSB... LSB), em que o MSB é uma parte da fração e determina o sinal:

-   1000 =-0,5 f (-8/16)
-   1001 =-0.4375 f (-7/16)
-   1010 =-0.375 f (-6/16)
-   1011 =-0.3125 f (-5/16)
-   1100 =-0,25 f (-4/16)
-   1101 =-0.1875 f (-3/16)
-   1110 =-0,125 f (-2/16)
-   1111 =-0.0625 f (-1/16)
-   0000 = 0,0 f (0/16)
-   0001 = 0.0625 f (1/16)
-   0010 = 0,125 f (2/16)
-   0011 = 0.1875 f (3/16)
-   0100 = 0,25 f (4/16)
-   0101 = 0.3125 f (5/16)
-   0110 = 0.375 f (6/16)
-   0111 = 0.4375 f (7/16)

> [!Note]  
> As bordas esquerda e superior de um pixel são incluídas no deslocamento; no entanto, as bordas inferior e direita não são incluídas. Todos os outros bits no inteiro de 32 bits você e os valores de deslocamento V são ignorados.

 

Uma implementação pode assumir o deslocamento fornecido pelo sombreador e obter um valor completo de ponto fixo de 32 bits (28,4), que abrange o intervalo válido, executando o seguinte cálculo:


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Se uma implementação precisar mapear o deslocamento para um deslocamento de ponto flutuante, ele executará o seguinte cálculo:


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




