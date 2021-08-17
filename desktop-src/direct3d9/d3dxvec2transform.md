---
description: Função D3DXVec2Transform (D3dx9math.h) – transforma um vetor 2D por uma determinada matriz.
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: Função D3DXVec2Transform (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2115b804dfda537508247785d897757a3f25263e8ee528fdacfb1a91b0515045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730795"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a>Função D3DXVec2Transform (D3dx9math.h)

Transforma um vetor 2D por uma determinada matriz.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para a estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem.

</dd> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX de origem.**](d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é o vetor transformado.

## <a name="remarks"></a>Comentários

Essa função transforma o *vetor pV* (x, y, 0, 1) pela *matriz pM*.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec2Transform** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2TransformCoord**](d3dxvec2transformcoord.md)
</dt> <dt>

[**D3DXVec2TransformNormal**](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




