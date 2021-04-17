---
description: 'Gerado pela origem do sequenciador quando o método IMFSequencerSource:: UpdateTopology é concluído de forma assíncrona.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Evento MESequencerSourceTopologyUpdated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766506"
---
# <a name="mesequencersourcetopologyupdated-event"></a>Evento MESequencerSourceTopologyUpdated

Gerado pela origem do sequenciador quando o método [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) é concluído de forma assíncrona.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE            | Descrição                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_UI4 VT<br/> | Identificador do elemento Sequencer da topologia que está sendo atualizada. O aplicativo especifica esse valor no parâmetro *dwID* do método [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento sinaliza que a origem do sequenciador atualizou a topologia, mas não significa que a topologia está pronta para reprodução. O aplicativo deve aguardar o evento [MESessionTopologyStatus](mesessiontopologystatus.md) .

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

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 




