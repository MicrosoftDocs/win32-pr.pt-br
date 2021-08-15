---
description: Gerado por uma fonte de mídia que fornece topologias por meio da interface IMFMediaSourceTopologyProvider, como a origem do sequenciador. A origem gera o evento quando ele tem uma nova apresentação. A sessão de mídia encaminha esse evento para o aplicativo.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2adec5b3dbb8544e537bdcc8f5c724130175b3167f9c51dc005112fdbd9a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228876"
---
# <a name="menewpresentation-event"></a>Evento MENewPresentation

Gerado por uma fonte de mídia que fornece topologias por meio da interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , como a origem do sequenciador. A origem gera o evento quando ele tem uma nova apresentação. A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação da nova apresentação.<br/> <br/> |



## <a name="remarks"></a>Comentários

O aplicativo pode obter a topologia que corresponde ao descritor de apresentação chamando [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) na origem da mídia. O aplicativo pode então enfileirar a nova topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 




