---
description: Função D3DXMatrixReflect (D3DX10Math.h) – cria uma matriz que reflete o sistema de coordenadas sobre um plano.
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: Função D3DXMatrixReflect (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c744c529025e0bfa1a619d41cc3e564c2be3203887b1ebbbbe047542ccce3370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810031"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a>Função D3DXMatrixReflect (D3DX10Math.h)

Cria uma matriz que reflete o sistema de coordenadas sobre um plano.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para a [**estrutura D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pPlane* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ponteiro para o [**D3DXPLANE de origem.**](d3d10-d3dxplane.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que reflete o sistema de coordenadas sobre o plano de origem.

## <a name="remarks"></a>Comentários

Essa função normaliza a equação do plano antes de criar a matriz refletida.

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixReflect pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
