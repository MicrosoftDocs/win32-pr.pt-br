---
description: Uma estrutura auxiliar que contém informações de tipo de membro.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Estrutura de D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298592"
---
# <a name="d3dxshader_typeinfo-structure"></a>\_Estrutura de TYPEINFO D3DXSHADER

Uma estrutura auxiliar que contém informações de tipo de membro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo de objeto Shader. Consulte [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo de dados. Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Linhas**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de linhas de matriz (matrizes).

</dd> <dt>

**Colunas**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de colunas (vetores e matrizes).

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensão da matriz.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de membros da estrutura.

</dd> <dt>

**StructMemberInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de informações de membro de estrutura, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] . Consulte [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações de tipo fazem parte de [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
