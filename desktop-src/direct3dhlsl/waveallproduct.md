---
title: Função WaveActiveProduct
description: Multiplica os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- HLSL da função WaveActiveProduct
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824063"
---
# <a name="waveactiveproduct-function"></a>Função WaveActiveProduct

Multiplica os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expr* 
</dt> <dd>

A expressão a ser avaliada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor do produto.

## <a name="remarks"></a>Comentários

A ordem das operações é indefinida.

Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador. 



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




