---
description: Função D3DXVec2TransformArray (D3DX10Math.h) – transforma uma matriz (x, y, 0, 1) por uma determinada matriz.
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: Função D3DXVec2TransformArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a795590530503819ae66d1e17f9a4c8f8236dfb3015af512f4c6e28d084ca778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989896"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a>Função D3DXVec2TransformArray (D3DX10Math.h)

Transforma uma matriz (x, y, 0, 1) por uma determinada matriz.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para a [**estrutura D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*OutStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de saída.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Ponteiro para o [**D3DXVECTOR2 de origem.**](d3d10-d3dxvector2.md)

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

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para uma estrutura D3DXVECTOR4 que é a matriz transformada.

## <a name="remarks"></a>Comentários

Essa função transforma a matriz pV (x, y, 0, 1) pela matriz pM.

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a [**função D3DXVec2Transform**](d3d10-d3dxvec2transform.md) pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
