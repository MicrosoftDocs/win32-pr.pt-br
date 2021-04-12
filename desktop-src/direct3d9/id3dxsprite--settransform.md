---
description: Define a transformação Sprite.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'Método ID3DXSprite:: SetTransform (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173065"
---
# <a name="id3dxspritesettransform-method"></a>Método ID3DXSprite:: SetTransform

Define a transformação Sprite.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTransform* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação do sprite do espaço do mundo original. Use essa transformação para dimensionar, girar ou transformar o sprite.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[Transformações (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




