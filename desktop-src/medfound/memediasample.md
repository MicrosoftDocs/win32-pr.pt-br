---
description: 'Enviado quando um fluxo de mídia fornece um novo exemplo em resposta a uma chamada para IMFMediaStream:: RequestSample.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Evento MEMediaSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105764979"
---
# <a name="memediasample-event"></a>Evento MEMediaSample

Enviado quando um fluxo de mídia fornece um novo exemplo em resposta a uma chamada para [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) do exemplo.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> </dl>

 

 




