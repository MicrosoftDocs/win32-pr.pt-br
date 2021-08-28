---
description: Características de material de PRT (transferência de radiance) pré-comutada (SH) esférica.
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Estrutura D3DXSHMATERIAL (D3dx9mesh.h)
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
ms.openlocfilehash: 4bfbf00c7d8654ad851ca8c691c9f028c09648219dbe76bb4ef07fe3b830e4d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849716"
---
# <a name="d3dxshmaterial-structure"></a>Estrutura D3DXSHMATERIAL

Características de material de PRT (transferência de radiance) pré-comutada (SH) esférica.

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

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Deve ser definido como **FALSE.**

</dd> <dt>

**bSubSurf**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Definido como **TRUE para** habilitar o dispersão de subsuficiência; qualquer objeto que faça dispersão de sub-superfície não pode ser um espelho.

</dd> <dt>

**RelativeIndexOfRedexion**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O índice relativo de reação é a proporção entre dois índices absolutos de refração. Um índice de reação é a proporção do seno do ângulo de redução para o seno do ângulo de refração.

</dd> <dt>

**Absorção**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

O coeficiente de absorção é um parâmetro para a equação de renderização de volume usada para modelar a propagação de luz em uma mídia participante.

</dd> <dt>

**ReducedScattering**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

O coeficiente de dispersão reduzido é um parâmetro para a equação de renderização de volume usada para modelar a propagação de luz em uma mídia participante.

</dd> </dl>

## <a name="remarks"></a>Comentários

Cenas não especificais usam o canal vermelho dos materiais em vez do valor de luminância.

Para obter mais informações sobre PRT, consulte:

-   Clara, Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
