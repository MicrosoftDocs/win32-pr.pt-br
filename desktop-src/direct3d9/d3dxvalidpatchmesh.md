---
description: Valida uma malha de patch, retornando o número de vértices e patches de degeneração.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Função D3DXValidPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930575"
---
# <a name="d3dxvalidpatchmesh-function"></a>Função D3DXValidPatchMesh

Valida uma malha de patch, retornando o número de vértices e patches de degeneração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMeshIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Ponteiro para uma interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) , representando a malha de patch a ser testada.

</dd> <dt>

*pNumDegenerateVertices* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Retorna o número de vértices de degeneração na malha do patch.

</dd> <dt>

*pNumDegeneratePatches* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Retorna o número de patches de degeneração na malha do patch.

</dd> <dt>

*ppErrorsAndWarnings* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um ponteiro para um buffer que contém uma cadeia de caracteres de erros e avisos que explicam os problemas encontrados na malha do patch.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método valida a malha verificando índices inválidos. As informações de erro estão disponíveis na saída do depurador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
