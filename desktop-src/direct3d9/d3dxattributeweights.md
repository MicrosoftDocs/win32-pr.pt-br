---
description: Estrutura D3DXATTRIBUTEWEIGHTS – especifica atributos de peso da malha.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Estrutura D3DXATTRIBUTEWEIGHTS (D3dx9mesh.h)
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
ms.openlocfilehash: fa40476bdd1f65dddf0f78b57cfca2b20ac7bd8186eaf78546ddda9b3fa8771a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096591"
---
# <a name="d3dxattributeweights-structure"></a>Estrutura D3DXATTRIBUTEWEIGHTS

Especifica atributos de peso da malha.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posição.

</dd> <dt>

**Limite**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso da mistura.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal.

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminação difusa.

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valor de iluminação especular.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Oito coordenadas de textura.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormal**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura descreve como uma operação de simplificação considerará dados de vértice ao calcular os custos relativos entre bordas de redução. Por exemplo, se o campo Normal for 0,0, a operação de simplificação ignorará o componente normal do vértice ao calcular o erro para o ressalvamento. No entanto, se o campo Normal for 1.0, a operação de simplificação usará o componente normal do vértice. Se o campo Normal for 2.0, dobre a quantidade de erros; se o campo Normal for 4.0, quadruplicar o número de erros e assim por diante.

O tipo LPD3DXATTRIBUTEWEIGHTS é definido como um ponteiro para a **estrutura D3DXATTRIBUTEWEIGHTS.**


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
