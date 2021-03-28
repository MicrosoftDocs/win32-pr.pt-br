---
title: função de DST
description: Calcula um vetor de distância. | função de DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- função de DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837742"
---
# <a name="dst-function"></a>função de DST

Calcula um vetor de distância.

## <a name="syntax"></a>Sintaxe

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*src0* \[ no\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

O primeiro vetor.

</dd> <dt>

*src1* \[ no\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

O segundo vetor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

O vetor de distância computada.

## <a name="remarks"></a>Comentários

Essa função intrínseca fornece a mesma funcionalidade que o [DST](dst---vs.md)de instrução do sombreador de vértice.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




