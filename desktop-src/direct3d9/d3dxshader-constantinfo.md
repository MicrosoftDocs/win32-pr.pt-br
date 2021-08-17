---
description: '\_Estrutura D3DXSHADER CONSTANTINFO'
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Estrutura de D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 34a9238ac7ab401a25874d65390ccfacb4dba68a9ccc4438500a1171e25e5e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122826"
---
# <a name="d3dxshader_constantinfo-structure"></a>\_Estrutura D3DXSHADER CONSTANTINFO

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início desta estrutura, em bytes, para a cadeia de caracteres que contém as informações de constante.

</dd> <dt>

**Registroset**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Conjunto de registros. Consulte [**D3DXREGISTER \_ set**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

O índice de registro.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de registros.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Reservado.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset do início desta estrutura, em bytes, para a cadeia de caracteres que contém as informações do [**\_ TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md) .

</dd> <dt>

**ValorPadrão**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início desta estrutura, em bytes, para a cadeia de caracteres que contém o valor padrão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
