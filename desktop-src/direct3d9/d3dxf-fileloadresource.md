---
description: Identifica os dados do recurso.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: D3DXF_FILELOADRESOURCE (D3dx9xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ddc105d3df7732e1572e41c3d9cb47a285caf69cba0a24f6ea65090706394592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564926"
---
# <a name="d3dxf_fileloadresource-structure"></a>Estrutura FILELOADRESOURCE D3DXF \_

Identifica os dados do recurso.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Hmodule**
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Lidar com o módulo que contém o recurso a ser carregado. Se esse membro for **NULL,** o recurso deverá ser anexado ao arquivo executável que o usará.

</dd> <dt>

**Lpname**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para uma cadeia de caracteres que especifica o nome do recurso a ser carregado. Por exemplo, se o recurso for uma malha, esse membro deverá especificar o nome do arquivo de malha.

</dd> <dt>

**lpType**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para uma cadeia de caracteres que especifica o tipo definido pelo usuário que identifica o recurso.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura identifica um recurso a ser carregado quando um aplicativo usa o método [**CreateEnumObject**](id3dxfile--createenumobject.md) e especifica o sinalizador [D3DXF \_ FILELOAD \_ FROMRESOURCE.](d3dxf.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
