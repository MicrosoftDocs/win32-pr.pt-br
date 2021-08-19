---
description: Função D3DXComputeBoundingBox (D3DX9Mesh. h) – computa uma caixa delimitadora orientada a eixo de coordenadas.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Função D3DXComputeBoundingBox (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03eb722e68b58ec48a3bf607ab72d67004ad30a0c765b19c1b84ae29577c773b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299948"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a>Função D3DXComputeBoundingBox (D3DX9Mesh. h)

Computa uma caixa delimitadora orientada a eixo de coordenadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFirstPosition* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a primeira posição.

</dd> <dt>

*NumVertices* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices.

</dd> <dt>

*dwStride* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Contagem ou número de bytes entre vértices.

</dd> <dt>

*pMin* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , descrevendo o canto inferior esquerdo retornado da caixa delimitadora. Consulte Observações.

</dd> <dt>

*pMax* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , descrevendo o canto superior direito retornado da caixa delimitadora. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
