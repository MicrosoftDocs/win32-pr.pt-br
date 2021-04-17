---
description: Especifica o nível de proteção para conteúdo de vídeo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Estrutura de D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
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
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783707"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>Estrutura de sinalizadores de \_ proteção do D3DAUTHENTICATEDCHANNEL \_

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

Se 1, a proteção de conteúdo de vídeo está habilitada.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Se for 1, o aplicativo exigirá que o vídeo seja exibido usando uma sobreposição de hardware ou o modo exclusivo de tela inteira.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado. Definir todos os bits como zero.

</dd> <dt>

**Valor**
</dt> <dd>

Use esse membro para acessar todos os bits na União.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




