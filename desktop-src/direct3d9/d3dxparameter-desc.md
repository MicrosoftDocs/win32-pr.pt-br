---
description: Descreve um parâmetro usado para um objeto de efeito.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: D3DXPARAMETER_DESC (D3dx9effect.h)
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
ms.openlocfilehash: a12541e9bfb33979b11f8198e218a3eb474f948aeb8c74982a5369eed782eaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631146"
---
# <a name="d3dxparameter_desc-structure"></a>Estrutura D3DXPARAMETER \_ DESC

Descreve um parâmetro usado para um objeto de efeito.

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

**Semântica**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Significado semântico, também chamado de uso.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **CLASSE D3DXPARAMETER \_**](./d3dxparameter-class.md)**

</dd> <dd>

Classe de parâmetro. De definido como um dos valores em [**D3DXPARAMETER \_ CLASS**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md)**

</dd> <dd>

Tipo de parâmetro. De definido como um dos valores em [**D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md).

</dd> <dt>

**Linhas**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de linhas na matriz.

</dd> <dt>

**Colunas**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de colunas na matriz.

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos na matriz.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de anotações.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de membros da estrutura.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Atributos de parâmetro. Consulte [Constantes de efeito](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

**Bytes**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

O tamanho do parâmetro, em bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
