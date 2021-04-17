---
description: Divide uma malha em malhas menores que o tamanho especificado.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Função D3DXSplitMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811722"
---
# <a name="d3dxsplitmesh-function"></a>Função D3DXSplitMesh

Divide uma malha em malhas menores que o tamanho especificado.

## <a name="syntax"></a>Sintaxe


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMeshIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha de origem.

</dd> <dt>

*pAdjacencyIn* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha a ser simplificada.

</dd> <dt>

*MaxSize* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Número máximo de vértices na malha resultante.

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Sinalizadores de opção para as novas malhas.

</dd> <dt>

*pMeshesOut* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de malhas retornadas.

</dd> <dt>

*ppMeshArrayOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de interfaces [**ID3DXMesh**](id3dxmesh.md) para as novas malhas. Para uma malha de origem dividida em n malhas, *ppMeshArrayOut* é uma matriz de n **ID3DXMesh** ponteiros.

</dd> <dt>

*ppAdjacencyArrayOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de matrizes de adjacência (DWORDs) para as novas malhas. Consulte [**ID3DXBuffer**](id3dxbuffer.md). Esse parâmetro é opcional.

</dd> <dt>

*ppFaceRemapArrayOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de matrizes de remapeamento facial (DWORDs) para as novas malhas. Consulte [**ID3DXBuffer**](id3dxbuffer.md). Esse parâmetro é opcional.

</dd> <dt>

*ppVertRemapArrayOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de matrizes de remapeamento de vértice para as novas malhas. Consulte [**ID3DXBuffer**](id3dxbuffer.md). Esse parâmetro é opcional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Um uso comum dessa função é dividir uma malha com índices de 32 bits (mais de 65535 vértices) em mais de uma malha, cada um com índices de 16 bits.

As matrizes de adjacência, remapeamento de vértice e remapeamento de face são as DWORDs em que cada matriz contém n ponteiros DWORD, seguidos pelos dados DWORD referenciados pelos ponteiros. Por exemplo, para obter as informações de remapeamento facial para a face 3 na malha 2, o código a seguir pode ser usado, supondo que os dados de remapeamento facial foram retornados em uma variável chamada *ppFaceRemapArrayOut*.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
