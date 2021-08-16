---
title: Função WaveGetLaneCount
description: Retorna o número de pistas em uma onda nessa arquitetura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Função WaveGetLaneCount HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a177e50ee3c4c9c715ea109faaed72c24e174e4e942059a4dee0dcd0de91a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504734"
---
# <a name="wavegetlanecount-function"></a>Função WaveGetLaneCount

Retorna o número de pistas em uma onda nessa arquitetura.

## <a name="syntax"></a>Sintaxe

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O resultado será entre 4 e 128 e inclui todas as ondas: ativas, inativas e/ou faixas auxiliares. O resultado retornado dessa função pode variar significativamente dependendo da implementação do driver.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6.0 em todos os estágios do sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do Modelo de Sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




