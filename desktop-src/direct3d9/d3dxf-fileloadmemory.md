---
description: Identifica dados de memória.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: D3DXF_FILELOADMEMORY (D3dx9xof.h)
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
ms.openlocfilehash: b3709e6eeb99026b76d066edfccbae578b5c851d6e73936ffe06d10fbf69dcb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045054"
---
# <a name="d3dxf_fileloadmemory-structure"></a>Estrutura FILELOADMEMORY D3DXF \_

Identifica dados de memória.

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

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho do bloco de memória a ser carregado, em bytes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura identifica os dados a serem carregados da memória quando um aplicativo usa o método [**CreateEnumObject**](id3dxfile--createenumobject.md) e especifica o sinalizador D3DXF \_ FILELOAD \_ FROMMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
