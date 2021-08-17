---
title: Função WaveActiveAnyTrue
description: Retornará true se a expressão for verdadeira em qualquer uma das faixas ativas na onda atual.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Função WaveActiveAnyTrue HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c49c9727461d316d7d2c9d8f048971384e568476d1ca693aeec49cdf14a4795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721726"
---
# <a name="waveactiveanytrue-function"></a>Função WaveActiveAnyTrue

Retornará true se a expressão for verdadeira em qualquer uma das faixas ativas na onda atual.

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

## <a name="return-value"></a>Valor retornado

True se a expressão for verdadeira em qualquer faixa.

## <a name="remarks"></a>Comentários

Essa função tem suporte do modelo de sombreador 6.0 em todos os estágios do sombreador. 



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do Modelo de Sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




