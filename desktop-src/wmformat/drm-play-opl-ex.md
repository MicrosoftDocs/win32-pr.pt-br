---
title: Estrutura de DRM_PLAY_OPL_EX (wmdrmsdk. h)
description: A \_ estrutura DRM Play \_ OPL \_ ex contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Formato de mídia do Windows de estrutura de DRM_PLAY_OPL_EX
- estruturar formato de mídia do Windows
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
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788998"
---
# <a name="drm_play_opl_ex-structure"></a>Estrutura de exemplo do DRM \_ Play \_ OPL \_

A estrutura **DRM \_ Play \_ OPL \_ ex** contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.

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

**DW**
</dt> <dd>

Número da versão.

</dd> <dt>

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

## <a name="remarks"></a>Comentários

Essa estrutura é idêntica à estrutura **\_ \_ OPL de reprodução DRM** , exceto pelo fato de que ela inclui um número de versão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_OPL de reprodução DRM \_**](drmdrm-play-opl.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





