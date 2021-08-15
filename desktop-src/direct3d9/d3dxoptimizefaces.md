---
description: Gera um remapeamento facial otimizado para uma lista de triângulos.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Função D3DXOptimizeFaces (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 165f81d9b829ce7a7b22ced6fb37851f926ed861f11b79feca3a63c763dabbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525225"
---
# <a name="d3dxoptimizefaces-function"></a>Função D3DXOptimizeFaces

Gera um remapeamento facial otimizado para uma lista de triângulos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIndices* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para índices de lista de triângulos a ser usado para ordenar vértices.

</dd> <dt>

*NumFaces* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de faces na lista de triângulos. Para malhas de 16 bits, isso é limitado a 2^16 - 1 (65535) ou menos faces.

</dd> <dt>

*NumVertices* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices referenciados pela lista de triângulos.

</dd> <dt>

*Índices32Bit* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Sinalizador que indica o tipo de índice: **TRUE** se os índices são de 32 bits (mais de 65535 índices), **FALSE** se os índices são de 16 bits (65535 ou menos índices).

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o rosto da malha original que foi dividido para gerar o rosto atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O procedimento de otimização dessa função é funcionalmente equivalente a chamar [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) com o sinalizador D3DXMESHOPT DEVICEINDEPENDENT, mas essa função faz uso mais eficiente de caches de \_ vértice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
