---
description: Função D3DXVec3TransformCoord (D3DX10Math. h) – transforma um vetor 3D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: Função D3DXVec3TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5b3e763d87503f9ca71911ad40ccf3c6ae9ca722
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108094"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a>Função D3DXVec3TransformCoord (D3DX10Math. h)

Transforma um vetor 3D por uma determinada matriz, projetando o resultado de volta em w = 1.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para a estrutura de D3DXVECTOR3 de origem.

</dd> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para uma estrutura D3DXVECTOR3 que é o vetor transformado.

## <a name="remarks"></a>Comentários

Essa função transforma o vetor, VP (x, y, z, 1), pela matriz, pM, projetando o resultado de volta em w = 1.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXVec3TransformCoord pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
