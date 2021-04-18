---
description: Recupera uma declaração que descreve os vértices na malha.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: 'Método ID3DXBaseMesh:: getdeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f8736e822bfe4a959f35f60bb79783e79f2d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771273"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a>Método ID3DXBaseMesh:: getdeclaration

Recupera uma declaração que descreve os vértices na malha.

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

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A matriz de elementos inclui a macro [**D3DDECL \_ end**](d3ddecl-end.md) , que encerra a declaração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
