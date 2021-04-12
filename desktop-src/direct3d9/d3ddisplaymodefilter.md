---
description: Especifica os tipos de modos de exibição a serem filtrados.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Estrutura D3DDISPLAYMODEFILTER (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298542"
---
# <a name="d3ddisplaymodefilter-structure"></a>Estrutura D3DDISPLAYMODEFILTER

Especifica os tipos de modos de exibição a serem filtrados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tamanho**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

O tamanho desta estrutura. Isso deve sempre ser definido como sizeof (D3DDISPLAYMODEFILTER).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

O formato do modo de exibição a ser filtrado. Consulte [D3DFORMAT](d3dformat.md).

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Se a ordenação de varredura é entrelaçada ou progressiva. Consulte [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
