---
description: Função D3DXMatrixReflect (D3dx9math. h) – compila uma matriz que reflete o sistema de coordenadas sobre um plano.
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: Função D3DXMatrixReflect (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4118a5f0a1cd997d5fab5fecebae449d4c30b09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118214"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a>Função D3DXMatrixReflect (D3dx9math. h)

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

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pPlane* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Ponteiro para a estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que reflete o sistema de coordenadas sobre o plano de origem.

## <a name="remarks"></a>Comentários

Essa função normaliza a equação do plano antes de criar a matriz refletida.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXMatrixReflect** pode ser usada como um parâmetro para outra função.

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
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




