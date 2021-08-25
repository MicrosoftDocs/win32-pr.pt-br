---
description: Função D3DXFresnelTerm (D3dx9math.h) – calcule o termo Fresnel.
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: Função D3DXFresnelTerm (D3dx9math.h)
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
ms.openlocfilehash: 15f0c5bac66d0c1b43bf3938e4ecb1f2fffd8dd235532b5dddc27eb5923ef5f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027646"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>Função D3DXFresnelTerm (D3dx9math.h)

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

*CosTheta* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O valor deve estar entre 0 e 1.

</dd> <dt>

*ReçãoçãoIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O índice de reação de um material. O valor deve ser maior que 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Essa função retorna o termo Fresnel para luz nãopolarizada. CosTheta é o cosseno do ângulo do incidente.

## <a name="remarks"></a>Comentários

Para encontrar o termo Fresnel (F):

Se A for o ângulo de redução e B for o ângulo de refração,


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Em seguida, expandindo usando as identidades trigonométricas e simplificando, você obterá:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
