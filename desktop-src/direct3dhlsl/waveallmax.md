---
title: Função WaveActiveMax
description: Retorna o valor máximo da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- HLSL da função WaveActiveMax
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2020
ms.locfileid: "104368979"
---
# <a name="waveactivemax-function"></a>Função WaveActiveMax

Retorna o valor máximo da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WaveActiveMax(
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

O valor máximo.

## <a name="remarks"></a>Comentários

A ordem das operações é indefinida.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




