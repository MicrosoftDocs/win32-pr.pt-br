---
title: Função WaveActiveBitAnd
description: Retorna o bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- HLSL da função WaveActiveBitAnd
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96d09d91df4ff9226a8fb86203be0bd79bc3c11d1882553607358c3c84d3814c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282994"
---
# <a name="waveactivebitand-function"></a>Função WaveActiveBitAnd

Retorna o bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas.

## <a name="syntax"></a>Sintaxe


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expr* 
</dt> <dd>

A expressão a ser avaliada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O bit e o valor.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




