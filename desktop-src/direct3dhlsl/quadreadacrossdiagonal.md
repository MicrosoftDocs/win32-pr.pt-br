---
title: Função QuadReadAcrossDiagonal
description: Retorna o valor local especificado que é lido da faixa diagonalmente oposta nesse quad.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- Função QuadReadAcrossDiagonal HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53066864ec87528406b20d5503f4e47497cb3aa80e44f01e279845fdc2674339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981926"
---
# <a name="quadreadacrossdiagonal-function"></a>Função QuadReadAcrossDiagonal

Retorna o valor local especificado que é lido da faixa diagonalmente oposta nesse quad.

## <a name="syntax"></a>Sintaxe


``` syntax
<type> QuadReadAcrossDiagonal(
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

O valor local especificado que é lido da faixa diagonalmente oposta nesse quad.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre quads, consulte [Visão geral do Modelo de Sombreador 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Essa função tem suporte do modelo de sombreador 6.0 somente em sombreadores de computação e pixel.



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




