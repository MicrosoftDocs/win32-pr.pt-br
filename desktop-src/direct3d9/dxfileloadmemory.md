---
description: Identifica os dados de memória. Preterido.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Estrutura DXFILELOADMEMORY (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813743"
---
# <a name="dxfileloadmemory-structure"></a>Estrutura DXFILELOADMEMORY

Identifica os dados de memória. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>Membros

<dl> <dt>

**lpMemory**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para um bloco de memória a ser carregado.

</dd> <dt>

**dSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho do bloco de memória a ser carregado, em bytes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura identifica um recurso a ser carregado quando um aplicativo usa o método [**Createenumobject**](idirectxfile--createenumobject.md) e especifica DXFILELOAD \_ FROMMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[X estruturas de arquivo](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**Createenumobject**](idirectxfile--createenumobject.md)
</dt> <dt>

[Constantes DXFILE](dxfile.md)
</dt> </dl>

 

 
