---
description: Gerado quando um coletor de mídia se torna inválido.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Evento MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164655"
---
# <a name="mesinkinvalidated-event"></a>Evento MESinkInvalidated

Gerado quando um coletor de mídia se torna inválido.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                    | Descrição                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_nó de \_ saída do evento MF \_**](mf-event-output-node-attribute.md)<br/> | Identifica o nó de topologia para este coletor de mídia.<br/> <br/> |



## <a name="remarks"></a>Comentários

A sessão de mídia gerará esse evento se receber qualquer um dos seguintes eventos do coletor de mídia:

-   [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)

-   [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)

-   [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)

-   [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)

-   [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)

Um coletor de mídia também pode gerar esse evento; nesse caso, a sessão de mídia define o atributo de [**\_ nó de \_ saída \_ de evento MF**](mf-event-output-node-attribute.md) no evento e encaminha o evento para o aplicativo.

Se o aplicativo receber esse evento, ele precisará recriar o coletor de mídia e enfileirar a topologia novamente.

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

 

 




