---
description: Retorna o componente z assumindo o produto cruzado de dois vetores 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Função D3DXVec2CCW (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b38adaf28b6e2394608cfb6f73f4a39d803d4fd5106f826d810a5c8dfd02618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630696"
---
# <a name="d3dxvec2ccw-function"></a>Função D3DXVec2CCW

Retorna o componente z assumindo o produto cruzado de dois vetores 2D.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O componente z.

## <a name="remarks"></a>Comentários

Essa função determina o componente z determinando o produto cruzado com base na seguinte fórmula: ((x1, y1, 0) Cross (x2, Y2, 0)). Ou conforme mostrado no exemplo a seguir.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Se o valor do componente z for positivo, o vetor v2 será no sentido anti-horário do vetor v1. Essas informações são úteis para a remoção de face para frente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
