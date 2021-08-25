---
description: Função D3DXMatrixMultiplyTranspose (D3dx9math. h) – calcula o produto transpodo de duas matrizes.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Função D3DXMatrixMultiplyTranspose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a33f6e1938acb3381d1f14190d3a2e1adbc6afe32147ff793cfc7597f5c3bacc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027366"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a>Função D3DXMatrixMultiplyTranspose (D3dx9math. h)

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

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pM1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.

</dd> <dt>

*pM2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o produto de duas matrizes.

## <a name="remarks"></a>Comentários

O resultado é o transpodo do produto de duas matrizes de transformação, out = T (M1 \* m2).

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXMatrixMultiplyTranspose** pode ser usada como um parâmetro para outra função.

Essa função é útil para definir matrizes como constantes para sombreadores de vértices e de pixel.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> <dt>

[**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




