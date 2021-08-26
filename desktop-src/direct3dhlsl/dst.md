---
title: Função dst
description: Calcula um vetor de distância. | Função dst
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- função dst HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b0d8112902486102e6a4338445a2526b23cab8dafb2ea8b7d68b87d5b803af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068336"
---
# <a name="dst-function"></a>Função dst

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

*src0* \[ Em\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

O primeiro vetor.

</dd> <dt>

*src1* \[ Em\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

O segundo vetor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

O vetor de distância computado.

## <a name="remarks"></a>Comentários

Essa função intrínseca fornece a mesma funcionalidade que a instrução de Sombreador [de Vértice dst](dst---vs.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




