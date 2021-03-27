---
title: Função WaveActiveSum
description: Soma o valor da expressão em todas as pistas ativas na onda atual e a Replica para todas as pistas na onda atual.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- HLSL da função WaveActiveSum
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917783"
---
# <a name="waveactivesum-function"></a>Função WaveActiveSum

Soma o valor da expressão em todas as pistas ativas na onda atual e a Replica para todas as pistas na onda atual.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WaveActiveSum(
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

O valor da soma.

## <a name="remarks"></a>Comentários

A ordem das operações é indefinida.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




