---
description: Estrutura auxiliar para gerenciar uma tabela de constante de sombreador. Isso também pode ser feito usando o ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Estrutura de D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788741"
---
# <a name="d3dxshader_constanttable-structure"></a>\_Estrutura de constante D3DXSHADER

Estrutura auxiliar para gerenciar uma tabela de constante de sombreador. Isso também pode ser feito usando o [**ID3DXConstantTable**](id3dxconstanttable.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tamanho**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho da estrutura. Consulte Observações.

</dd> <dt>

**Criador**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset do início desta estrutura, em bytes, para a cadeia de caracteres que contém o nome do criador.

</dd> <dt>

**Versão**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Versão do sombreador.

</dd> <dt>

**Constantes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de constantes.

</dd> <dt>

**ConstantInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de informações constantes, \_ constantes D3DXSHADER CONSTANTINFO \[  \] . Consulte [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Os sinalizadores de [sinalizadores D3DXSHADER](d3dxshader-flags.md) usados para compilar o sombreador.

</dd> <dt>

**Target (destino)**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento na cadeia de caracteres que contém o destino.

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações constantes do sombreador estão incluídas em uma tabela de comentários delimitada por tabulação. Todos os deslocamentos são medidos em bytes desde o início da estrutura. As entradas na tabela de constantes são classificadas por criador em ordem crescente.

Uma tabela de constantes de sombreador pode ser gerenciada com as interfaces [**ID3DXConstantTable**](id3dxconstanttable.md) . Como alternativa, você pode gerenciar a tabela constante com **a \_ constante D3DXSHADER**.

Esse membro de tamanho geralmente é inicializado usando o seguinte:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
