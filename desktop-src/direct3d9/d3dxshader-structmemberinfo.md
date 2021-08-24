---
description: Uma estrutura auxiliar que contém informações de estrutura de membro.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f41c3d1911a046165d929bee50ef4e0b5691cebee9d90007bc367636e343731
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524209"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>Estrutura D3DXSHADER \_ STRUCTMEMBERINFO

Uma estrutura auxiliar que contém informações de estrutura de membro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início dessa estrutura, em bytes, para a cadeia de caracteres que contém o nome do membro da estrutura.

</dd> <dt>

**Typeinfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início dessa estrutura, em bytes, para a cadeia de caracteres que contém as informações de tipo. Consulte [**\_ TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
