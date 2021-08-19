---
description: Função D3DXVec3TransformNormalArray (D3dx9math.h) – transforma uma matriz (x, y, z, 0) por uma determinada matriz.
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: Função D3DXVec3TransformNormalArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f90521b51c9c939d459fb10bcf2badd7e551b80e5e9f134d5dfd38b5ec8e18aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730814"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a>Função D3DXVec3TransformNormalArray (D3dx9math.h)

Transforma uma matriz (x, y, z, 0) por uma determinada matriz.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
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

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para a [**matriz D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*OutStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de saída.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a matriz [**D3DXVECTOR3 de origem.**](d3dxvector3.md)

</dd> <dt>

*VStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de entrada.

</dd> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX de origem.**](d3dxmatrix.md)

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para uma [**matriz D3DXVECTOR3**](d3dxvector3.md) que é a matriz transformada.

## <a name="remarks"></a>Comentários

Essa função transforma o vetor (*pV*->x, *pV*->y, *pV*->z, 0) pela matriz apontada pelo *pM*.

Se você quiser transformar um normal, a matriz que você passar para essa função deverá ser a transposição do inverso da matriz que você usaria para transformar um ponto.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec3TransformNormalArray** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
