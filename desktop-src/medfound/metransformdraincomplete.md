---
description: Enviado por uma MFT (transformação Media Foundation assíncrona) quando uma operação de esgotamento é concluída.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5ab03ac5027d1dc7549e7b7f0b8494cd8066b07afb64c5df17415a4986866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974025"
---
# <a name="metransformdraincomplete-event"></a>Evento METransformDrainComplete

Enviado por uma MFT (transformação Media Foundation assíncrona) quando uma operação de esgotamento é concluída.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição               |
|----------------------|---------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para esse evento.



| Atributo                                                                        | Descrição                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [ID DO FLUXO \_ \_ DE ENTRADA MFT DO EVENTO \_ \_ \_ MF](mf-event-mft-input-stream-id.md)<br/> | O identificador do fluxo que foi esvaziado.<br/>*(Obrigatório)*<br/> |



## <a name="remarks"></a>Comentários

Os MFTs assíncronos enviam esse evento por meio da interface [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Os MFTs síncronos nunca enviam esse evento.

Para esvaziar uma MFT, chame [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem DRAIN do COMANDO DE MENSAGEM **\_ \_ \_ MFT.** Especifique o fluxo de entrada a ser esvaziado no *parâmetro ulParam.* Quando a operação de dreno é concluída, um MFT assíncrono envia o evento METransformDrainComplete. O [atributo MF \_ EVENT \_ MFT INPUT STREAM \_ \_ \_ ID](mf-event-mft-input-stream-id.md) do evento contém o identificador de fluxo dado no *parâmetro ulParam.*

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

 

 




