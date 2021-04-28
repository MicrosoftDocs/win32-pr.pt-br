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
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108034"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
