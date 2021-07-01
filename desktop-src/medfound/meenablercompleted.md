---
description: Gerado por um objeto do habilitador de conteúdo quando os objetos que habilitam a ação são concluídos.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119441"
---
# <a name="meenablercompleted-event"></a>Evento MEEnablerCompleted

Gerado por um objeto do habilitador de conteúdo quando a ação de habilitação do objeto é concluída. Objetos que expõem a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) podem autenuá-lo. O evento será gerado se um dos seguintes eventos ocorrer:

-   O [**método IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) é concluído de forma assíncrona.
-   O aplicativo chama [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)e, em seguida, o aplicativo conclui a solicitação HTTP POST, conforme descrito no **método MonitorEnable.**

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

O código de status do evento pode conter um dos valores a seguir.



| Valor                                     | Descrição                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **S \_ OK**                            | A operação foi realizada com êxito.                                                                                                                                                        |
| **NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED** | A licença drm não foi adquirida. Se a tentativa anterior tiver [**usado AutomaticEnable,**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)o aplicativo deverá tentar a aquisição não silenciosa. |
| **NS \_ S \_ DRM \_ MONITOR \_ CANCELLED**   | A [**operação MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) foi cancelada.                                                                                            |



 

Para receber esse evento, consulte a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para a interface [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Em seguida, [**chame IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), conforme descrito no tópico [Geradores](media-event-generators.md)de Eventos de Mídia .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente \[ aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2008 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Geradores de eventos de mídia](media-event-generators.md)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




