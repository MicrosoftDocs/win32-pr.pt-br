---
description: A \_ estrutura de \_ Caps config do fluxo de áudio TAPI \_ \_ está contida na \_ estrutura Caps de configuração do fluxo TAPI \_ \_ quando o membro capstype é definido como o membro AudioCap da União StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: Estrutura de TAPI_AUDIO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780588"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>\_Estrutura de \_ Caps de configuração de fluxo de áudio TAPI \_ \_

\[ Essa estrutura não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A estrutura de **\_ \_ \_ \_ Caps config do fluxo de áudio TAPI** está contida na estrutura [**\_ \_ \_ Caps de configuração do fluxo TAPI**](tapi-stream-config-caps.md) quando o membro **capstype** é definido como o membro **AudioCap** da União [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Sintaxe


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Descrição**
</dt> <dd>

Uma descrição amigável do tipo de configuração de fluxo de áudio para exibição para usuários do aplicativo.

</dd> <dt>

**MinimumChannels**
</dt> <dd>

O número mínimo de canais associados ao fluxo.

</dd> <dt>

**MaximumChannels**
</dt> <dd>

O número máximo de canais associados ao fluxo.

</dd> <dt>

**ChannelsGranularity**
</dt> <dd>

A granularidade da contagem de canais.

</dd> <dt>

**MinimumBitsPerSample**
</dt> <dd>

O número mínimo de bits por amostra.

</dd> <dt>

**MaximumBitsPerSample**
</dt> <dd>

O número máximo de bits por amostra.

</dd> <dt>

**BitsPerSampleGranularity**
</dt> <dd>

A granularidade dos bits por valores de exemplo.

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

A frequência de amostragem mínima.

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

A frequência de amostragem máxima.

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

A granularidade dos valores de frequência de amostragem.

</dd> <dt>

**MinimumAvgBytesPerSec**
</dt> <dd>

A média mínima de bytes por segundo.

</dd> <dt>

**MaximumAvgBytesPerSec**
</dt> <dd>

A média máxima de bytes por segundo.

</dd> <dt>

**AvgBytesPerSecGranularity**
</dt> <dd>

A granularidade dos valores de bytes por segundo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                       |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_limites de \_ configuração de fluxo TAPI \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




