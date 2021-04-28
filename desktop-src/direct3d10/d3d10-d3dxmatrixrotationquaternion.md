---
description: Função D3DXMatrixRotationQuaternion (D3DX10Math. h) – compila uma matriz de rotação de um Quaternion.
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: Função D3DXMatrixRotationQuaternion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d95d28b7f7106df9ddfb43a9175f5c19292d52c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103424"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a>Função D3DXMatrixRotationQuaternion (D3DX10Math. h)

Cria uma matriz de rotação de um Quaternion.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pQ* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para a estrutura de D3DXQUATERNION de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX criada a partir do Quaternion de origem.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixRotationQuaternion pode ser usada como um parâmetro para outra função.

Para obter informações sobre como calcular valores de Quaternion de um vetor de direção (x, y, z) e um ângulo de rotação, consulte [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
