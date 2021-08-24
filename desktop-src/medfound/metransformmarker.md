---
description: Enviado por uma transformação de Media Foundation (MFT) assíncrona em resposta a uma mensagem MFT \_ MESSAGE \_ COMMAND \_ MARKER.
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7029119b30314e56531c0afb29accadb67e1efb343a906c2558af2157c0b1f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827036"
---
# <a name="metransformmarker-event"></a>Evento METransformMarker

Enviado por uma transformação de Media Foundation (MFT) assíncrona em resposta a uma **mensagem MFT \_ MESSAGE COMMAND \_ \_ MARKER.**

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição               |
|----------------------|---------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para esse evento.



| Atributo                                                      | Descrição                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CONTEXTO \_ MFT DO EVENTO \_ \_ MF](mf-event-mft-context.md)<br/> | O valor do parâmetro *ulParam* da mensagem **MFT \_ MESSAGE \_ \_ MARKER.**<br/>*(Obrigatório)*<br/> |



## <a name="remarks"></a>Comentários

Os MFTs assíncronos enviam esse evento por meio da interface [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Os MFTs síncronos nunca enviam esse evento.

O cliente de um MFT assíncrono pode colocar um marcador no fluxo chamando [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem **MFT \_ MESSAGE COMMAND \_ \_ MARKER.** O *parâmetro ulParam* contém dados definidos pelo aplicativo.

Quando o MFT concluir o processamento de todos os dados de entrada que estava disponível no momento da chamada [**processMessage,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) o MFT enfilra um evento METransformMarker. O [atributo MF \_ EVENT \_ MFT \_ CONTEXT](mf-event-mft-context.md) do evento contém o valor do *parâmetro ulParam.* Para obter mais informações, consulte [MFTs assíncronos.](asynchronous-mfts.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[MFTs assíncronos](asynchronous-mfts.md)
</dt> </dl>

 

 




