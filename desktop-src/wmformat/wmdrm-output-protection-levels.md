---
title: WMDRM_OUTPUT_PROTECTION_LEVELS estrutura (Wmdrmsdk.h)
description: A estrutura NÍVEIS DE PROTEÇÃO DE SAÍDA WMDRM contém os níveis de proteções de saída \_ \_ \_ (OPLs) exigidos por uma licença para executar várias ações.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS formato de mídia windows da estrutura
- formato de mídia de janelas de estrutura
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
ms.openlocfilehash: 4a19d7098266857f8a17e395ad749b216e45ce101278812f67c032943933955a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843957"
---
# <a name="wmdrm_output_protection_levels-structure"></a>Estrutura DE NÍVEIS DE \_ PROTEÇÃO \_ DE SAÍDA \_ WMDRM

A **estrutura NÍVEIS DE PROTEÇÃO DE SAÍDA \_ \_ \_ WMDRM** contém os níveis de proteções de saída (OPLs) exigidos por uma licença para executar várias ações.

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

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

O OPL mínimo necessário para copiar o conteúdo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada pelo [**método IWMDRMLicense::GetOutputProtectionLevels.**](iwmdrmlicense-getoutputprotectionlevels.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





