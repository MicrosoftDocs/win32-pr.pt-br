---
description: Identifica os dados de memória.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Estrutura de D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930596"
---
# <a name="d3dxf_fileloadmemory-structure"></a>\_Estrutura D3DXF FILELOADMEMORY

Identifica os dados de memória.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>Membros

<dl> <dt>

**lpMemory**
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para um bloco de memória a ser carregado.

</dd> <dt>

**dSize**
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho do bloco de memória a ser carregado, em bytes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura identifica os dados a serem carregados da memória quando um aplicativo usa o método [**Createenumobject**](id3dxfile--createenumobject.md) e especifica o \_ sinalizador FROMMEMORY do D3DXF fileload \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
