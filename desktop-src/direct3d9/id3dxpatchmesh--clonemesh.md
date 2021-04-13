---
description: Cria uma nova malha de patch com a declaração de vértice especificada.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'Método ID3DXPatchMesh:: CloneMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298514"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>Método ID3DXPatchMesh:: CloneMesh

Cria uma nova malha de patch com a declaração de vértice especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.

</dd> <dt>

*pDecl* \[ no\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que especificam o formato de vértice para os vértices na malha de saída.

</dd> <dt>

*pMesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa a malha clonada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

**CloneMesh** converte o buffer de vértice para a nova declaração de vértice. As entradas na declaração de vértice que são novas na malha original são definidas como 0. Se a malha atual tiver uma adjacência, a nova malha também terá uma adjacência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
