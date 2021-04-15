---
description: Gerado quando uma fonte de mídia é iniciada sem busca.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Evento MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502392"
---
# <a name="mesourcestarted-event"></a>Evento MESourceStarted

Gerado quando uma fonte de mídia é iniciada sem busca.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento. A hora de início foi a partir da posição atual.<br/> <br/>                            |
| VT \_ i8<br/>    | A hora de início, em unidades de 100 nanossegundos, em relação aos carimbos de data/hora nos exemplos.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                                     | Descrição                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ início real da origem do evento MF \_ \_**](mf-event-source-actual-start-attribute.md)<br/> | Hora de início. A origem de mídia define esse atributo se ele for reiniciado a partir de sua posição atual.<br/> <br/>                     |
| [**\_ \_ Início falso da origem do evento MF \_ \_**](mf-event-source-fake-start-attribute.md)<br/>     | Especifica se a topologia de segmento atual está vazia. A origem do sequenciador define esse atributo.<br/> <br/>             |
| [**\_origem do evento MF \_ \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)<br/>  | Hora de início de um segmento, em relação ao início da apresentação. A origem do sequenciador define esse atributo.<br/> <br/> |



## <a name="remarks"></a>Comentários

Uma origem de mídia gera esse evento quando ele é iniciado a partir de um estado parado ou inicia de um estado em pausa na mesma posição na origem. O evento será gerado se o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) retornar S \_ OK.

Se a origem da mídia iniciar a partir da posição atual e o estado anterior da origem estiver em execução ou em pausa, os dados do evento poderão ser vazios (VT \_ vazio). Se os dados do evento forem VT \_ vazio, a origem da mídia poderá definir o atributo de [**\_ \_ \_ \_ início real da origem do evento MF**](mf-event-source-actual-start-attribute.md) com a hora de início real.

Se a origem da mídia iniciar a partir de uma nova posição ou se o estado anterior da origem tiver sido interrompido, os dados do evento deverão ser a hora de início (VT \_ i8).

Se o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) fizer uma busca, a origem da mídia enviará o evento [MESourceSeeked](mesourceseeked.md) em vez de MESourceStarted.

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

 

 




