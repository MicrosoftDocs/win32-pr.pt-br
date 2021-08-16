---
description: Enviado por uma transformação de Media Foundation (MFT) assíncrona para solicitar um novo exemplo de entrada.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects.h)
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

Enviado por uma transformação de Media Foundation (MFT) assíncrona para solicitar um novo exemplo de entrada.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição               |
|----------------------|---------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para esse evento.



| Atributo                                                                        | Descrição                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID DO FLUXO \_ \_ DE ENTRADA MFT DO EVENTO \_ \_ \_ MF](mf-event-mft-input-stream-id.md)<br/> | O identificador do fluxo que precisa de dados de entrada.<br/>*(Obrigatório)*<br/> |



## <a name="remarks"></a>Comentários

Os MFTs assíncronos enviam esse evento por meio da interface [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Os MFTs síncronos nunca enviam esse evento.

Quando o cliente do MFT recebe esse evento, ele deve chamar [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para entregar o próximo exemplo. O [atributo MF \_ EVENT \_ MFT INPUT STREAM \_ \_ \_ ID](mf-event-mft-input-stream-id.md) do objeto de evento especifica qual fluxo de entrada requer dados.

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

 

 




