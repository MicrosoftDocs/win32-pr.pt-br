---
title: Estrutura de DRM_PLAY_OPL (wmdrmsdk. h)
description: A \_ estrutura OPL de reprodução do DRM \_ contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Formato de mídia do Windows de estrutura de DRM_PLAY_OPL
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f649263db5435310d076386c49b2e77960552646e7ea2325190c3f0b94f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708306"
---
# <a name="drm_play_opl-structure"></a>\_Estrutura OPL de reprodução DRM \_

A **estrutura \_ \_ OPL de reprodução do DRM** contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**minOPL**
</dt> <dd>

[**DRM \_ A estrutura de \_ \_ \_ níveis de proteção de saída mínima**](drmdrm-minimum-output-protection-levels.md) que contém o OPL mínimo necessário para reproduzir o conteúdo em formatos diferentes.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ A \_ proteção de saída de vídeo \_ \_ identifica**](drmdrm-video-output-protection-ids.md) a estrutura que contém os identificadores de proteção de saída de vídeo que se aplicam à reprodução do conteúdo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_OPL de cópia DRM \_**](drmdrm-copy-opl.md)
</dt> <dt>

[**execução do DRM \_ \_ OPL \_ ex**](drm-play-opl-ex.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





