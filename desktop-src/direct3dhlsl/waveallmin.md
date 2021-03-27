---
title: Função WaveActiveMin
description: Retorna o valor mínimo da expressão em todas as pistas ativas na onda atual, replicando-a de volta para todas as pistas ativas.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- HLSL da função WaveActiveMin
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008598"
---
# <a name="waveactivemin-function"></a>Função WaveActiveMin

Retorna o valor mínimo da expressão em todas as pistas ativas na onda atual, replicando-a de volta para todas as pistas ativas.

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

## <a name="return-value"></a>Retornar valor

O valor mínimo.

## <a name="remarks"></a>Comentários

A ordem das operações é indefinida.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




