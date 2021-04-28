---
description: Função D3DXSHEvalDirection (D3DX10. h) – avalia as funções de base esférica harmônica (SH) de um vetor de direção de entrada.
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: Função D3DXSHEvalDirection (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7fa1f94d65ca8096a0398d71ca2f562b643d47a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108584"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a>Função D3DXSHEvalDirection (D3DX10. h)

Avalia as funções de base esférica harmônica (SH) de um vetor de direção de entrada.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para os coeficientes de saída harmônicas (SH). A avaliação gera coeficientes do Order ². Consulte Observações.

</dd> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*pDir* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

(x, y, z) vetor de direção no qual avaliar as funções de base SH. Deve ser normalizado. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para SH coeficientes de saída. Consulte Observações.

## <a name="remarks"></a>Comentários

Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:

-   l é o grau da função base.
-   m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.

Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na direção da mão direita e Phi, o ângulo de z.

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade. O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
