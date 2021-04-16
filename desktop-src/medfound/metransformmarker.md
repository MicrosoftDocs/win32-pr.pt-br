---
description: Enviado por uma Media Foundation de transformação assíncrona (MFT) em resposta a uma \_ mensagem de marcador de comando de mensagem MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757716"
---
# <a name="metransformmarker-event"></a>Evento METransformMarker

Enviado por uma Media Foundation de transformação assíncrona (MFT) em resposta a uma mensagem de **\_ marcador de \_ comando \_ de mensagem MFT** .

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição               |
|----------------------|---------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                      | Descrição                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [\_contexto de \_ MFT do evento MF \_](mf-event-mft-context.md)<br/> | O valor do parâmetro *ulParam* da mensagem do **\_ marcador de \_ comando \_ da mensagem MFT** .<br/>*Necessária*<br/> |



## <a name="remarks"></a>Comentários

MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . O MFTs síncrono nunca envia este evento.

O cliente de uma MFT assíncrona pode inserir um marcador no fluxo chamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem **do \_ \_ \_ marcador de comando de mensagem MFT** . O parâmetro *ulParam* contém dados definidos pelo aplicativo.

Quando o MFT termina de processar todos os dados de entrada que estavam disponíveis no momento da chamada [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , o MFT enfileira um evento METransformMarker. O atributo de [contexto de \_ MFT do evento \_ \_ MF](mf-event-mft-context.md) do evento contém o valor do parâmetro *ulParam* . Para obter mais informações, consulte [assíncrona MFTs](asynchronous-mfts.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> </dl>

 

 




