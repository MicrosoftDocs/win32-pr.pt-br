---
title: Função WaveGetLaneIndex
description: Retorna o índice da pista atual dentro da onda atual.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- HLSL da função WaveGetLaneIndex
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb6b0290b46727cdf0d9ce705d2910df003cbc114638a0135be2023bb836202a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721716"
---
# <a name="wavegetlaneindex-function"></a>Função WaveGetLaneIndex

Retorna o índice da pista atual dentro da onda atual.

## <a name="syntax"></a>Sintaxe

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O índice de raia atual. O resultado será entre 0 e o resultado retornado de [**WaveGetLaneCount**](wavegetlanecount.md).

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




