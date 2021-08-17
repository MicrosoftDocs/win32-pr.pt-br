---
description: Define a transformação de exibição do mundo de direita para um sprite. Uma chamada para esse método é necessária antes de classificar sprites ou de mód.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: Método ID3DXSprite::SetWorldViewRH (D3dx9core.h)
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
ms.openlocfilehash: 54da854fff0aeb2001e674218a7e7868971a6cf43af7bc00606b124c3f082b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800414"
---
# <a name="id3dxspritesetworldviewrh-method"></a>Método ID3DXSprite::SetWorldViewRH

Define a transformação de exibição do mundo de direita para um sprite. Uma chamada para esse método é necessária antes de classificar sprites ou de mód.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetWorldViewRH(
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

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

Uma chamada para esse método (ou para [**ID3DXSprite::SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) será necessária se o sprite for renderizado com o valor do sinalizador [BACKTOFRONT D3DXSprite: \_ \_ :Begin OU](d3dxsprite.md) \_ \_ \_ \_ D3DXSprite \_ \_ SORT DEPTH \_ \_ BACKTOFRONT. [](id3dxsprite--begin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




