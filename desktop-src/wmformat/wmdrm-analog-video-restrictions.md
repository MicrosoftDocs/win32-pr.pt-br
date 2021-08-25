---
title: Estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS (wmdrmsdk. h)
description: A \_ estrutura de restrições de vídeo analógica do WMDRM \_ \_ contém informações sobre uma restrição para reproduzir conteúdo como vídeo analógico.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8221fe325983387107f4e0c03f5672a6762502d8865e1d5895a9e48e96b99d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928806"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>\_Estrutura de \_ restrições de vídeo analógico WMDRM \_

A estrutura de **\_ \_ \_ restrições de vídeo analógica do WMDRM** contém informações sobre uma restrição para reproduzir conteúdo como vídeo analógico.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**guidRestrictionID**
</dt> <dd>

Identificador de restrição.

</dd> <dt>

**dwRestrictionData**
</dt> <dd>

Dados de restrição.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é recebida quando você chama [**IWMDRMLicense:: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> <dt>

[**\_restrições de \_ vídeo analógico WMDRM \_ \_ ex**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





