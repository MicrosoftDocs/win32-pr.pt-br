---
description: A estrutura de Caps de configuração de \_ fluxo TAPI \_ \_ contém informações de configuração de fluxo de áudio ou vídeo.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Estrutura de TAPI_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789843"
---
# <a name="tapi_stream_config_caps-structure"></a>\_Estrutura de \_ Caps de configuração de fluxo TAPI \_

\[ Essa estrutura não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A estrutura de **\_ \_ \_ Caps** de configuração de fluxo TAPI contém informações de configuração de fluxo de áudio ou vídeo.

## <a name="syntax"></a>Sintaxe


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Capstype**
</dt> <dd>

Define se o membro de União contém informações de vídeo ou áudio.

</dd> <dt>

**VideoCap**
</dt> <dd>

Uma [**estrutura \_ \_ Caps de \_ configuração \_ de fluxo de vídeo TAPI**](tapi-video-stream-config-caps.md) que contém os recursos de fluxo de vídeo.

</dd> <dt>

**AudioCap**
</dt> <dd>

Uma estrutura de [**limites de configuração de \_ fluxo de áudio \_ \_ \_ TAPI**](tapi-audio-stream-config-caps.md) que contém os recursos de fluxo de áudio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                       |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**\_limites de \_ configuração de fluxo de vídeo TAPI \_ \_**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**\_limites de \_ configuração do fluxo de áudio TAPI \_ \_**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




