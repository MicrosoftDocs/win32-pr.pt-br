---
description: Transforma uma matriz (x, y, 0, 1) por uma determinada matriz.
ms.assetid: ba8c1983-bd65-4249-9451-69d813e4a3a4
title: Função D3DXVec2TransformArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf95c4b8ffd9fd2804b4168609e60ff7278d1209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663993"
---
# <a name="d3dxvec2transformarray-function-d3dx9mathh"></a>Função D3DXVec2TransformArray (D3dx9math. h)

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

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*Didistância* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride entre os vetores no fluxo de dados de saída.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.

</dd> <dt>

*VStride* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride entre os vetores no fluxo de dados de entrada.

</dd> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é a matriz transformada.

## <a name="remarks"></a>Comentários

Essa função transforma a matriz *PV* (x, y, 0, 1) pela matriz *PM*.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função [**D3DXVec2Transform**](d3dxvec2transform.md) pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2TransformCoord**](d3dxvec2transformcoord.md)
</dt> <dt>

[**D3DXVec2TransformNormal**](d3dxvec2transformnormal.md)
</dt> </dl>

 

 
