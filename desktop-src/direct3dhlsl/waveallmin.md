---
title: Função WaveActiveMin
description: Retorna o valor mínimo da expressão em todas as faixas ativas na onda atual replica-a de volta para todas as faixas ativas.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Função WaveActiveMin HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b97f2e58449e8b33270318f305a6fee87662a6aac4643b35152024366bf8b08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721783"
---
# <a name="waveactivemin-function"></a>Função WaveActiveMin

Retorna o valor mínimo da expressão em todas as faixas ativas na onda atual replica-a de volta para todas as faixas ativas.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expr* 
</dt> <dd>

A expressão a ser avaliada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor mínimo.

## <a name="remarks"></a>Comentários

A ordem das operações é indefinida.

Essa função tem suporte do modelo de sombreador 6.0 em todos os estágios do sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do Modelo de Sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




