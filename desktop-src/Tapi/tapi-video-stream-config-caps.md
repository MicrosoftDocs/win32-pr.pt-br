---
description: A \_ estrutura Caps de configuração de fluxo de vídeo TAPI \_ \_ \_ está contida \_ na \_ estrutura Caps de configuração de fluxo TAPI \_ quando o membro capstype é definido como o membro VideoCap da União StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: Estrutura de TAPI_VIDEO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768563"
---
# <a name="tapi_video_stream_config_caps-structure"></a>\_Estrutura de \_ Caps de configuração de fluxo de vídeo TAPI \_ \_

\[ Essa estrutura não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A **estrutura \_ \_ Caps de \_ configuração \_ de fluxo de vídeo TAPI** está contida na estrutura [**\_ \_ \_ Caps de configuração de fluxo TAPI**](tapi-stream-config-caps.md) quando o membro **capstype** é definido como o membro **VideoCap** da União [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Sintaxe


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Descrição**
</dt> <dd>

Uma descrição amigável do tipo de configuração de fluxo de áudio para exibição para usuários do aplicativo.

</dd> <dt>

**VideoStandard**
</dt> <dd>

Padrão de vídeo sendo usado.

</dd> <dt>

**Incolocar**
</dt> <dd>

Tamanho de entrada do quadro.

</dd> <dt>

**MinCroppingSize**
</dt> <dd>

Tamanho mínimo de corte.

</dd> <dt>

**MaxCroppingSize**
</dt> <dd>

Tamanho máximo de corte.

</dd> <dt>

**CropGranularityX**
</dt> <dd>

Granularidade do corte permitido ao longo do eixo x.

</dd> <dt>

**CropGranularityY**
</dt> <dd>

Granularidade do corte permitido ao longo do eixo y.

</dd> <dt>

**CropAlignX**
</dt> <dd>

Alinhamento do corte do eixo x.

</dd> <dt>

**CropAlignY**
</dt> <dd>

Alinhamento do corte do eixo y.

</dd> <dt>

**MinOutputSize**
</dt> <dd>

Tamanho mínimo resultante da janela de vídeo.

</dd> <dt>

**MaxOutputSize**
</dt> <dd>

Tamanho máximo resultante da janela de vídeo.

</dd> <dt>

**OutputGranularityX**
</dt> <dd>

Granularidade do tamanho de saída ao longo do eixo x.

</dd> <dt>

**OutputGranularityY**
</dt> <dd>

Granularidade do tamanho de saída ao longo do eixo y.

</dd> <dt>

**StretchTapsX**
</dt> <dd>

Stretch ao longo do eixo x.

</dd> <dt>

**StretchTapsY**
</dt> <dd>

Stretch ao longo do eixo y.

</dd> <dt>

**ShrinkTapsX**
</dt> <dd>

Reduzir ao longo do eixo x.

</dd> <dt>

**ShrinkTapsY**
</dt> <dd>

Reduzir ao longo do eixo y.

</dd> <dt>

**MinFrameInterval**
</dt> <dd>

Intervalo mínimo de quadros de vídeo.

</dd> <dt>

**MaxFrameInterval**
</dt> <dd>

Intervalo máximo de quadros de vídeo.

</dd> <dt>

**MinBitsPerSecond**
</dt> <dd>

Mínimo de bits por segundo.

</dd> <dt>

**MaxBitsPerSecond**
</dt> <dd>

Máximo de bits por segundo.

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

 

 




