---
description: Retorna o tamanho de um vértice da declaração de vértice.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: Função D3DXGetDeclVertexSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798528"
---
# <a name="d3dxgetdeclvertexsize-function"></a>Função D3DXGetDeclVertexSize

Retorna o tamanho de um vértice da declaração de vértice.

## <a name="syntax"></a>Sintaxe


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDecl* \[ no\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Um ponteiro para a declaração de vértice. Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*Fluxo* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

O índice de fluxo com base em zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O tamanho da declaração de vértice, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
