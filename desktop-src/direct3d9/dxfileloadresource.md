---
description: Identifica os dados do recurso. Preterido.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Estrutura DXFILELOADRESOURCE (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 54d0072d7c87f6d26483faf8c591ea7651eff29b411643eb9848de11ff50d899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803033"
---
# <a name="dxfileloadresource-structure"></a>Estrutura DXFILELOADRESOURCE

Identifica os dados do recurso. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a>Membros

<dl> <dt>

**hModule**
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador do módulo que contém o recurso a ser carregado. Se esse membro for **nulo**, o recurso deverá ser anexado ao arquivo executável que o usará.

</dd> <dt>

**lpName**
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para uma cadeia de caracteres especificando o nome do recurso a ser carregado. Por exemplo, se o recurso for uma malha, esse membro deverá especificar o nome do arquivo de malha.

</dd> <dt>

**lpType**
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para uma cadeia de caracteres que especifica o tipo definido pelo usuário que identifica o recurso.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura identifica um recurso a ser carregado quando um aplicativo usa o método [**Createenumobject**](idirectxfile--createenumobject.md) e especifica DXFILELOAD \_ FROMRESOURCE.

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

 

 
