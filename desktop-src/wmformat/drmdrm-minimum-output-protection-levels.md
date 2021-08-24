---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS estrutura (Wmdrmsdk.h)
description: A estrutura NÍVEIS MÍNIMOS DE PROTEÇÃO DE SAÍDA DRM contém os níveis mínimos de proteção de saída \_ \_ \_ \_ (OPLs) para reprodução de vários tipos de conteúdo. Um dispositivo deve dar suporte ao OPL mínimo para um tipo de dados receber esse tipo de dados do leitor.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS formato de mídia windows da estrutura
- formato de mídia de janelas de estrutura
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
ms.openlocfilehash: d5559527507f0399a09661dfe380f51d11e10750eddf7d996b38d110e4f38e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708916"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>Estrutura DE \_ NÍVEIS \_ MÍNIMOS DE \_ PROTEÇÃO DE \_ SAÍDA DRM

A **estrutura NÍVEIS \_ MÍNIMOS DE PROTEÇÃO DE SAÍDA \_ \_ \_ DRM** contém os níveis mínimos de proteção de saída (OPLs) para reprodução de vários tipos de conteúdo. Um dispositivo deve dar suporte ao OPL mínimo para um tipo de dados receber esse tipo de dados do leitor.

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

O OPL mínimo necessário para receber vídeo digital compactado.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

O OPL mínimo necessário para receber vídeo digital descompactado.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

O OPL mínimo necessário para receber vídeo análogo.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

O OPL mínimo necessário para receber áudio digital compactado.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

O OPL mínimo necessário para receber áudio digital descompactado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada como membro da estrutura [**\_ \_ OPL DO DRM PLAY.**](drmdrm-play-opl.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





