---
description: Recupera a matriz atual na parte superior da pilha.
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
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790565"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>Método ID3DXMATRIXStack:: GetTop (D3DX10. h)

Recupera a matriz atual na parte superior da pilha.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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

 

 
