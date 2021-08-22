---
description: Função D3DXMatrixShadow (D3dx9math.h) – cria uma matriz que nivela a geometria em um plano.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: Função D3DXMatrixShadow (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e8d2b476d57306261d9261215a1e5053827a972412fa78b76cf0d136fbf97e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460296"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a>Função D3DXMatrixShadow (D3dx9math.h)

Cria uma matriz que nivela a geometria em um plano.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a [**estrutura D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pLight* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR4**](d3dxvector4.md) que descreve a posição da luz.

</dd> <dt>

*pPlane* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Ponteiro para a estrutura [**D3DXPLANE de origem.**](d3dxplane.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma [**estrutura D3DXMATRIX**](d3dxmatrix.md) que nivela a geometria em um plano.

## <a name="remarks"></a>Comentários

A **função D3DXMatrixShadow** nivela a geometria em um plano, como se estivesse lançando uma sombra de uma luz.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXMatrixShadow** pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



Se o componente w da luz for 0, o raio da origem para a luz representará uma luz direcional. Se for 1, a luz será uma luz de ponto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




