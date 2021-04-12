---
title: Função QuadReadLaneAt
description: Retorna o valor de origem especificado da pista identificada pela ID da pista dentro do Quad atual.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- HLSL da função QuadReadLaneAt
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454455"
---
# <a name="quadreadlaneat-function"></a>Função QuadReadLaneAt

Retorna o valor de origem especificado da pista identificada pela ID da pista dentro do Quad atual.

## <a name="syntax"></a>Sintaxe


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*origemvalue* 
</dt> <dd>

O tipo solicitado.

</dd> <dt>

*quadLaneID* 
</dt> <dd>

A ID da raia; Esse será um valor de 0 a 3.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de origem especificado. O resultado dessa função é uniforme em todo o quad. Se a pista de origem estiver inativa, os resultados serão indefinidos.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre os quatro processadores, consulte [visão geral do sombreador modelo 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Essa função tem suporte do modelo de sombreador 6,0 somente em sombreadores de computação e pixel.



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelo do sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




