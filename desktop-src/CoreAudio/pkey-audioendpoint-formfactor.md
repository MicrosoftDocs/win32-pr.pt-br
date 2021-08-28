---
description: A propriedade \_ FormFactor de AudioEndpoint \_ PKEY especifica o fator forma do dispositivo de ponto de extremidade de áudio. O fator forma indica os atributos físicos do dispositivo de ponto de extremidade de áudio que o usuário manipula.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76b53b91a03cda5e8484878f62c3c7a205e422f53ed647d29cca6435e0f14f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018334"
---
# <a name="pkey_audioendpoint_formfactor"></a>PKEY \_ AudioEndpoint \_ FormFactor

A **propriedade \_ \_ FormFactor de AudioEndpoint PKEY** especifica o fator forma do dispositivo de ponto de extremidade de áudio. O fator forma indica os atributos físicos do dispositivo de ponto de extremidade de áudio que o usuário manipula.

O **membro vt** da estrutura **PROPVARIANT** é definido como VT \_ UI4.

O **membro uintVal** da estrutura **PROPVARIANT** contém um valor de enumeração que é lançado para o tipo UINT. Ele é definido como um dos seguintes valores [**de enumeração EndpointFormFactor:**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)

-   RemoteNetworkDevice
-   Speakers
-   LineLevel
-   Auscultadores
-   Microfone
-   Headset
-   Aparelho
-   UnknownDigitalPassthrough
-   Spdif
-   HDMI
-   UnknownFormFactor

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
</dt> </dl>

 

 




