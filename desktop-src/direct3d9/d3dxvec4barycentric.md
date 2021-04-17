---
description: Retorna um ponto nas coordenadas de barycentric, usando os vetores de 4D especificados.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: Função D3DXVec4BaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75f0d068d1545f1b8b55dc3b976d3585e6f9bc88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752366"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a>Função D3DXVec4BaryCentric (D3dx9math. h)

Retorna um ponto nas coordenadas de barycentric, usando os vetores de 4D especificados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.

</dd> <dt>

*pV3* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.

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

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) em coordenadas barycentric.

## <a name="remarks"></a>Comentários

A função **D3DXVec4BaryCentric** fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado. Essa função retorna o ponto resultante usando a seguinte equação: v1 + f (v2-v1) + g (v3-v1).

Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (f, g). O parâmetro *f* controla a quantidade de v2 que é ponderada no resultado e o parâmetro *g* controla a quantidade de v3 ponderada no resultado. Por fim, 1-f-g controla o quanto v1 é ponderado no resultado.

Observe as seguintes relações.

-   Se (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará dentro do triângulo V1V2V3.
-   Se (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará na linha V1V3.
-   Se (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), o ponto estará na linha V1V2.
-   Se (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), o ponto estará na linha V2V3.

As coordenadas de barycentric são uma forma de coordenadas gerais. Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas. O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas Barycentrics.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXVec4BaryCentric** pode ser usada como um parâmetro para outra função.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
