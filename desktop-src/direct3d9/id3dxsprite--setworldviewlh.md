---
description: Define a transformação de exibição mundial esquerda para um sprite. Uma chamada para esse método é necessária antes do uso de sprites de classificação ou de méd.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: Método ID3DXSprite::SetWorldViewLH (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67ee276b90629a18f93bd9a26879e8a7ad62d71ae46baf2d2c0a6bfba82a53a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292568"
---
# <a name="id3dxspritesetworldviewlh-method"></a>Método ID3DXSprite::SetWorldViewLH

Define a transformação de exibição mundial esquerda para um sprite. Uma chamada para esse método é necessária antes do uso de sprites de classificação ou de méd.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWorld* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para um [**D3DXMATRIX que**](d3dxmatrix.md) contém uma transformação mundial. Se **NULL**, a matriz de identidade será usada para a transformação do mundo.

</dd> <dt>

*pView* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para um [**D3DXMATRIX que**](d3dxmatrix.md) contém uma transformação de exibição. Se **NULL**, a matriz de identidade será usada para a transformação de exibição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

Uma chamada para esse método (ou para [**ID3DXSprite::SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) será necessária se o sprite for renderizado com o valor do sinalizador [BACKTOFRONT D3DXSpriteVIEW \_ \_ ,](d3dxsprite.md)D3DXSprite \_ \_ SORT DEPTH OU \_ \_ D3DXSprite \_ \_ SORT \_ DEPTH \_ BACKTOFRONT [**em ID3DXSprite::Begin.**](id3dxsprite--begin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




