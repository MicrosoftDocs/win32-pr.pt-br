---
description: Recupera uma declaração que descreve os vértices na malha.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: Método ID3DXBaseMesh::GetDeclaration (D3DX9Mesh.h)
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
ms.openlocfilehash: 4d66afd8daf6a8cc60fa63dcf38e6bb853c33ca05986d2a37b94eba1250eb01b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026466"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a>Método ID3DXBaseMesh::GetDeclaration

Recupera uma declaração que descreve os vértices na malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Declaração* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de [**elementos D3DVERTEXELEMENT9**](d3dvertexelement9.md) que descrevem o formato de vértice dos vértices de malha. O limite superior dessa matriz declarator é [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md). A matriz de elementos de vértice termina com a macro [**END D3DDECL. \_**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A matriz de elementos inclui a macro [**END D3DDECL, \_**](d3ddecl-end.md) que encerra a declaração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
