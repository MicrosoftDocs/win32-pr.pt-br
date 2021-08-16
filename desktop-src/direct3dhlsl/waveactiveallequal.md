---
title: Função WaveActiveAllEqual
description: Retornará true se a expressão for a mesma para cada pista ativa na onda atual (e, portanto, uniforme em toda a ti).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- HLSL da função WaveActiveAllEqual
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f62493a1bf08b85e95acad319bac2d022c30a53d43c28a87d0f5f603e78d300f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786106"
---
# <a name="waveactiveallequal-function"></a>Função WaveActiveAllEqual

Retornará true se a expressão for a mesma para cada pista ativa na onda atual (e, portanto, uniforme em toda a ti).

## <a name="syntax"></a>Sintaxe


``` syntax
bool WaveActiveAllEqual(
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

True se a expressão for a mesma para todas as pistas ativas na onda atual.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




