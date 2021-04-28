---
description: Função D3DXVec2TransformCoord (D3dx9math. h) – transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: Função D3DXVec2TransformCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 717af9eed2c7cedae7ac292a19239e13521dfa74
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115664"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a>Função D3DXVec2TransformCoord (D3dx9math. h)

Transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.

</dd> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o vetor transformado.

## <a name="remarks"></a>Comentários

Essa função transforma o vetor, *VP* (x, y, 0, 1), pela matriz, *PM*, projetando o resultado de volta em w = 1.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXVec2TransformCoord** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Transform**](d3dxvec2transform.md)
</dt> <dt>

[**D3DXVec2TransformNormal**](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




