---
description: Calcule o termo Fresnel.
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: Função D3DXFresnelTerm (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6c6dd19dd6b7b70c5eeb08051f9799756b0782
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298618"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>Função D3DXFresnelTerm (D3dx9math. h)

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

## <a name="return-value"></a>Retornar valor

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
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
