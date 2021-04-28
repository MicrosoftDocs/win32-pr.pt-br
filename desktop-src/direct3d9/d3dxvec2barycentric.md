---
description: Função D3DXVec2BaryCentric (D3dx9math. h) – retorna um ponto em coordenadas barycentric, usando os vetores 2D especificados.
ms.assetid: afbffe6d-d786-4d65-b737-ae201613d1ac
title: Função D3DXVec2BaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3210624087a3d1d5a612ba1eb628e7d85ba4fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117784"
---
# <a name="d3dxvec2barycentric-function-d3dx9mathh"></a>Função D3DXVec2BaryCentric (D3dx9math. h)

Retorna um ponto em coordenadas barycentric, usando os vetores 2D especificados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _Out_       D3DXVECTOR2 *pOut,
  _In_  const D3DXVECTOR2 *pV1,
  _In_  const D3DXVECTOR2 *pV2,
  _In_  const D3DXVECTOR2 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.

</dd> <dt>

*pV3* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.

</dd> <dt>

*f* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> <dt>

*g* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) em coordenadas barycentric.

## <a name="remarks"></a>Comentários

A função **D3DXVec2BaryCentric** fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado. Essa função retorna o ponto resultante usando a seguinte equação: v1 + f (v2-v1) + g (v3-v1).

Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (f, g). O parâmetro *f* controla a quantidade de v2 que é ponderada no resultado, e o parâmetro *g* controla a quantidade de v3 ponderada no resultado. Por fim, 1-f-g controla o quanto v1 é ponderado no resultado.

Observe as seguintes relações.

-   Se (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará dentro do triângulo V1V2V3.
-   Se (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará na linha V1V3.
-   Se (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), o ponto estará na linha V1V2.
-   Se (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), o ponto estará na linha V2V3.

As coordenadas de barycentric são uma forma de coordenadas gerais. Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas. O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas Barycentrics.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXVec2BaryCentric** pode ser usada como um parâmetro para outra função.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html). (Esse recurso pode não estar disponível em alguns idiomas e países.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
