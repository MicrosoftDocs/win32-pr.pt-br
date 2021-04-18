---
description: Gera um remapeamento facial otimizado para uma lista de triângulos.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Função D3DXOptimizeFaces (D3DX9Mesh. h)
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
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781313"
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

*pIndices* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para índices da lista de triângulos a serem usados para ordenar vértices.

</dd> <dt>

*NumFaces* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de rostos na lista de triângulos. Para malhas de 16 bits, isso é limitado a 2 ^ 16-1 (65535) ou menos faces.

</dd> <dt>

*NumVertices* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices referenciados pela lista de triângulos.

</dd> <dt>

*Indices32Bit* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Sinalizador que indica o tipo de índice: **verdadeiro** se os índices forem de 32 bits (mais de 65535 índices), **falso** se os índices forem de 16 bits (65535 ou menos índices).

</dd> <dt>

*pFaceRemap* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para a face de malha original que foi dividida para gerar a face atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O procedimento de otimização da função é funcionalmente equivalente a chamar [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) com o \_ sinalizador D3DXMESHOPT DEVICEINDEPENDENT, mas essa função faz uso mais eficiente de caches de vértice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
