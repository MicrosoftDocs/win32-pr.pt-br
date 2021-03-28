---
title: Função WaveGetLaneCount
description: Retorna o número de pistas em uma onda nessa arquitetura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- HLSL da função WaveGetLaneCount
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366924"
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

O resultado será entre 4 e 128 e incluirá todas as ondas: as pistas ativas, inativas e/ou auxiliares. O resultado retornado por essa função pode variar significativamente dependendo da implementação do driver.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




