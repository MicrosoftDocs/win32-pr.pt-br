---
description: Método ID3DXMATRIXStack::P (D3DX10.h) – adiciona uma matriz à pilha.
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: Método ID3DXMATRIXStack::P (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8c9054274666b41e70fa060d10a28309be929a19ee5c363ff4afeb76b25e1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914232"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a>Método ID3DXMATRIXStack::P (D3DX10.h)

Adiciona uma matriz à pilha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Push();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método incrementa a contagem de itens na pilha em 1, duplicando a matriz atual. A pilha aumentará dinamicamente conforme mais itens são adicionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




