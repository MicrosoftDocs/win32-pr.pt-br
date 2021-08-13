---
description: Gerado pela Sessão de Mídia quando o formato muda em um sink de mídia.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Evento MESessionStreamSinkFormatChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08d086d5966e0fc1f6ce4b4b3d639b40d795a4e05799f3928f61afa9abddf4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268586"
---
# <a name="mesessionstreamsinkformatchanged-event"></a>Evento MESessionStreamSinkFormatChanged

Gerado pela Sessão de Mídia quando o formato muda em um sink de mídia.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para esse evento.



| Atributo                                                                    | Descrição                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**NÓ DE \_ SAÍDA DO \_ EVENTO \_ MF**](mf-event-output-node-attribute.md)<br/> | Identifica o nó de topologia para o sink de mídia cujo formato foi alterado.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




