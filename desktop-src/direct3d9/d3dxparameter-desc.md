---
description: Descreve um parâmetro usado para um objeto Effect.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Estrutura de D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172925"
---
# <a name="d3dxparameter_desc-structure"></a>\_Estrutura desc de D3DXPARAMETER

Descreve um parâmetro usado para um objeto Effect.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome do parâmetro.

</dd> <dt>

**Semântico**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Significado semântico, também chamado de uso.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **\_ classe D3DXPARAMETER**](./d3dxparameter-class.md)**

</dd> <dd>

Classe de parâmetro. Defina isso para um dos valores na [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md)**

</dd> <dd>

Tipo de parâmetro. Defina isso para um dos valores no [**\_ tipo D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Linhas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de linhas na matriz.

</dd> <dt>

**Colunas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de colunas na matriz.

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos na matriz.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de anotações.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de membros da estrutura.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Atributos de parâmetro. Consulte [constantes de efeito](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

**Bytes**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

O tamanho do parâmetro, em bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
