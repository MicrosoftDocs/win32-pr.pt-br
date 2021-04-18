---
description: Gera um remapeamento de vértice otimizado para uma lista de triângulos. Essa função é comumente usada após a aplicação do remapeamento facial gerado por D3DXOptimizeFaces.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: Função D3DXOptimizeVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 734c2224ae29e7ab166010d59859d00355e5400e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105795459"
---
# <a name="d3dxoptimizevertices-function"></a>Função D3DXOptimizeVertices

Gera um remapeamento de vértice otimizado para uma lista de triângulos. Essa função é comumente usada após a aplicação do remapeamento facial gerado por [**D3DXOptimizeFaces**](d3dxoptimizefaces.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIndices* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para índices da lista de triângulos a serem usados para ordenar vértices.

</dd> <dt>

*NumFaces* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de rostos na lista de triângulos.

</dd> <dt>

*NumVertices* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices referenciados pela lista de triângulos.

</dd> <dt>

*Indices32Bit* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Sinalizador que indica o tipo de índice: **verdadeiro** se os índices forem de 32 bits (mais de 65535 vértices), **falso** se os índices forem de 16 bits (65535 ou menos vértices).

</dd> <dt>

*pVertexRemap* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para um buffer de destino que conterá o novo índice para cada vértice. O valor armazenado em *pVertexRemap* para um determinado elemento é o local do vértice de origem na nova ordenação de vértice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Por padrão, uma malha usa índices de 16 bits quando ele é criado, a menos que o aplicativo especifique o contrário. Para verificar se uma malha existente usa índices de 16 ou 32 bits, chame [**ID3DXBaseMesh:: getoptions**](id3dxbasemesh--getoptions.md) e verifique o sinalizador de 32 bits do D3DXMESH \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
