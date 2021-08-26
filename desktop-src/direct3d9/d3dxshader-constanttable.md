---
description: Estrutura auxiliar para gerenciar uma tabela constante do sombreador. Isso também pode ser feito usando ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE estrutura (D3dx9shader.h)
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
ms.openlocfilehash: f423eba3187c6bbc5c17d4ba9284e4e1b2048a016b8a11744b83b46e4d8522af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027286"
---
# <a name="d3dxshader_constanttable-structure"></a>Estrutura CONSTANTTABLE D3DXSHADER \_

Estrutura auxiliar para gerenciar uma tabela constante do sombreador. Isso também pode ser feito usando [**ID3DXConstantTable.**](id3dxconstanttable.md)

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

Deslocamento do início dessa estrutura, em bytes, para a cadeia de caracteres que contém o nome do criador.

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

Matriz de informações constantes, \_ \[ *constantes* CONSTANTINFO D3DXSHADER \] . Consulte [**\_ CONSTANTINFO D3DXSHADER**](d3dxshader-constantinfo.md).

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Os [sinalizadores D3DXSHADER usados](d3dxshader-flags.md) para compilar o sombreador.

</dd> <dt>

**Target (destino)**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento para a cadeia de caracteres que contém o destino.

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações constantes do sombreador são incluídas em uma tabela de comentários delimitada por tabulação. Todos os deslocamentos são medidos em bytes do início da estrutura. As entradas na tabela constante são ordenadas pelo Criador em ordem crescente.

Uma tabela constante do sombreador pode ser gerenciada com as interfaces [**ID3DXConstantTable.**](id3dxconstanttable.md) Como alternativa, você pode gerenciar a tabela constante com **D3DXSHADER \_ CONSTANTTABLE**.

Esse membro de tamanho geralmente é inicializado usando o seguinte:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
