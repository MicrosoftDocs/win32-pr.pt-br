---
description: Sinaliza que um fluxo de mídia não tem dados disponíveis em um horário especificado.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793395"
---
# <a name="mestreamtick-event"></a>Evento MEStreamTick

Sinaliza que um fluxo de mídia não tem dados disponíveis em um horário especificado.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE           | Descrição                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ i8<br/> | Hora em que a lacuna ocorre, em unidades de 100 a nanossegundos.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento sinaliza uma lacuna nos dados. O evento notifica os componentes downstream para não esperar nenhum dado no tempo especificado.

O evento deve ser enviado por qualquer objeto que gere os carimbos de data/hora para os exemplos de mídia no fluxo. Dependendo do formato dos dados, isso é o seguinte:

-   O fluxo de mídia na origem da mídia (interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ) ou
-   A transformação do decodificador (interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).

Durante a lacuna, o objeto deve enviar o evento, com a frequência em que normalmente produziria amostras. Para vídeo, envie um evento para cada quadro ausente. Para áudio, envie o evento pelo menos uma vez por segundo durante o intervalo. O valor do evento é o carimbo de data/hora do exemplo ausente. Envie quantos eventos MEStreamTick forem necessários para preencher a lacuna nos dados.

Se uma fonte de mídia tiver vários fluxos e houver um intervalo em mais de um fluxo, cada fluxo deverá enviar eventos MEStreamTick. Por exemplo, se houver uma lacuna nos dados de áudio e de vídeo, ambos os fluxos enviarão o evento.

O evento MEStreamTick não conclui uma solicitação [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . A origem da mídia ainda deve enviar um evento [MEMediaSample](memediasample.md) para cada chamada para **RequestSample**.

Os coletores de mídia não podem consumir esse evento diretamente. Para sinalizar uma lacuna no fluxo para um coletor de mídia, chame [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) com um marcador de **\_ \_ tique MFSTREAMSINK** . O pipeline de Media Foundation converte eventos MEStreamTick em marcadores de **\_ \_ tique de marcador MFSTREAMSINK** quando necessário.

Não defina o atributo [**de \_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) no próximo exemplo de mídia após um evento MEStreamTick. O atributo de **\_ descontinuidade MFSampleExtension** implica que o carimbo de data/hora é descontínuo com carimbos de data/hora anteriores, enquanto MEStreamTick implica que os carimbos de hora são contínuos, mas alguns dados estão ausentes

> [!Note]  
> Uma versão anterior da documentação incorretamente afirmou que o exemplo depois de um evento MEStreamTick deve ter o atributo [**de \_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




