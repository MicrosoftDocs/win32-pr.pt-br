---
description: 'Método ID3DXMesh:: SetAttributeTable – define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'Método ID3DXMesh:: SetAttributeTable (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4cdb503e934ca00b41482601b59266eee750365
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093344"
---
# <a name="id3dxmeshsetattributetable-method"></a>Método ID3DXMesh:: SetAttributeTable

Define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAttribTable* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Ponteiro para uma matriz de estruturas [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , representando as entradas na tabela de atributos de malha.

</dd> <dt>

*cAttribTableSize* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de atributos na tabela de atributos de malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se um aplicativo acompanhar as informações em uma tabela de atributos e reorganizar a tabela como resultado de alterações em atributos ou rostos, esse método permitirá que o aplicativo atualize as tabelas de atributos em vez de chamar [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh::LockAttributeBuffer**
</dt> </dl>

 

 
