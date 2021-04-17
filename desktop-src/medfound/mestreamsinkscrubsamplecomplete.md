---
description: Gerado por um coletor de fluxo quando ele conclui uma solicitação de depuração.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812803"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>Evento MEStreamSinkScrubSampleComplete

Gerado por um coletor de fluxo quando ele conclui uma solicitação de depuração.

A depuração ocorre quando a taxa de reprodução é zero e o relógio de apresentação é iniciado com um horário de srubbing especificado. Se um coletor de mídia der suporte à depuração, cada fluxo do coletor gerará esse evento sempre que o método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) for chamado enquanto a taxa de reprodução for zero.

Se o fluxo renderiza dados durante a limpeza, ele envia o evento assim que os dados são renderizados. Se o fluxo não renderizar dados, ele envia o evento imediatamente após a chamada de [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                              | Descrição                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tempo de \_ SCRUBSAMPLE do evento MF \_**](mf-event-scrubsample-time-attribute.md)<br/> | Tempo de apresentação para o qual os dados foram renderizados. Se o coletor de mídia não renderizar dados durante a depuração, ele não definirá esse atributo.<br/> <br/> |



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
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




