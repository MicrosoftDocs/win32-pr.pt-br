---
description: 'Método ID3DXMATRIXStack:: GetTop (D3dx9math. h) – recupera a matriz atual na parte superior da pilha.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'Método ID3DXMATRIXStack:: GetTop (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093574"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: GetTop (D3dx9math. h)

Recupera a matriz atual na parte superior da pilha.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Esse método retorna um ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que representa a matriz atual.

## <a name="remarks"></a>Comentários

Não há garantia de que o ponteiro [**D3DXMATRIX**](d3dxmatrix.md) retornado por esse método seja válido após operações de pilha subsequentes.

Observe que esse método não remove a matriz atual da parte superior da pilha; em vez disso, ele apenas retorna a matriz atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




