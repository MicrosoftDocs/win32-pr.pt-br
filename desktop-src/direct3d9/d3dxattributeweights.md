---
description: Especifica os atributos de peso de malha.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Estrutura D3DXATTRIBUTEWEIGHTS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793980"
---
# <a name="d3dxattributeweights-structure"></a>Estrutura D3DXATTRIBUTEWEIGHTS

Especifica os atributos de peso de malha.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
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

O tipo LPD3DXATTRIBUTEWEIGHTS é definido como um ponteiro para a estrutura **D3DXATTRIBUTEWEIGHTS** .


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
