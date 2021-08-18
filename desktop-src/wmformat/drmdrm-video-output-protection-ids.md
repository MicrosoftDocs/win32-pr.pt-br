---
title: Estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: A \_ \_ estrutura de IDs da proteção de saída de vídeo DRM \_ \_ contém uma matriz de \_ estruturas de proteção de saída de vídeo DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Formato de mídia do Windows de estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9439328ed817da40630c3a600cf7e6db553738a12799babbe9e71c48f28923b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119085868"
---
# <a name="drm_video_output_protection_ids-structure"></a>\_Estrutura de \_ IDs de proteção de saída de vídeo DRM \_ \_

A estrutura de **IDs da proteção de \_ saída de vídeo \_ \_ \_ DRM** contém uma matriz de estruturas de **proteção de \_ \_ saída \_ de vídeo DRM** .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**cEntries**
</dt> <dd>

Número de elementos na matriz referenciados por **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Endereço de uma matriz de estruturas de **\_ proteção de \_ saída \_ de vídeo DRM** . **DRM \_ A \_ \_ proteção de saída de vídeo** é um tipo definido como [**\_ \_ proteção de saída DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada como um membro da estrutura [**\_ \_ OPL de reprodução DRM**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IDs de \_ proteção de saída de áudio DRM \_ \_**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**\_IDs de proteção de saída de vídeo DRM \_ \_ \_ \_ ex**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





