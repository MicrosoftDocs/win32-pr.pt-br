---
description: Transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Função D3DXVec2TransformCoord (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0d7e93c2b3a78160f2f1f1ad3342575b4369a057
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772932"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a>Função D3DXVec2TransformCoord (D3DX10Math. h)

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

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Ponteiro para a estrutura de D3DXVECTOR2 de origem.

</dd> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Ponteiro para uma estrutura D3DXVECTOR2 que é o vetor transformado.

## <a name="remarks"></a>Comentários

Essa função transforma o vetor, VP (x, y, 0, 1), pela matriz, pM, projetando o resultado de volta em w = 1.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXVec2TransformCoord pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
