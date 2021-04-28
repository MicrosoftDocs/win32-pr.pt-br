---
description: Função D3DXFresnelTerm (D3DX10Math. h) – calcular o termo de Fresnel.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Função D3DXFresnelTerm (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9efa557d44451674d2ae4c48a58370e939760a03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113264"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>Função D3DXFresnelTerm (D3DX10Math. h)

Calcule o termo Fresnel.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CosTheta* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O valor deve estar entre 0 e 1.

</dd> <dt>

*RefractionIndex* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O índice de refração de um material. O valor deve ser maior que 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Essa função retorna o termo Fresnel para uma luz não polarizada. CosTheta é o cosseno do ângulo do incidente.

## <a name="remarks"></a>Comentários

Para localizar o termo de Fresnel (F):

Se um for um ângulo de incidência e B for o ângulo de refração, então


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Em seguida, expandindo o usando as identidades trigonométricas e simplificando, você obtém:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
