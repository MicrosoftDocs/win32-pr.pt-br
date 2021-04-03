---
description: Descreve o modo de exibição.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: Estrutura D3DDISPLAYMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091951"
---
# <a name="d3ddisplaymode-structure"></a>Estrutura D3DDISPLAYMODE

Descreve o modo de exibição.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura da tela, em pixels.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura da tela, em pixels.

</dd> <dt>

**Taxa_de_atualização**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Taxa de atualização. O valor 0 indica um padrão de adaptador.

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície do modo de exibição.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[**GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
