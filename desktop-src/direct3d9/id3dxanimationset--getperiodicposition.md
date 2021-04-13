---
description: Retorna a posição de hora no período de tempo local de um conjunto de animações.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'Método ID3DXAnimationSet:: GetPeriodicPosition (D3dx9anim. h)'
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
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298836"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a>Método ID3DXAnimationSet:: GetPeriodicPosition

Retorna a posição de hora no período de tempo local de um conjunto de animações.

## <a name="syntax"></a>Sintaxe


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Posição* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Hora local do conjunto de animações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Posição de tempo conforme medida no período do conjunto de animações. Esse valor será limitado pelo período do conjunto de animações.

## <a name="remarks"></a>Comentários

A posição de tempo retornada por esse método pode ser usada como o parâmetro PeriodicPosition de [**ID3DXAnimationSet:: GetSRT**](id3dxanimationset--getsrt.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
