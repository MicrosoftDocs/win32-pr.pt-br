---
description: Clona uma malha usando um declarator.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: Método ID3DXBaseMesh::CloneMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fec8b0881cdef43051afcb06d63ec20284cb116299912ce0acf7ac4c54a0f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521859"
---
# <a name="id3dxbasemeshclonemesh-method"></a>Método ID3DXBaseMesh::CloneMesh

Clona uma malha usando um declarator.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Opções* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) especificando opções de criação para a malha.

</dd> <dt>

*pDeclaration* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Uma matriz de [**elementos D3DVERTEXELEMENT9,**](d3dvertexelement9.md) que especificam o formato de vértice para os vértices na malha de saída.

</dd> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o objeto de dispositivo associado à malha.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh,**](id3dxmesh.md) representando a malha clonada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

**ID3DXBaseMesh::CloneMesh** é usado para reformatar e alterar o layout de dados de vértice. Isso é feito criando um novo objeto de malha. Por exemplo, use-o para adicionar espaço para normais, coordenadas de textura, cores, pesos etc. que não estavam presentes antes.

[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) atualiza a declaração de vértice com informações semânticas diferentes sem alterar o layout do buffer de vértice. Esse método não modifica o conteúdo do buffer de vértice. Por exemplo, use-o para rotular uma coordenada de textura 3D como binormal ou tangente ou vice-versa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
