---
description: Gerado por uma fonte de mídia quando ele reinicia ou busca um fluxo que já está ativo.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5746b619f885ab7648110cbe58b66b7897c839031202d811becd33e1c84991a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974015"
---
# <a name="meupdatedstream-event"></a>Evento MEUpdatedStream

Gerado por uma fonte de mídia quando ele reinicia ou busca um fluxo que já está ativo.

Quando o [**método IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é chamado em uma fonte de mídia, a fonte de mídia envia um evento para cada fluxo selecionado:

-   A origem envia [o evento MENewStream](menewstream.md) se o fluxo não foi selecionado na  chamada anterior para Iniciar [**ou**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)essa é a primeira chamada para Iniciar nessa fonte de mídia.

-   A origem enviará o evento MEUpdatedStream se o fluxo já tiver sido selecionado na chamada anterior para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Nenhum evento é enviado para fluxos não selecionados.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFMediaStream do**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) fluxo.<br/> <br/> |



## <a name="remarks"></a>Comentários

Na primeira chamada para [**Iniciar em que**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) um fluxo se torna ativo, a fonte de mídia envia um evento [MENewStream](menewstream.md) para o fluxo. Em chamadas subsequentes para **Iniciar**, a fonte de mídia envia um evento MEUpdatedStream, até que o fluxo seja desseletório.

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

 

 




