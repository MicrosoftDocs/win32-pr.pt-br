---
description: Gerado por uma origem de mídia quando uma apresentação termina. Esse evento sinaliza que todos os fluxos na apresentação são concluídos. A sessão de mídia encaminha esse evento para o aplicativo.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Evento MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e97a2689b8d0e2ae156daa84f27f0e10fb31b828ffedf027a7be47a6c330b7b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941455"
---
# <a name="meendofpresentation-event"></a>Evento MEEndOfPresentation

Gerado por uma origem de mídia quando uma apresentação termina. Esse evento sinaliza que todos os fluxos na apresentação são concluídos. A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                                               | Descrição                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_topologia de origem do evento MF \_ \_ \_ cancelada**](mf-event-source-topology-canceled-attribute.md)<br/> | Especifica se a origem do sequenciador cancelou esta apresentação.<br/> <br/> |



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

 

 




