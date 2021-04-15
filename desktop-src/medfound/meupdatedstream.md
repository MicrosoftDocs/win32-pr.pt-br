---
description: Gerado por uma origem de mídia quando ele é reiniciado ou busca um fluxo que já está ativo.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506044"
---
# <a name="meupdatedstream-event"></a>Evento MEUpdatedStream

Gerado por uma origem de mídia quando ele é reiniciado ou busca um fluxo que já está ativo.

Quando o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é chamado em uma origem de mídia, a origem da mídia envia um evento para cada fluxo selecionado:

-   A origem envia o evento [MENewStream](menewstream.md) se o fluxo não foi selecionado na chamada anterior para [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou esta é a primeira chamada para **Iniciar** nesta fonte de mídia.

-   A origem enviará o evento MEUpdatedStream se o fluxo já tiver sido selecionado na chamada anterior para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Nenhum evento é enviado para fluxos não selecionados.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) do fluxo.<br/> <br/> |



## <a name="remarks"></a>Comentários

Na primeira chamada para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) em que um fluxo se torna ativo, a origem da mídia envia um evento [MENewStream](menewstream.md) para o fluxo. Em chamadas subsequentes para **Iniciar**, a origem da mídia envia um evento MEUpdatedStream até que o fluxo seja desmarcado.

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

 

 




