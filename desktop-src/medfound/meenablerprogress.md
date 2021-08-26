---
description: Sinaliza o progresso de um objeto do habilitador de conteúdo. Objetos que expõem a interface IMFContentEnabler podem ative esse evento para notificar o aplicativo sobre o progresso das ações dos habilitadores de conteúdo.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Evento MEEnablerProgress (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9772a076e1d9de0cff2336b4c6d6b9b068f11e4fc572b44f0f914a8353f651bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013756"
---
# <a name="meenablerprogress-event"></a>Evento MEEnablerProgress

Sinaliza o progresso de um objeto do habilitador de conteúdo. Objetos que expõem a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) podem ative esse evento para notificar o aplicativo sobre o progresso das ações do habilitador de conteúdo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype               | Descrição                                                               |
|-----------------------|---------------------------------------------------------------------------|
| VT \_ LPWSTR<br/> | Cadeia de caracteres largos que descreve o progresso.<br/> <br/> |



## <a name="remarks"></a>Comentários

Para receber esse evento, consulte a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para a interface [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Em seguida, [**chame IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), conforme descrito no tópico [Geradores](media-event-generators.md)de Eventos de Mídia .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Geradores de eventos de mídia](media-event-generators.md)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




