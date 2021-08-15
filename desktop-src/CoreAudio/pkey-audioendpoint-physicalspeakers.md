---
description: 'Saiba mais sobre: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358623626274a0ab3a0898e9e912e4f5f990c14d00dd6f6ef57bb4050297403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406412"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

A **propriedade PKEY \_ AudioEndpoint \_ PhysicalSpeakers** especifica a máscara de configuração de canal para o dispositivo de ponto de extremidade de áudio. A máscara indica a configuração física de um conjunto de alto-falantes e especifica a atribuição de canais a alto-falantes. Para obter mais informações sobre máscaras de configuração de canal, consulte o seguinte:

1.  A descrição da propriedade KSPROPERTY AUDIO CHANNEL CONFIG na \_ \_ \_ documentação Windows DDK.
2.  O white paper intitulado "Suporte do driver de áudio para configurações do locutor do Home Speaker" no site Tecnologias de Dispositivo de Áudio [para Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

O **membro vt** da estrutura **PROPVARIANT** é definido como VT \_ UI4.

O **membro uintVal** da estrutura **PROPVARIANT** contém uma máscara de configuração de canal que é lançada para o **tipo UINT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio principais](core-audio-properties.md)
</dt> </dl>

 

 




