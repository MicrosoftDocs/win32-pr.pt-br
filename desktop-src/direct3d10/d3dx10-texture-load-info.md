---
description: Descreve os parâmetros usados para carregar uma textura de outra textura.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Estrutura de D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772741"
---
# <a name="d3dx10_texture_load_info-structure"></a>\_Estrutura de \_ informações de carregamento de textura D3DX10 \_

Descreve os parâmetros usados para carregar uma textura de outra textura.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**pSrcBox**
</dt> <dd>

Tipo: **[ **\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Caixa de textura de origem (consulte a [**\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Caixa textura de destino (consulte a [**\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nível de mipmap de textura de origem, consulte [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obter mais detalhes.

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nível de mipmap de textura de destino, consulte [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obter mais detalhes.

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de níveis de mipmap na textura de origem.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Primeiro elemento da textura de origem.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Primeiro elemento da textura de destino.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos a serem carregados.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opções de filtragem durante a reamostragem (consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opções de filtragem ao gerar níveis MIP (consulte o [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada em uma chamada para [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
