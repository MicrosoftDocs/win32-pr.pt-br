---
description: Especifica como combinar os dados de glifo das superfícies de origem e destino em uma chamada para ComposeRects.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Enumeração D3DCOMPOSERECTSOP (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8d968770eb58d9d3dd59f178b05e8e6536079e8de601ddef602a41da4b52ee51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911164"
---
# <a name="d3dcomposerectsop-enumeration"></a>Enumeração D3DCOMPOSERECTSOP

Especifica como combinar os dados de glifo das superfícies de origem e destino em uma chamada para [**ComposeRects.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects)

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**CÓPIA DE D3DCOMPOSERECTS \_**
</dt> <dd>

Copie a origem para o destino.

</dd> <dt>

<span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ OU**
</dt> <dd>

OU bit a bit, a origem e o destino.

</dd> <dt>

<span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ E**
</dt> <dd>

AND bit a bit, a origem e o destino.

</dd> <dt>

<span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ NEG**
</dt> <dd>

Copie a origem negada para o destino (Dst & ~Src).

</dd> <dt>

<span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ FORCE \_ DWORD**
</dt> <dd>

Reservado. Usado para forçar a enumeração a 32 bits de tamanho.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




