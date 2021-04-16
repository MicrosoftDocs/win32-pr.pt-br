---
description: Altere quais vértices são influenciados por quais Bones.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'Método ID3DX10SkinInfo:: RemapVertices (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765319"
---
# <a name="id3dx10skininforemapvertices-method"></a>Método ID3DX10SkinInfo:: RemapVertices

Altere quais vértices são influenciados por quais Bones.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewVertexCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O novo número de vértices.

</dd> <dt>

*pVertexRemap* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Um ponteiro para uma matriz de índices de vértice, que descrevem o remapeamento. Por exemplo, digamos que SkinInfo contenha alguns vértices de modo que bone0 seja mapeado para V0, bone1 para v1 e bone2 para v2, e matriz com 2, 1, 0 seja especificado para pBoneRemap. Isso fará com que bone0 seja mapeado para v2, bone1 para v1 e bone2 para V0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY ou E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
