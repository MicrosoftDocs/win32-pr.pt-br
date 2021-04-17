---
description: Gerado por uma origem de mídia quando ele inicia um novo fluxo.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760991"
---
# <a name="menewstream-event"></a>Evento MENewStream

Gerado por uma origem de mídia quando ele inicia um novo fluxo.

Quando o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é chamado em uma origem de mídia, a origem da mídia envia um evento para cada fluxo selecionado:

-   A origem envia o evento MENewStream se o fluxo não foi selecionado na chamada anterior para [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou esta é a primeira chamada para **Iniciar** nesta fonte de mídia.

-   A origem enviará o evento [MEUpdatedStream](meupdatedstream.md) se o fluxo já tiver sido selecionado na chamada anterior para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Nenhum evento é enviado para fluxos não selecionados.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ desconhecido<br/> | Contém um ponteiro para a interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) do fluxo.<br/> <br/> |



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

 

 




