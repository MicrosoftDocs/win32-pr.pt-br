---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS estrutura (Wmdrmsdk.h)
description: A estrutura IDS de PROTEÇÃO DE SAÍDA DE ÁUDIO \_ \_ \_ \_ DRM contém uma lista de identificadores de proteção de saída de áudio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS formato de mídia do Windows
- formato de mídia de janelas de estrutura
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
ms.openlocfilehash: 7e31589a229dcd5e32a0198cf7f3679846574bdb605e25a8df272b1793704b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659006"
---
# <a name="drm_audio_output_protection_ids-structure"></a>Estrutura de \_ \_ \_ \_ IDS DE PROTEÇÃO DE SAÍDA DE ÁUDIO DRM

A **estrutura \_ \_ \_ \_ IDS** de PROTEÇÃO DE SAÍDA DE ÁUDIO DRM contém uma lista de identificadores de proteção de saída de áudio.

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

Número de entradas na matriz **rgAop.**

</dd> <dt>

**rgAop**
</dt> <dd>

Matriz de **estruturas DE \_ PROTEÇÃO DE SAÍDA DE ÁUDIO \_ \_ DRM.** **DRM \_ AUDIO \_ OUTPUT \_ PROTECTION é** um tipo definido como PROTEÇÃO DE SAÍDA [**\_ \_ DRM.**](drm-output-protection.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ \_ IDS DE PROTEÇÃO DE SAÍDA DE ÁUDIO \_ \_ DRM \_ EX**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_ \_ IDS DE PROTEÇÃO DE SAÍDA DE VÍDEO \_ \_ DRM**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





