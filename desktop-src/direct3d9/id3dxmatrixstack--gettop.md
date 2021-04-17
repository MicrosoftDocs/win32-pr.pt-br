---
description: Recupera a matriz atual na parte superior da pilha.
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
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762520"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: GetTop (D3dx9math. h)

Recupera a matriz atual na parte superior da pilha.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




