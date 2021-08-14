---
description: Sinaliza que um fluxo de mídia não tem dados disponíveis em um momento especificado.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42b72a61964e296ac5f7aa69eb2be6773b622f7b44df8300affa0150af2f8a77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974055"
---
# <a name="mestreamtick-event"></a>Evento MEStreamTick

Sinaliza que um fluxo de mídia não tem dados disponíveis em um momento especificado.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype           | Descrição                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ I8<br/> | Hora em que a lacuna ocorre, em unidades de 100 nanossegundos.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento sinaliza uma lacuna nos dados. O evento notifica os componentes downstream para não esperar dados no momento especificado.

O evento deve ser enviado por qualquer objeto que gere os carimbos de data/hora para os exemplos de mídia no fluxo. Dependendo do formato dos dados, isso é:

-   O fluxo de mídia na fonte de mídia (interface [**IMFMediaStream)**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ou
-   A transformação do decodificador ( interface [**IMFTransform).**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Durante a lacuna, o objeto deve enviar o evento com a mesma frequência que normalmente produziria amostras. Para o vídeo, envie um evento para cada quadro ausente. Para áudio, envie o evento pelo menos uma vez por segundo durante a lacuna. O valor do evento é o carimbo de data/hora do exemplo ausente. Envie quantos eventos MEStreamTick necessários para preencher a lacuna nos dados.

Se uma fonte de mídia tiver vários fluxos e houver uma lacuna em mais de um fluxo, cada fluxo deverá enviar eventos MEStreamTick. Por exemplo, se houver uma lacuna nos dados de áudio e vídeo, ambos os fluxos enviarão o evento.

O evento MEStreamTick não conclui uma [**solicitação IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) A fonte de mídia ainda deve enviar um [evento MEMediaSample](memediasample.md) para cada chamada para **RequestSample.**

Os sinks de mídia não podem consumir esse evento diretamente. Para sinalizar uma lacuna no fluxo para um sink de mídia, chame [**IMFStreamSink::P marker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) com um marcador TICK DE MARCADOR **MFSTREAMSINK. \_ \_** O Media Foundation pipeline converte eventos MEStreamTick em marcadores **MFSTREAMSINK \_ MARKER \_ TICK** quando necessário.

Não de definir o [**atributo MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) no próximo exemplo de mídia após um evento MEStreamTick. O atributo **MFSampleExtension \_ Discontinuity** implica que o carimbo de data/hora é descontinuado com carimbos de data/hora anteriores, enquanto MEStreamTick implica que os carimbos de data/hora são contínuos, mas alguns dados estão ausentes.

> [!Note]  
> Uma versão anterior da documentação incorretamente declarou que o exemplo após um evento MEStreamTick deve ter o atributo [**MFSampleExtension \_ Discontinuity.**](mfsampleextension-discontinuity-attribute.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




