---
description: Função D3DXVec2TransformNormalArray (D3dx9math.h) – transforma uma matriz (x, y, 0, 0) por uma determinada matriz.
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: Função D3DXVec2TransformNormalArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f6f64b705ac76c1b4922938d4d08a8bb8f2dd4f75d2433d2bbd8317db67e798c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044604"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a>Função D3DXVec2TransformNormalArray (D3dx9math.h)

Transforma uma matriz (x, y, 0, 0) por uma determinada matriz.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
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

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*OutStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Distância entre vetores no fluxo de dados de saída.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para a matriz [**D3DXVECTOR2 de**](d3dxvector2.md) origem.

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

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é a matriz transformada.

## <a name="remarks"></a>Comentários

Essa função transforma o vetor (*pV-*>x, *pV-*>y, 0, 0) pela matriz apontada *por pM.*

Se você quiser transformar um normal, a matriz que você passar para essa função deverá ser a transposição do inverso da matriz que você usaria para transformar um ponto.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec2TransformNormalArray** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
