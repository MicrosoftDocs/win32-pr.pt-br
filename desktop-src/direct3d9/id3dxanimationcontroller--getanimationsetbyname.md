---
description: Obtém um conjunto de animação, considerando seu nome.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: Método ID3DXAnimationController::GetAnimationSetByName (D3dx9 multimídia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b417bf9434b712903e61839807f71765b2e3c69916430f162a67febe65fc6cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297039"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a>Método ID3DXAnimationController::GetAnimationSetByName

Obtém um conjunto de animação, considerando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome do conjunto de animação.

</dd> <dt>

*pp PppmSet* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Ponteiro para o [**conjunto de animação ID3DXAnimationSet.**](id3dxanimationset.md)

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

O controlador de animação contém uma matriz de conjuntos de animação. Esse método retorna um conjunto de animação que tem o nome determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
