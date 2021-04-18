---
title: Estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: A \_ \_ estrutura de IDs da proteção de saída de áudio DRM \_ \_ contém uma lista de identificadores de proteção de saída de áudio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Formato de mídia do Windows de estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766515"
---
# <a name="drm_audio_output_protection_ids-structure"></a>\_Estrutura de \_ IDs de proteção de saída de áudio DRM \_ \_

A estrutura de **IDs da proteção de \_ saída de áudio \_ \_ \_ DRM** contém uma lista de identificadores de proteção de saída de áudio.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**cEntries**
</dt> <dd>

Número de entradas na matriz **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Matriz de estruturas de **\_ proteção de \_ saída \_ de áudio DRM** . **DRM \_ A \_ \_ proteção de saída de áudio** é um tipo definido como [**\_ \_ proteção de saída DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IDs de proteção de saída de áudio DRM \_ \_ \_ \_ ex**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_IDs de \_ proteção de saída de vídeo DRM \_ \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





