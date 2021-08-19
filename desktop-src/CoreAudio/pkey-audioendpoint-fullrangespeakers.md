---
description: A propriedade \_ PKEY AudioEndpoint FullRangeSpeakers especifica a máscara de configuração de canal para os alto-falantes de intervalo completo conectados ao dispositivo de ponto de \_ extremidade de áudio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad27e5623189ce3ba78707377837493c1ea8dccb248d02ddd3d8e2c64570bed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406442"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

A **propriedade \_ PKEY AudioEndpoint \_ FullRangeSpeakers** especifica a máscara de configuração de canal para os alto-falantes de intervalo completo conectados ao dispositivo de ponto de extremidade de áudio. A máscara indica a configuração física dos alto-falantes de intervalo completo e especifica a atribuição de canais a esses alto-falantes.

O **membro vt** da estrutura **PROPVARIANT** é definido como VT \_ UI4.

O **membro uintVal** da estrutura **PROPVARIANT** contém uma máscara de configuração de canal que é lançada para o **tipo UINT.**

Um locutor de intervalo completo é capaz de tocar sons em todo o intervalo, desde o sol até o treble. Normalmente, os alto-falantes maiores têm uma gama completa, mas os alto-falantes menores são significativamente menos capazes de tocar sons de ruídos. No Windows Vista, o mecanismo de áudio usa essa propriedade para gerenciar níveis de baixo no fluxo de saída de áudio que é tocada pelo dispositivo de ponto de extremidade de áudio.

A máscara de configuração de canal para essa propriedade está no mesmo formato que a máscara de configuração de canal para a [**propriedade PKEY \_ AudioEndpoint \_ PhysicalSpeakers.**](pkey-audioendpoint-physicalspeakers.md) Para obter mais informações sobre máscaras de configuração de canal, consulte o seguinte:

-   A descrição da propriedade KSPROPERTY AUDIO CHANNEL CONFIG na \_ \_ \_ documentação Windows DDK.
-   O white paper intitulado "Suporte do driver de áudio para configurações do locutor do Home Speaker" no site tecnologias de dispositivo de áudio [para Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

O sistema obtém a máscara de configuração de canal para a propriedade \_ PKEY AudioEndpoint \_ FullRangeSpeakers do usuário. O usuário ins insira essas informações por meio do painel de controle Windows multimídia, Mmsys.cpl. Para obter mais informações sobre Mmsys.cpl, consulte a documentação Windows DDK.

A máscara de configuração de canal para a propriedade PKEY AudioEndpoint FullRangeSpeakers de um dispositivo de ponto de extremidade de áudio é um subconjunto da máscara de configuração de canal para a propriedade \_ \_ PKEY \_ AudioEndpoint \_ PhysicalSpeakers do mesmo dispositivo.

Por exemplo, se um dispositivo de ponto de extremidade de áudio conduz um conjunto de alto-falantes de som surround 5.1, a máscara de configuração de canal para a propriedade PKEY \_ AudioEndpoint \_ PhysicalSpeakers é KSAUDIO \_ SPEAKER \_ 5POINT1. Essa máscara indica a presença de alto-falantes à esquerda, à direita, à direita, à frente, à esquerda e à direita, além de um subwoofer. Se os alto-falantes front-left e front-right são grandes o suficiente para produzir sons de bateria, mas os alto-falantes laterais e front-center menores não são, então a máscara de configuração de canal para a propriedade \_ \_ FullRangeSpeakers de AudioEndpoint PKEY é KSAUDIO SPEAKER STEREO, que indica apenas os \_ \_ alto-falantes front-left e front-right. As máscaras de configuração de canal KSAUDIO SPEAKER 5POINT1 e KSAUDIO SPEAKER ESTÉREO são definidas no arquivo de \_ \_ \_ \_ header Ksmedia.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio principais](core-audio-properties.md)
</dt> <dt>

[**Propriedade PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




