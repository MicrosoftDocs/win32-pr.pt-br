---
description: Função D3DXVec3TransformCoordArray (D3DX10Math.h) – transforma uma matriz (x, y, z, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: Função D3DXVec3TransformCoordArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 27f0187f3533b6cb7c9782ddaa0f59692a15335ebb27b86184b2b5544d44fe5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895326"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a>Função D3DXVec3TransformCoordArray (D3DX10Math.h)

Transforma uma matriz (x, y, z, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para [**o D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*OutStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de saída.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para a matriz D3DXVECTOR3 de origem.

</dd> <dt>

*VStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de entrada.

</dd> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX de origem.**](d3d10-d3dxmatrix.md)

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para uma estrutura D3DXVECTOR3 que é a matriz transformada.

## <a name="remarks"></a>Comentários

Essa função transforma a matriz pV (x, y, z, 1) pela matriz pM, projetando o resultado de volta em w = 1.

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a [**função D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
