---
title: Função EvaluateAttributeAtCentroid
description: Avalia no pixel centróide.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- HLSL da função EvaluateAttributeAtCentroid
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364872"
---
# <a name="evaluateattributeatcentroid-function"></a>Função EvaluateAttributeAtCentroid

Avalia no pixel centróide.

## <a name="syntax"></a>Sintaxe

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **Atrib. numérico**

O valor de entrada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O modo de interpolação pode ser **linear** ou **linear \_ sem nenhuma \_ perspectiva** na variável. O uso de **centróide** ou de **exemplo** é ignorado. Atributos com interpolação de constante também são permitidos; nesse caso, o índice de exemplo é ignorado.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




