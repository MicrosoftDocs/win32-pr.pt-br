---
description: Descreve uma região retangular bloqueada.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT (D3D9Types.h)
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
ms.openlocfilehash: b419483329e5461de5bc98b3a37b556e37138a055932b1d6c80d3a19b13ae516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988896"
---
# <a name="d3dlocked_rect-structure"></a>Estrutura D3DLOCKED \_ RECT

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

**Densidade**
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes em uma linha da superfície.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **\* void**

</dd> <dd>

Ponteiro para os bits bloqueados. Se um [**RECT**](/previous-versions//dd162897(v=vs.85)) tiver sido fornecido para a [**chamada LockRect,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) pBits será devidamente deslocada do início da superfície.

</dd> </dl>

## <a name="remarks"></a>Comentários

O tom para formatos DXTn é diferente do que foi retornado no DirectX 7. Agora, ele se refere ao número de bytes em uma linha de blocos. Por exemplo, se você tiver uma largura de 16, terá um tom de 4 blocos (4 8 para \* DXT1, 4 \* 16 para DXT2-5.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
