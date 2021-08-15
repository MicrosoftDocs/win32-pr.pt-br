---
title: Função WaveReadLaneAt
description: Retorna o valor da expressão para o índice de lane especificado dentro da onda especificada.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Função WaveReadLaneAt HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08fa669f8c4284c26052dd68bdbe9ab4f5b99b80b8bdf9445aa3375f0a87a9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504616"
---
# <a name="wavereadlaneat-function"></a>Função WaveReadLaneAt

Retorna o valor da expressão para o índice de lane especificado dentro da onda especificada.

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

O índice da faixa para a qual o *resultado do expr* será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor resultante é o resultado de *expr*. Ele será uniforme se *laneIndex* for uniforme.

## <a name="remarks"></a>Comentários

Essa função é efetivamente uma difusão do valor na *laneIndex*'th lane.

Essa função tem suporte do modelo de sombreador 6.0 em todos os estágios do sombreador.

## <a name="see-also"></a>Confira também

* [Visão geral do Modelo de Sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [Modelo de sombreador 6](shader-model-6-0.md)
