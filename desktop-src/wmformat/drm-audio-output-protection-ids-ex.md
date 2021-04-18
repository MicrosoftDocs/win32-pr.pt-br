---
title: Estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: A \_ \_ estrutura ex de proteção de saída de áudio DRM \_ \_ \_ contém uma lista de identificadores de proteção de saída de áudio. Essa estrutura estende as \_ \_ \_ IDs de proteção de saída de áudio DRM \_ adicionando um número de versão.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- Formato de mídia do Windows de estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793954"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a>\_ \_ \_ \_ Estrutura ex de proteção de saída de áudio DRM \_

A **estrutura \_ \_ \_ \_ \_ ex de proteção de saída de áudio DRM** contém uma lista de identificadores de proteção de saída de áudio. Essa estrutura estende **as \_ \_ IDs de \_ proteção \_ de saída de áudio DRM** adicionando um número de versão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

Número da versão.

</dd> <dt>

**cEntries**
</dt> <dd>

Número de entradas na matriz **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Matriz de **estruturas \_ \_ ex de \_ proteção \_ de saída de áudio DRM** . **DRM \_ Proteção de saída de áudio \_ \_ \_ ex** é um tipo definido como [**proteção de \_ saída DRM \_ \_ ex**](drm-output-protection-ex.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

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

 

 





