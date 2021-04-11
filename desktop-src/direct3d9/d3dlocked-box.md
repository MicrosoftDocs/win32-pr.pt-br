---
description: Descreve uma caixa bloqueada (volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Estrutura de D3DLOCKED_BOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173056"
---
# <a name="d3dlocked_box-structure"></a>Estrutura da caixa de D3DLOCKED \_

Descreve uma caixa bloqueada (volume).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a>Membros

<dl> <dt>

**De semidensidade**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento de byte da borda esquerda de uma linha para a borda esquerda da próxima linha.

</dd> <dt>

**SlicePitch**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento de byte do canto superior esquerdo de uma fatia para a parte superior esquerda da próxima fatia mais profunda.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **void \***

</dd> <dd>

Ponteiro para o início da caixa volume. Se um [**D3DBOX**](d3dbox.md) foi fornecido para a chamada de Lockbox, o pBits será adequadamente deslocado do início do volume.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os volumes podem ser visualizados como organizados em fatias de largura x altura 2D superfícies empilhadas para fazer um volume de profundidade x altura x de largura. Para obter mais informações, consulte [recursos de textura de volume (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9:: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9:: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
