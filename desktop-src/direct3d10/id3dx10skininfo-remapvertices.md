---
description: Alterar quais vértices são influenciados por qual esqueleto.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: Método ID3DX10SkinInfo::RemapVertices (D3DX10.h)
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
ms.openlocfilehash: d73b9878a43ef876174561f16678f78787b15b88f423ecfb3f1765bd82c84630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302472"
---
# <a name="id3dx10skininforemapvertices-method"></a>Método ID3DX10SkinInfo::RemapVertices

Alterar quais vértices são influenciados por qual esqueleto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewVertexCount* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O novo número de vértices.

</dd> <dt>

*pVertexRemap* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Um ponteiro para uma matriz de índices de vértice, que descrevem o remapeamento. Por exemplo, digamos que SkinInfo contenha alguns vértices, de forma que seja mapeado para v0, hop1 a v1 e hop2 a v2, e a matriz com 2,1,0 seja especificada para pBoneRemap. Isso fará com que o 10 seja mapeado para v2, ltd1 a v1 e para v0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY ou E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
