---
description: Enviado por uma Media Foundation de transformação assíncrona (MFT) para solicitar um novo exemplo de entrada.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc15bdffebfd22b4aecac2818da85e39379f681aec0e12fe92f895824edb78f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013496"
---
# <a name="metransformneedinput-event"></a>Evento METransformNeedInput

Enviado por uma Media Foundation de transformação assíncrona (MFT) para solicitar um novo exemplo de entrada.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição               |
|----------------------|---------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                        | Descrição                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID do \_ fluxo de entrada do MFT do evento MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | O identificador do fluxo que precisa de dados de entrada.<br/>*Necessária*<br/> |



## <a name="remarks"></a>Comentários

MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . O MFTs síncrono nunca envia este evento.

Quando o cliente do MFT receber esse evento, ele deverá chamar [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para entregar o próximo exemplo. O atributo de [ID do fluxo de entrada do \_ MFT do evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) do objeto de evento especifica qual fluxo de entrada requer dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> </dl>

 

 




