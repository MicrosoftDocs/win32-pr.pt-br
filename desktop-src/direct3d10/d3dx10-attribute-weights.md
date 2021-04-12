---
description: Especifica os atributos de peso de malha.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Estrutura de D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298671"
---
# <a name="d3dx10_attribute_weights-structure"></a>Estrutura de pesos de \_ atributo D3DX10 \_

Especifica os atributos de peso de malha.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Posição**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição.

</dd> <dt>

**Limite**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso de mistura.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal.

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminação difusa.

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminação especular.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Oito coordenadas de textura.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormal**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta estrutura descreve como uma operação de simplificação considerará os dados de vértice ao calcular os custos relativos entre as bordas de recolhimento. Por exemplo, se o campo normal for 0,0, a operação de simplificação irá ignorar o componente normal de vértice ao calcular o erro para o recolhimento. No entanto, se o campo normal for 1,0, a operação de simplificação usará o componente normal de vértice. Se o campo normal for 2,0, dobrar a quantidade de erros; Se o campo normal for 4,0, o número de erros será quádruplo e assim por diante.

O \_ tipo de pesos do atributo LPD3DX \_ é definido como um ponteiro para a \_ estrutura de pesos do atributo D3DX \_ .


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
