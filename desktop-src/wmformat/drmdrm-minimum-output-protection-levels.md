---
title: Estrutura de DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: A \_ estrutura de níveis de proteção de saída mínima de DRM \_ \_ \_ contém os níveis mínimos de proteção de saída (OPLs) para reprodução de vários tipos de conteúdo. Um dispositivo deve dar suporte ao mínimo de OPL para um tipo de dados para receber esse tipo de dados do leitor.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Formato de mídia do Windows de estrutura de DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786131"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>\_Estrutura de \_ \_ níveis de proteção de saída mínima do DRM \_

A estrutura de **\_ níveis de \_ \_ proteção \_ de saída mínima de DRM** contém os níveis mínimos de proteção de saída (OPLs) para reprodução de vários tipos de conteúdo. Um dispositivo deve dar suporte ao mínimo de OPL para um tipo de dados para receber esse tipo de dados do leitor.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

OPL mínimo necessário para receber vídeo digital compactado.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

OPL mínimo necessário para receber vídeo digital não compactado.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

OPL mínimo necessário para receber vídeo analógico.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

OPL mínimo necessário para receber áudio digital compactado.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

OPL mínimo necessário para receber áudio digital descompactado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada como um membro da estrutura [**\_ \_ OPL de reprodução DRM**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





