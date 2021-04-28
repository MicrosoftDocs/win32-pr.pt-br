---
description: 'Método ID3DXSkinInfo:: getdeclaration-Obtém a declaração de vértice.'
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'Método ID3DXSkinInfo:: getdeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093134"
---
# <a name="id3dxskininfogetdeclaration-method"></a>Método ID3DXSkinInfo:: getdeclaration

Obtém a declaração de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Declaração* \[ de entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que descreve o formato de vértice dos vértices de malha. O limite superior dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md). A matriz do elemento Vertex termina com a macro [**\_ end D3DDECL**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A matriz de elementos inclui a macro [**D3DDECL \_ end**](d3ddecl-end.md) , que encerra a declaração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: setdeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
