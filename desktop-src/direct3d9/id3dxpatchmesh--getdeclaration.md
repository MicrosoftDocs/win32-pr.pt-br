---
description: 'Método ID3DXPatchMesh:: getdeclaration-Obtém a declaração de vértice.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'Método ID3DXPatchMesh:: getdeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093294"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>Método ID3DXPatchMesh:: getdeclaration

Obtém a declaração de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDeclaration* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que descreve o formato de vértice dos vértices de malha. A dimensão dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md). A matriz do elemento Vertex termina com a macro [**\_ end D3DDECL**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A matriz de elementos inclui a macro [**D3DDECL \_ end**](d3ddecl-end.md) , que encerra a declaração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
