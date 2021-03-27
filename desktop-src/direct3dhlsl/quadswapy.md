---
title: Função QuadReadAcrossY
description: Retorna o valor de origem especificado lido da outra pista neste Quad na direção Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- HLSL da função QuadReadAcrossY
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104967232"
---
# <a name="quadreadacrossy-function"></a>Função QuadReadAcrossY

Retorna o valor de origem especificado lido da outra pista neste Quad na direção Y.

## <a name="syntax"></a>Sintaxe

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*localValue* 
</dt> <dd>

O tipo solicitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de origem especificado. Se a pista de origem estiver inativa, os resultados serão indefinidos.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre os quatro processadores, consulte [visão geral do sombreador modelo 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Essa função tem suporte do modelo de sombreador 6,0 somente em sombreadores de computação e pixel.



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




