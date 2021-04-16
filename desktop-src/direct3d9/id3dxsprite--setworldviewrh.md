---
description: Define a transformação de exibição Mundial da mão direita para um Sprite. Uma chamada para esse método é necessária antes de obter ou classificar sprites.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'Método ID3DXSprite:: SetWorldViewRH (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765315"
---
# <a name="id3dxspritesetworldviewrh-method"></a>Método ID3DXSprite:: SetWorldViewRH

Define a transformação de exibição Mundial da mão direita para um Sprite. Uma chamada para esse método é necessária antes de obter ou classificar sprites.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWorld* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação do mundo. Se for **NULL**, a matriz de identidade será usada para a transformação mundial.

</dd> <dt>

*pView* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação de exibição. Se for **NULL**, a matriz de identidade será usada para a transformação de exibição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

Uma chamada para esse método (ou para [**ID3DXSprite:: SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) será necessária se o sprite for renderizado com o [D3DXSprite \_ \_ mural](d3dxsprite.md), D3DXSprite \_ \_ classificar \_ profundidade \_ FRONTTOBACK ou D3DXSprite \_ \_ \_ \_ valor do sinalizador BACKTOFRONT de profundidade de classificação em [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




