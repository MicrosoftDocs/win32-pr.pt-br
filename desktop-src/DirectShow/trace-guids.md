---
description: Os GUIDs a seguir são usados para rastreamento de eventos no DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUIDs de rastreamento (PerfStruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753498"
---
# <a name="trace-guids"></a>GUIDs de rastreamento

Os GUIDs a seguir são usados para rastreamento de eventos no DirectShow.



| GUID                                                                                                                                                                   | Descrição                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**\_AUDIOBREAK GUID**</dt> </dl>    | Evento de quebra de áudio. Eventos desse tipo usam a estrutura [**PERFINFO do \_ DShow \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) para dados de evento.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**\_CTL de DShow de GUID \_**</dt> </dl>      | Provedor de eventos do DirectShow.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**\_STREAMTRACE GUID**</dt> </dl> | Evento de streaming geral. Eventos desse tipo usam a estrutura [**PERFINFO do \_ DShow \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) para dados de evento.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**\_VIDEOREND GUID**</dt> </dl>       | Evento de renderização de vídeo. Eventos desse tipo usam a estrutura [**PERFINFO do \_ DShow \_ AVREND**](perfinfo-dshow-avrend.md) para dados de evento.<br/>             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PerfStruct. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Rastreamento de eventos no DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




