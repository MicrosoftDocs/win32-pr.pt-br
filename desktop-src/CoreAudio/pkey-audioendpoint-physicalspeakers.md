---
description: 'Saiba mais sobre: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501057"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

A propriedade **PKEY \_ AudioEndpoint \_ PhysicalSpeakers** especifica a máscara de configuração de canal para o dispositivo de ponto de extremidade de áudio. A máscara indica a configuração física de um conjunto de alto-falantes e especifica a atribuição de canais aos alto-falantes. Para obter mais informações sobre máscaras de configuração de canal, consulte o seguinte:

1.  A descrição da propriedade de \_ configuração do canal de áudio KSPROPERTY \_ \_ na documentação do Windows DDK.
2.  A white paper intitulada "suporte de driver de áudio para configurações de alto-falante de Home Theater" no site de [tecnologias de dispositivo de áudio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ UI4.

O membro **uintVal** da estrutura **PROPVARIANT** contém uma máscara de configuração de canal que é convertida para o tipo **uint**.

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
</dt> </dl>

 

 




