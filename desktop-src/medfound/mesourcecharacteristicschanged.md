---
description: Gerado por uma origem de mídia quando as características das fontes são alteradas.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Evento MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd69be00727ec3f1f635b82fb6c8e29c4016959ced480be4e9de6b8a83cfe8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877363"
---
# <a name="mesourcecharacteristicschanged-event"></a>Evento MESourceCharacteristicsChanged

Gerado por uma origem de mídia quando as características da fonte são alteradas.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                                                   | Descrição                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_características de \_ origem do evento MF \_**](mf-event-source-characteristics-attribute.md)<br/>          | Novas características da origem da mídia.<br/> <br/>      |
| [**\_características de origem do evento MF \_ \_ \_ antigas**](mf-event-source-characteristics-old-attribute.md)<br/> | Características anteriores da origem de mídia.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




