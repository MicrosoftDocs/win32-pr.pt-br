---
description: Enviado por uma Media Foundation de transformação assíncrona (MFT) quando uma operação de descarga é concluída.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297398"
---
# <a name="metransformdraincomplete-event"></a>Evento METransformDrainComplete

Enviado por uma Media Foundation de transformação assíncrona (MFT) quando uma operação de descarga é concluída.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição               |
|----------------------|---------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                        | Descrição                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [\_ID do \_ fluxo de entrada do MFT do evento MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | O identificador do fluxo que foi esgotado.<br/>*Necessária*<br/> |



## <a name="remarks"></a>Comentários

MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . O MFTs síncrono nunca envia este evento.

Para drenar uma MFT, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem de **dreno de \_ \_ comando \_ de mensagem MFT** . Especifique o fluxo de entrada a ser esgotado no parâmetro *ulParam* . Quando a operação de descarga é concluída, um MFT assíncrono envia o evento METransformDrainComplete. O atributo de [ID do fluxo de entrada do \_ MFT do evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) do evento contém o identificador de fluxo fornecido no parâmetro *ulParam* .

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

 

 




