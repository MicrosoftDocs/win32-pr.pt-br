---
title: Função EvaluateAttributeAtSample
description: É avaliada no local de exemplo indexado.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- Função EvaluateAttributeAtSample HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29191a3790afee2d37fee3d2ee8fb58673ff487af178bd8b1e2b33f26f1ec44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982476"
---
# <a name="evaluateattributeatsample-function"></a>Função EvaluateAttributeAtSample

É avaliada no local de exemplo indexado.

## <a name="syntax"></a>Sintaxe

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ Em\]
</dt> <dd>

Tipo: **numérico de atrib**

O valor de entrada.

</dd> <dt>

*sampleindex* \[ Em\]
</dt> <dd>

Tipo: **uint**

O local de exemplo.

</dd> </dl>

## <a name="remarks"></a>Comentários

O modo de interpolação pode **ser linear** ou linear **sem \_ \_ perspectiva** na variável. O uso **de centroide** **ou amostra** é ignorado. Atributos com interpolação constante também são permitidos, caso em que o índice de exemplo é ignorado.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




