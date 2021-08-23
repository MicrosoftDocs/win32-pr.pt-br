---
title: Função EvaluateAttributeAtCentoid
description: É avaliada no centroide de pixel.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- Função EvaluateAttributeAtCentoid HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 867f7dadc2ccf7d86eed602dd9e65d07be7558f0a8a00426e3a45bc1c2c97a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744036"
---
# <a name="evaluateattributeatcentroid-function"></a>Função EvaluateAttributeAtCentoid

É avaliada no centroide de pixel.

## <a name="syntax"></a>Sintaxe

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ Em\]
</dt> <dd>

Tipo: **numérico de atrib**

O valor de entrada.

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

 

 




