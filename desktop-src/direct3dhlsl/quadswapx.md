---
title: Função QuadReadAcrossX
description: Retorna o valor local especificado lido da outra pista neste Quad na direção X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- HLSL da função QuadReadAcrossX
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86a2f525a79fa2458e4f7e0ef44379053e03128782d2625e1bdceb23ec518b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672436"
---
# <a name="quadreadacrossx-function"></a>Função QuadReadAcrossX

Retorna o valor local especificado lido da outra pista neste Quad na direção X.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*localValue* 
</dt> <dd>

O tipo solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor local especificado. Se a pista de origem estiver inativa, os resultados serão indefinidos.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre os quatro processadores, consulte [visão geral do sombreador modelo 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Essa função tem suporte do modelo de sombreador 6,0 somente em sombreadores de computação e pixel.



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




