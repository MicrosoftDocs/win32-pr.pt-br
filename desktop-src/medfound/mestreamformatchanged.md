---
description: Gerado por um fluxo de mídia quando o tipo de mídia do fluxo muda.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Evento MEStreamFormatChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762f65beb26f5095c9e89be845f468e3ca53c9b5cd227916bb7cc38417626c60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957266"
---
# <a name="mestreamformatchanged-event"></a>Evento MEStreamFormatChanged

Gerado por um fluxo de mídia quando o tipo de mídia do fluxo muda.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) do novo tipo de mídia.<br/> <br/> |



## <a name="remarks"></a>Comentários

Use esse evento para sinalizar alterações de formato no fluxo.

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

 

 




