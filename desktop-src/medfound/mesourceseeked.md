---
description: 'Gerado quando uma fonte de mídia busca uma nova posição. Uma fonte de mídia gerará esse evento se a fonte estiver em execução ou em pausa e o aplicativo chamar IMFMediaSource:: Start com uma hora de início que não seja igual à posição atual.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b913089ca40895a782f3c013b752db25fe754443ae6d79b410da98e759b4b8ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941406"
---
# <a name="mesourceseeked-event"></a>Evento MESourceSeeked

Gerado quando uma fonte de mídia busca uma nova posição. Uma fonte de mídia gerará esse evento se a fonte estiver em execução ou em pausa e o aplicativo chamar [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) com uma hora de início que não seja igual à posição atual.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE           | Descrição                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ i8<br/> | A nova posição inicial, em unidades de 100 a nanossegundos.<br/> <br/> |



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

 

 




