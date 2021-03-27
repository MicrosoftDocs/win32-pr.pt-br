---
title: Função EvaluateAttributeAtSample
description: Avalia no local de exemplo indexado.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- HLSL da função EvaluateAttributeAtSample
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638449"
---
# <a name="evaluateattributeatsample-function"></a>Função EvaluateAttributeAtSample

Avalia no local de exemplo indexado.

## <a name="syntax"></a>Sintaxe

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **Atrib. numérico**

O valor de entrada.

</dd> <dt>

*sampleindex* \[ no\]
</dt> <dd>

Tipo: **uint**

O local de exemplo.

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

 

 




