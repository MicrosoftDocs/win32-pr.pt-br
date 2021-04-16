---
description: Características de material de PRT (transferência de radiante computacional) de harmônica esférica (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Estrutura D3DXSHMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808346"
---
# <a name="d3dxshmaterial-structure"></a>Estrutura D3DXSHMATERIAL

Características de material de PRT (transferência de radiante computacional) de harmônica esférica (SH).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a>Membros

<dl> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Albedo difuso da superfície. Esse valor será ignorado se o objeto for um espelho.

</dd> <dt>

**bMirror**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Deve ser definido como **false**.

</dd> <dt>

**bSubSurf**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Defina como **true** para habilitar a dispersão de subsuperfície; qualquer objeto que faça a dispersão da subsuperfície não pode ser um espelho.

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O índice relativo de refração é a proporção entre dois índices absolutos de refração. Um índice de refração é a proporção do seno do ângulo de incidência para o seno do ângulo de refração.

</dd> <dt>

**Absorção**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

O coeficiente de absorção é um parâmetro para a equação de renderização de volume usado para modelar a propagação clara em uma mídia participante.

</dd> <dt>

**ReducedScattering**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

O coeficiente de dispersão reduzida é um parâmetro para a equação de renderização de volume usado para modelar a propagação clara em uma mídia de participação.

</dd> </dl>

## <a name="remarks"></a>Comentários

As cenas não Spectrals usam o canal vermelho dos materiais em vez do valor de luminância.

Para obter mais informações sobre o PRT, consulte:

-   Jensen, Henrik Wann, et al. SIGGRAPH procedimentos: um modelo prático para transporte de luz de subsuperfície, 2001.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
