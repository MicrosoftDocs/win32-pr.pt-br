---
description: Função D3DXVec3BaryCentric (D3dx9math.h) – retorna um ponto em coordenadas centradas em barras, usando os vetores 3D especificados.
ms.assetid: ecbabc76-9936-4f31-adec-1ec807984787
title: Função D3DXVec3BaryCentric (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e20e0f632fc25f25f5eedc76491cc7835a19e225dd0742a2a4647cdba1894e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297852"
---
# <a name="d3dxvec3barycentric-function-d3dx9mathh"></a>Função D3DXVec3BaryCentric (D3dx9math.h)

Retorna um ponto em coordenadas centradas em barras, usando os vetores 3D especificados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _Out_       D3DXVECTOR3 *pOut,
  _In_  const D3DXVECTOR3 *pV1,
  _In_  const D3DXVECTOR3 *pV2,
  _In_  const D3DXVECTOR3 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para a [**estrutura D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> <dt>

*pV3* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> <dt>

*f* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> <dt>

*g* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR3**](d3dxvector3.md) em coordenadas centradas em barras.

## <a name="remarks"></a>Comentários

A **função D3DXVec3BaryCentric** fornece uma maneira de entender os pontos dentro e ao redor de um triângulo, independentemente de onde o triângulo está realmente localizado. Essa função retorna o ponto resultante usando a seguinte equação: V1 + f(V2-V1) + g(V3-V1).

Qualquer ponto no plano V1V2V3 pode ser representado pela coordenada centrada em barras (f,g). O parâmetro *f* controla quanto V2 é ponderado no resultado e o parâmetro *g* controla quanto V3 é ponderado no resultado. Por fim, 1-f-g controla quanto V1 é ponderado no resultado.

Observe as relações a seguir.

-   Se (f>=0 &, & g>=0 &, & 1-f-g>=0), o ponto está dentro do triângulo V1V2V3.
-   Se (f==0 &, & g>=0 &, & 1-f-g>=0), o ponto está na linha V1V3.
-   Se (f>=0 &, & g==0 &, & 1-f-g>=0), o ponto está na linha V1V2.
-   Se (f>=0 &, & g>=0 &, & 1-f-g==0), o ponto está na linha V2V3.

Coordenadas barycentric são uma forma de coordenadas gerais. Nesse contexto, o uso de coordenadas centradas em barras representa uma alteração em sistemas de coordenadas. O que é verdadeiro para coordenadas cartesianas é verdadeiro para coordenadas centradas em barras.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec3BaryCentric** pode ser usada como um parâmetro para outra função.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas centradas em barras, consulte Descrição de [coordenadas barycentric da Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
