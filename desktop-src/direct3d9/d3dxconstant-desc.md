---
description: Uma descrição de uma constante em uma tabela constante.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: Estrutura de D3DXCONSTANT_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: bdb3b8276711f3165c0c138155eb6e628c19a124d6f9301de7638e5be24d1c1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952446"
---
# <a name="d3dxconstant_desc-structure"></a>\_Estrutura desc de D3DXCONSTANT

Uma descrição de uma constante em uma tabela constante.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome da constante.

</dd> <dt>

**Registroset**
</dt> <dd>

Tipo: **[ **D3DXREGISTER \_ definido**](./d3dxregister-set.md)**

</dd> <dd>

Tipo de dados Constant. Consulte [**D3DXREGISTER \_ set**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice de base zero da constante na tabela.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de registros que contêm dados.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **\_ classe D3DXPARAMETER**](./d3dxparameter-class.md)**

</dd> <dd>

Classe de parâmetro. Consulte [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md)**

</dd> <dd>

Tipo de parâmetro. Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Linhas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de linhas.

</dd> <dt>

**Colunas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de colunas.

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos na matriz.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de subparâmetros de membro de estrutura.

</dd> <dt>

**Bytes**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho dos dados em número de bytes.

</dd> <dt>

**ValorPadrão**
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para o valor padrão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
