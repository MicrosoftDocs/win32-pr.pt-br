---
title: Função WaveIsFirstLane
description: Retorna true somente para a pista ativa na onda atual com o menor índice.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- HLSL da função WaveIsFirstLane
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294607"
---
# <a name="waveisfirstlane-function"></a>Função WaveIsFirstLane

Retorna true somente para a pista ativa na onda atual com o menor índice.

## <a name="syntax"></a>Sintaxe


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

True somente para a pista ativa na onda atual com o menor índice.

## <a name="remarks"></a>Comentários

Essa função pode ser usada para identificar as operações que devem ser executadas apenas uma vez por onda.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="examples"></a>Exemplos

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




