---
title: Função WaveActiveAnyTrue
description: Retornará true se a expressão for verdadeira em qualquer uma das pistas ativas na onda atual.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- HLSL da função WaveActiveAnyTrue
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104988716"
---
# <a name="waveactiveanytrue-function"></a>Função WaveActiveAnyTrue

Retornará true se a expressão for verdadeira em qualquer uma das pistas ativas na onda atual.

## <a name="syntax"></a>Sintaxe

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expr* 
</dt> <dd>

A expressão booliana a ser avaliada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

True se a expressão for verdadeira em qualquer pista.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




