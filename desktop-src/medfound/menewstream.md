---
description: Gerado por uma fonte de mídia quando ele inicia um novo fluxo.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499b7899c499e87a45e9b7f043db94724b41d729d3b836e7c9f8d71d83616841
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228765"
---
# <a name="menewstream-event"></a>Evento MENewStream

Gerado por uma fonte de mídia quando ele inicia um novo fluxo.

Quando o [**método IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é chamado em uma fonte de mídia, a fonte de mídia envia um evento para cada fluxo selecionado:

-   A origem envia o evento MENewStream se o fluxo não foi selecionado na  chamada anterior para Iniciar [**ou**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)essa é a primeira chamada para Iniciar nessa fonte de mídia.

-   A origem enviará [o evento MEUpdatedStream](meupdatedstream.md) se o fluxo já tiver sido selecionado na chamada anterior para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Nenhum evento é enviado para fluxos não selecionados.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Contém um ponteiro para a interface [**IMFMediaStream do**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) fluxo.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




