---
description: Determina se um quatrion é um quaterão de identidade.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Função D3DXQuaternionIsIdentity (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b34debbe70ec6edcd3f08a1ec83383335a0d4f97801d122bc1bd73a82a81ff36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731588"
---
# <a name="d3dxquaternionisidentity-function"></a>Função D3DXQuaternionIsIdentity

Determina se um quatrion é um quaterão de identidade.

## <a name="syntax"></a>Sintaxe


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pQ* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para a [**estrutura D3DXQUATERNION**](d3dxquaternion.md) que será testada quanto à identidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se o quatternion for um quatternion de identidade, essa função retornará **TRUE.** Caso contrário, essa função **retornará FALSE.**

## <a name="remarks"></a>Comentários

Use [**D3DXQuaternionNormalize para**](d3dxquaternionnormalize.md) qualquer entrada de quatérnion que ainda não tenha sido normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
</dt> </dl>

 

 
