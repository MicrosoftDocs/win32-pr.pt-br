---
description: Função D3DXMatrixMultiplyTranspose (D3DX10Math. h) – calcula o produto transpodo de duas matrizes.
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Função D3DXMatrixMultiplyTranspose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55bf8dc8eaed13c6bfdc4a8cedacd02b9c5cc5aa11ca0d3e494ed194c8cc9245
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858776"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a>Função D3DXMatrixMultiplyTranspose (D3DX10Math. h)

Calcula o produto transpodo de duas matrizes.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pM1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma estrutura de D3DXMATRIX de origem (lado esquerdo).

</dd> <dt>

*pM2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma estrutura de D3DXMATRIX de origem (lado direito).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que é o produto de duas matrizes.

## <a name="remarks"></a>Comentários

O resultado é o transpodo do produto de duas matrizes de transformação, out = T (M1 \* m2).

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixMultiplyTranspose pode ser usada como um parâmetro para outra função.

Essa função é útil para definir matrizes como constantes para sombreadores de vértices e de pixel.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
