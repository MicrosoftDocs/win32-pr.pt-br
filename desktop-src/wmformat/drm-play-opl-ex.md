---
title: DRM_PLAY_OPL_EX estrutura (Wmdrmsdk.h)
description: A estrutura DRM PLAY OPL EX contém informações sobre os níveis de proteção de saída \_ \_ \_ (OPLs) especificados em uma licença para ações de reprodução.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX formato de mídia do Windows
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89ca0c6b1cf33a422265fb177e1b1432a52fbd12b3f9fda658125682f3888ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848435"
---
# <a name="drm_play_opl_ex-structure"></a>Estrutura \_ \_ OPL EX DO DRM PLAY \_

A **estrutura DRM \_ PLAY \_ OPL \_ EX** contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwversion**
</dt> <dd>

Número da versão.

</dd> <dt>

**minOPL**
</dt> <dd>

[**DRM \_ Estrutura MINIMUM \_ OUTPUT \_ PROTECTION \_ LEVELS**](drmdrm-minimum-output-protection-levels.md) contendo o OPL mínimo necessário para reproduzir conteúdo em formatos diferentes.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ Estrutura \_ de \_ \_ IDS de PROTEÇÃO DE SAÍDA DE**](drmdrm-video-output-protection-ids.md) VÍDEO que contém os identificadores de proteção de saída de vídeo que se aplicam à reprodução do conteúdo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é idêntica à estrutura **\_ \_ OPL DO DRM PLAY,** exceto que ela inclui um número de versão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





