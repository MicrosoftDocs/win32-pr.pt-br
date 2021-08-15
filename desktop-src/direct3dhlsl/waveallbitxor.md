---
title: Função WaveActiveBitXor
description: Retorna o XOR bit a bit de todos os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- HLSL da função WaveActiveBitXor
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 733ab8c40a59b784af8a7d50c4f8e1e543f344ee2d75ed9b6896992e6176ff18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504876"
---
# <a name="waveactivebitxor-function"></a>Função WaveActiveBitXor

Retorna o XOR bit a bit de todos os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.

## <a name="syntax"></a>Sintaxe

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expr* 
</dt> <dd>

A expressão a ser avaliada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de XOR de bits.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




