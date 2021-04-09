---
description: A \_ Propriedade PKEY AudioEndpoint \_ FullRangeSpeakers especifica a máscara de configuração de canal para os alto-falantes de intervalo completo que estão conectados ao dispositivo de ponto de extremidade de áudio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089517"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

A propriedade **PKEY \_ AudioEndpoint \_ FullRangeSpeakers** especifica a máscara de configuração de canal para os alto-falantes de intervalo completo que estão conectados ao dispositivo de ponto de extremidade de áudio. A máscara indica a configuração física dos alto-falantes do intervalo completo e especifica a atribuição de canais a esses alto-falantes.

O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ UI4.

O membro **uintVal** da estrutura **PROPVARIANT** contém uma máscara de configuração de canal que é convertida para o tipo **uint**.

Um palestrante de intervalo completo é capaz de reproduzir sons em todo o intervalo de baixo a agudos. Normalmente, os alto-falantes maiores são um intervalo completo, mas os altifalantes menores são significativamente menos capazes de reproduzir sons graves. No Windows Vista, o mecanismo de áudio usa essa propriedade para gerenciar os níveis de baixo desempenho no fluxo de saída de áudio que é reproduzido pelo dispositivo de ponto de extremidade de áudio.

A máscara de configuração de canal para essa propriedade está no mesmo formato que a máscara de configuração de canal para a propriedade [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) . Para obter mais informações sobre máscaras de configuração de canal, consulte o seguinte:

-   A descrição da propriedade de \_ configuração do canal de áudio KSPROPERTY \_ \_ na documentação do Windows DDK.
-   A white paper intitulada "suporte de driver de áudio para configurações de alto-falante de Home Theater" no site de [tecnologias de dispositivo de áudio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

O sistema Obtém a máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ FullRangeSpeakers do usuário. O usuário insere essas informações por meio do painel de controle multimídia do Windows Mmsys.cpl. Para obter mais informações sobre Mmsys.cpl, consulte a documentação do Windows DDK.

A máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ FullRangeSpeakers de um dispositivo de ponto de extremidade de áudio é um subconjunto da máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ PhysicalSpeakers do mesmo dispositivo.

Por exemplo, se um dispositivo de ponto de extremidade de áudio direcionar um conjunto de alto-falantes de 5,1 surround, a máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ PHYSICALSPEAKERS será KSAUDIO de \_ alto-falante \_ 5POINT1. Essa máscara indica a presença de alto-falantes da esquerda, frontal direita, Front-Center, lateral esquerda e lateral direita — além de um subwoofer. Se os alto-falantes front-Left e front-Right forem grandes o suficiente para produzir sons graves, mas o front-Center e os alto-falantes laterais menores não forem, a máscara de configuração de canal para a \_ Propriedade PKEY AudioEndpoint \_ FULLRANGESPEAKERS será KSAUDIO \_ \_ , que indica apenas os alto-falantes front-Left e front-Right. As máscaras de configuração de canal KSAUDIO \_ \_ 5POINT1 de orador e KSAUDIO \_ \_ estéreo são definidas no arquivo de cabeçalho Ksmedia. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> <dt>

[**\_Propriedade PKEY AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




