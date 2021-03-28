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
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2020
ms.locfileid: "104365800"
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

## <a name="return-value"></a>Retornar valor

O valor resultante é o resultado de *expr*. Será uniforme se *laneIndex* for uniforme.

## <a name="remarks"></a>Comentários

Essa função é efetivamente uma difusão do valor na pista laneIndex'th.

Essa função tem suporte do modelo de sombreador 6,0, nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




