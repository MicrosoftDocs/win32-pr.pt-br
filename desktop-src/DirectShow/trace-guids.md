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
ms.openlocfilehash: 89465996c57e1f1f97f2c101c8dfee99a00219f992a4e68681f76465d21bef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951545"
---
# <a name="trace-guids"></a>GUIDs de rastreamento

Os GUIDs a seguir são usados para rastreamento de eventos no DirectShow.



| GUID                                                                                                                                                                   | Descrição                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**\_AUDIOBREAK GUID**</dt> </dl>    | Evento de quebra de áudio. Eventos desse tipo usam a estrutura [**PERFINFO do \_ DShow \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) para dados de evento.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**\_CTL de DShow de GUID \_**</dt> </dl>      | provedor de eventos de DirectShow.<br/>                                                                                                                        |
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

 

 




