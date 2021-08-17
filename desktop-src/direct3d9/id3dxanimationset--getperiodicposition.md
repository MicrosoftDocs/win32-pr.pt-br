---
description: Retorna a posição de hora no período local de um conjunto de animação.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: Método ID3DXAnimationSet::GetPeriodicPosition (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8451e3332b61d7e6e993de7df0832a78c0c45c0240633fd5f421998816f7f26f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122057"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>Método ID3DXAnimationSet::GetPeriodicPosition

Retorna a posição de hora no período local de um conjunto de animação.

## <a name="syntax"></a>Sintaxe


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Posição* \[ Em\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Hora local do conjunto de animação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Posição de tempo, conforme medido no período do conjunto de animação. Esse valor será limitado pelo período do conjunto de animação.

## <a name="remarks"></a>Comentários

A posição de tempo retornada por esse método pode ser usada como o parâmetro PeriodicPosition de [**ID3DXAnimationSet::GetSRT.**](id3dxanimationset--getsrt.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
