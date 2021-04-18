---
description: Clona uma malha usando um código de formato de vértice flexível (FVF).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'Método ID3DXBaseMesh:: CloneMeshFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807934"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>Método ID3DXBaseMesh:: CloneMeshFVF

Clona uma malha usando um código de formato de vértice flexível (FVF).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) especificando as opções de criação para a malha.

</dd> <dt>

*FVF* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de códigos FVF, que especifica o formato de vértice para os vértices na malha de saída. Para obter os valores dos códigos, consulte [D3DFVF](d3dfvf.md).

</dd> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o objeto de dispositivo associado à malha.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha clonada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

**ID3DXBaseMesh:: CloneMeshFVF** é usado para reformatar e alterar o layout de dados de vértice. Isso é feito criando um novo objeto de malha. Por exemplo, use-o para adicionar espaço para Normals, coordenadas de textura, cores, pesos, etc. que não estavam presentes antes.

[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) atualiza a declaração de vértice com informações semânticas diferentes sem alterar o layout do buffer de vértice. Esse método não modifica o conteúdo do buffer de vértice. Por exemplo, use-o para rerotular uma coordenada de textura 3D como uma binormal ou uma tangente ou vice-versa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
