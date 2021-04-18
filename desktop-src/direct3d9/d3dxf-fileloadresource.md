---
description: Identifica os dados do recurso.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Estrutura de D3DXF_FILELOADRESOURCE (D3dx9xof. h)
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
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781217"
---
# <a name="d3dxf_fileloadresource-structure"></a>\_Estrutura D3DXF FILELOADRESOURCE

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

**hModule**
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador do módulo que contém o recurso a ser carregado. Se esse membro for **nulo**, o recurso deverá ser anexado ao arquivo executável que o usará.

</dd> <dt>

**lpName**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para uma cadeia de caracteres especificando o nome do recurso a ser carregado. Por exemplo, se o recurso for uma malha, esse membro deverá especificar o nome do arquivo de malha.

</dd> <dt>

**lpType**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para uma cadeia de caracteres que especifica o tipo definido pelo usuário que identifica o recurso.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura identifica um recurso a ser carregado quando um aplicativo usa o método [**Createenumobject**](id3dxfile--createenumobject.md) e especifica o [sinalizador \_ \_ FROMRESOURCE fileload D3DXF](d3dxf.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
