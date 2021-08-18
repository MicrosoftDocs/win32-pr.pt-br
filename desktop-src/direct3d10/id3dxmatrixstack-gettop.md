---
description: 'Método ID3DXMATRIXStack:: GetTop (D3DX10. h) – recupera a matriz atual na parte superior da pilha.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'Método ID3DXMATRIXStack:: GetTop (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 340ea7ed85e05795dbc3949a29c5384871dfe840aa25ed4f9b2f07e1d4264de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852226"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>Método ID3DXMATRIXStack:: GetTop (D3DX10. h)

Recupera a matriz atual na parte superior da pilha.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Esse método retorna um ponteiro para uma estrutura D3DXMATRIX que representa a matriz atual.

## <a name="remarks"></a>Comentários

Não há garantia de que o ponteiro D3DXMATRIX retornado por esse método seja válido após operações de pilha subsequentes.

Observe que esse método não remove a matriz atual da parte superior da pilha; em vez disso, ele apenas retorna a matriz atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
