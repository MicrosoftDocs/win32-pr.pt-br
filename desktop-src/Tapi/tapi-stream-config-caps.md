---
description: A estrutura TAPI \_ STREAM \_ CONFIG \_ CAPS contém informações de configuração de fluxo de áudio ou vídeo.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbbb3b3ec72cc99810311cc510e36c2adc8242e2b3d98b321fd8bc8c6a9ab4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002644"
---
# <a name="tapi_stream_config_caps-structure"></a>Estrutura CAPS DE \_ \_ CONFIGURAÇÃO DO \_ FLUXO DE TAPI

\[Essa estrutura não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A **estrutura TAPI \_ STREAM \_ CONFIG \_ CAPS** contém informações de configuração de fluxo de áudio ou vídeo.

## <a name="syntax"></a>Sintaxe


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Membros

<dl> <dt>

**CapsType**
</dt> <dd>

Define se o membro da união contém informações de áudio ou vídeo.

</dd> <dt>

**VideoCap**
</dt> <dd>

Uma [**estrutura CAPS DE \_ \_ \_ CONFIGURAÇÃO DE FLUXO DE VÍDEO \_ DA TAPI**](tapi-video-stream-config-caps.md) que contém os recursos de fluxo de vídeo.

</dd> <dt>

**AudioCap**
</dt> <dd>

Uma [**estrutura CAPS DE \_ \_ \_ CONFIGURAÇÃO DE FLUXO DE ÁUDIO \_ TAPI**](tapi-audio-stream-config-caps.md) que contém os recursos de fluxo de áudio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                       |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**TAPI \_ VIDEO \_ STREAM \_ CONFIG \_ CAPS**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**TAPI \_ AUDIO \_ STREAM \_ CONFIG \_ CAPS**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




