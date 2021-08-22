---
title: Estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: A \_ estrutura ex de proteção de saída de vídeo DRM \_ \_ \_ \_ contém uma matriz de \_ estruturas de proteção de saída de vídeo DRM \_ \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Formato de mídia do Windows de estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5482734c2ded470b4e3dc885e32505c556b3106a12518969622f8007cf6e4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704083"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>\_ \_ \_ \_ Estrutura ex de proteção de saída de vídeo DRM \_

A **estrutura \_ \_ \_ \_ \_ ex de proteção de saída de vídeo DRM** contém uma matriz de estruturas de **\_ \_ \_ proteção de saída de vídeo DRM** .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
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

Número de elementos na matriz referenciados por **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Endereço de uma matriz de **estruturas \_ \_ ex de \_ proteção \_ de saída de vídeo DRM** . **DRM \_ Proteção de saída de vídeo \_ \_ \_ ex** é um tipo definido como [**proteção de \_ saída DRM \_ \_ ex**](drm-output-protection-ex.md).

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

 

 





