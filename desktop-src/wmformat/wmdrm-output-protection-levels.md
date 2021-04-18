---
title: Estrutura de WMDRM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: A estrutura de níveis de proteção de saída do WMDRM \_ \_ \_ contém os OPLs (níveis de proteções de saída) exigidos por uma licença para executar várias ações.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_OUTPUT_PROTECTION_LEVELS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815428"
---
# <a name="wmdrm_output_protection_levels-structure"></a>\_Estrutura de \_ níveis de proteção de saída WMDRM \_

A estrutura de níveis de proteção de saída do WMDRM contém os OPLs (níveis de proteções de saída) exigidos por uma licença para executar várias ações. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
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

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

OPL mínimo necessário para copiar o conteúdo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada pelo método [**IWMDRMLicense:: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





