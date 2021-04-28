---
description: Estrutura de D3DX10_WELD_EPSILONS-especifica valores de tolerância para cada componente de vértice ao comparar vértices para determinar se eles são semelhantes o suficiente para serem soldados juntos.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: Estrutura de D3DX10_WELD_EPSILONS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105424"
---
# <a name="d3dx10_weld_epsilons-structure"></a>Estrutura de 13 de \_ solda de D3DX10 \_

Especifica os valores de tolerância para cada componente de vértice ao comparar vértices para determinar se eles são semelhantes o suficiente para serem soldados juntos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_WELD_EPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Posição**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição

</dd> <dt>

**BlendWeights**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso de mistura

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal

</dd> <dt>

**PSize**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor do tamanho do ponto

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminação especular

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminação difusa

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Oito coordenadas de textura

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente

</dd> <dt>

**Binormal**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal

</dd> <dt>

**TessFactor**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Fator de mosaico

</dd> </dl>

## <a name="remarks"></a>Comentários

O tipo LPD3DXWeldEpsilons é definido como um ponteiro para a estrutura D3DXWeldEpsilons.


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
