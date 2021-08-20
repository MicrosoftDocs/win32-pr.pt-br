---
description: Um novo segmento foi iniciado.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b33d9f75dc4fa8e86b13e61c78b98a19248c16f2f627e1c1b09e536b31a73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015914"
---
# <a name="ec_segment_started"></a>segmento de EC \_ \_ iniciado

Um novo segmento foi iniciado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

( **\_ tempo de referência** const \* ) ponteiro para um valor de **\_ tempo de referência** que especifica o tempo de fluxo acumulado desde o início do segmento, em unidades de 100 nanossegundos.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Número do segmento (baseado em zero).

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Esse evento não é enviado para o aplicativo. Os aplicativos não podem substituir a ação padrão para este evento.

## <a name="remarks"></a>Comentários

Se um filtro enviar um [**\_ fim \_ de \_ segmento do EC**](ec-end-of-segment.md) no final de um segmento, ele enviará esse evento no início do segmento. O Gerenciador do grafo de filtro usa essa notificação de evento para calcular quantas \_ \_ notificações de fim de segmento do EC \_ devem esperar no final do segmento.

Por padrão, os filtros não enviam eventos [**\_ \_ de fim de \_ segmento do EC**](ec-end-of-segment.md) no final dos segmentos e, portanto, não devem enviar esse evento. Para obter mais informações, consulte [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




