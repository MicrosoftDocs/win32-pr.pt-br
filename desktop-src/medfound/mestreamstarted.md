---
description: Gerado por um fluxo de mídia quando a origem é iniciada sem busca. Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a385516a6f0f973dd5bd0453d6c9751a0f7411a8ea43cb6acb936d8601c5272
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113936"
---
# <a name="mestreamstarted-event"></a>Evento MEStreamStarted

Gerado por um fluxo de mídia quando a origem é iniciada sem busca. Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento [MESourceStarted](mesourcestarted.md) .

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/>                                                                          |
| VT \_ i8<br/>    | A hora de início, em unidades de 100 nanossegundos, em relação aos carimbos de data/hora nos exemplos.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




