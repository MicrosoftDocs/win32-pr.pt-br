---
description: Divide uma malha em malhas menores que o tamanho especificado.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Função D3DXSplitMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: aee07e79286867ce11ce394e852fdfc01c6a1e41dc75b8c979838844b4f09d2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298248"
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

*pMeshIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma [**interface ID3DXMesh,**](id3dxmesh.md) que representa a malha de origem.

</dd> <dt>

*pAdjacencyIn* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha a ser simplificado.

</dd> <dt>

*MaxSize* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Número máximo de vértices na malha resultante.

</dd> <dt>

*Opções* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Sinalizadores de opção para as novas malhas.

</dd> <dt>

*pMeshesOut* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de malhas retornadas.

</dd> <dt>

*ppMeshArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de interfaces [**ID3DXMesh**](id3dxmesh.md) para as novas malhas. Para uma malha de origem dividida em n malhas, *ppMeshArrayOut* é uma matriz de n **ponteiros ID3DXMesh.**

</dd> <dt>

*ppAdjacencyArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de DWORDs (matrizes de adjacência) para as novas malhas. Consulte [**ID3DXBuffer.**](id3dxbuffer.md) Esse parâmetro é opcional.

</dd> <dt>

*ppFaceRemapArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de DWORDs (matrizes de remapa facial) para as novas malhas. Consulte [**ID3DXBuffer.**](id3dxbuffer.md) Esse parâmetro é opcional.

</dd> <dt>

*ppVertRemapArrayOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de matrizes de remapa de vértice para as novas malhas. Consulte [**ID3DXBuffer.**](id3dxbuffer.md) Esse parâmetro é opcional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Um uso comum dessa função é dividir uma malha com índices de 32 bits (mais de 65535 vértices) em mais de uma malha, cada uma com índices de 16 bits.

As matrizes de remapa de adjacency, remap de vértice e face são matrizes DWORDs em que cada matriz contém ponteiros n DWORD, seguidos pelos dados DWORD referenciados pelos ponteiros. Por exemplo, para obter as informações de remapeamento facial para face 3 na malha 2, o código a seguir pode ser usado, supondo que os dados de remapeamento facial foram retornados em uma variável chamada *ppFaceRemapArrayOut*.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
