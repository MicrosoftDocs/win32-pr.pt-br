---
description: Descreve uma região retangular bloqueada.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Estrutura de D3DLOCKED_RECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506495"
---
# <a name="d3dlocked_rect-structure"></a>\_Estrutura D3DLOCKED Rect

Descreve uma região retangular bloqueada.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Zumbi**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes em uma linha da superfície.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **void \***

</dd> <dd>

Ponteiro para os bits bloqueados. Se um [**Rect**](/previous-versions//dd162897(v=vs.85)) foi fornecido para a chamada [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits será adequadamente deslocado do início da superfície.

</dd> </dl>

## <a name="remarks"></a>Comentários

O Tom dos formatos DXTn é diferente do que foi retornado no DirectX 7. Agora, ele se refere ao número de bytes em uma linha de blocos. Por exemplo, se você tiver uma largura de 16, terá um timbre de 4 blocos (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
