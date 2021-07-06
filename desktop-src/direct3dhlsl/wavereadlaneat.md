---
title: Função WaveReadLaneAt
description: Retorna o valor da expressão para o índice de raia fornecido dentro da onda especificada.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- HLSL da função WaveReadLaneAt
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316478"
---
# <a name="wavereadlaneat-function"></a>Função WaveReadLaneAt

Retorna o valor da expressão para o índice de raia fornecido dentro da onda especificada.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expr* 
</dt> <dd>

A expressão a ser avaliada.

</dd> <dt>

*laneIndex* 
</dt> <dd>

O índice da pista para a qual o resultado de *expr* será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor resultante é o resultado de *expr*. Será uniforme se *laneIndex* for uniforme.

## <a name="remarks"></a>Comentários

Essa função é efetivamente uma difusão do valor na pista do *laneIndex*' th.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.

## <a name="see-also"></a>Consulte também

* [Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [Modelo do sombreador 6](shader-model-6-0.md)
