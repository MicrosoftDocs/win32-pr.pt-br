---
description: Gerado por um fluxo de mídia quando a origem é iniciada sem busca. Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765732"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




