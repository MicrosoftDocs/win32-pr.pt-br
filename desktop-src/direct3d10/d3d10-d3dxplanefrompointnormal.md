---
description: Constrói um plano de um ponto e um normal.
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: Função D3DXPlaneFromPointNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9900a9f6838e253bd195374d00f90ee31fae07a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772719"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a>Função D3DXPlaneFromPointNormal (D3DX10Math. h)

Constrói um plano de um ponto e um normal.

## <a name="syntax"></a>Sintaxe


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md) que é o resultado da operação.

</dd> <dt>

*pPoint* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), definindo o ponto usado para construir o plano.

</dd> <dt>

*pNormal* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3, definindo o normal usado para construir o plano.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para a estrutura D3DXPLANE construída a partir do ponto e do normal.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXPlaneFromPointNormal pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
