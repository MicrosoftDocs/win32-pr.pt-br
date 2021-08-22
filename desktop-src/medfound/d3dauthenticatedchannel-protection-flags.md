---
description: Especifica o nível de proteção para conteúdo de vídeo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1d1b76a6fea0dd6b966bd72001efb187a7a3a14e75b4d41d631e5a1ea163fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974705"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>Estrutura DE SINALIZADORES DE PROTEÇÃO D3DAUTHENTICATEDCHANNEL \_ \_

Especifica o nível de proteção para conteúdo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a>Membros

<dl> <dt>

**ProtectionEnabled**
</dt> <dd>

Se 1, a proteção de conteúdo de vídeo será habilitada.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Se 1, o aplicativo exigirá que o vídeo seja exibido usando uma sobreposição de hardware ou um modo exclusivo de tela inteira.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado. De definir todos os bits como zero.

</dd> <dt>

**Valor**
</dt> <dd>

Use esse membro para acessar todos os bits na união.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




