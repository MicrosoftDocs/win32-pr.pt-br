---
description: Gerado por um coletor de fluxo quando o tipo de mídia de coletores não é mais válido.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Evento MEStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165035"
---
# <a name="mestreamsinkformatchanged-event"></a>Evento MEStreamSinkFormatChanged

Gerado por um coletor de fluxo quando o tipo de mídia do coletor não é mais válido.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Um coletor de fluxo pode gerar isso mesmo se algo acontecer invalidando o tipo de mídia do coletor de fluxo. Por exemplo, o processador de vídeo avançado (EVR) envia esse evento quando a exibição é alterada.

O valor **HRESULT** recuperado por [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) pode indicar por que o tipo de mídia não é mais válido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Coletores de mídia](media-sinks.md)
</dt> </dl>

 

 




