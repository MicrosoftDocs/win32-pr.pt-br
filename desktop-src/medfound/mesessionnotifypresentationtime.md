---
description: Gerado pela sessão de mídia quando uma nova apresentação é iniciada. Esse evento indica quando a apresentação será iniciada e o deslocamento entre a hora da apresentação e a hora da origem.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752589"
---
# <a name="mesessionnotifypresentationtime-event"></a>Evento MESessionNotifyPresentationTime

Gerado pela sessão de mídia quando uma nova apresentação é iniciada. Esse evento indica quando a apresentação será iniciada e o deslocamento entre a hora da apresentação e a hora da origem.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                                                                   | Descrição                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_hora de \_ início da \_ apresentação \_ do evento MF**](mf-event-start-presentation-time-attribute.md)<br/>                       | Hora de início da apresentação.<br/> <br/>                                                      |
| [**\_deslocamento do \_ tempo de apresentação do evento MF \_ \_**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Deslocamento entre o tempo de apresentação e os carimbos de data/hora da fonte de mídia.<br/> <br/>                 |
| [**\_ \_ \_ hora de início da apresentação do evento MF \_ \_ na \_ saída**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Hora da apresentação quando os coletores de mídia processarão o primeiro exemplo da nova topologia.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




