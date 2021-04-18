---
description: Um processador de vídeo requer um redesenho.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760095"
---
# <a name="ec_repaint"></a>redesenho de EC \_

Um processador de vídeo requer um redesenho.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada do processador de vídeo ou **NULL**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O parâmetro *lParam1* pode especificar o pino de entrada do processador de vídeo. Nesse caso, o Gerenciador do grafo de filtro localiza o pino de saída conectado a esse PIN e o consulta para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Se o pino de saída der suporte a **IMediaEventSink**, o Gerenciador de gráfico de filtro chamará [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) com o código de evento do EC \_ Repaint. Isso dá ao filtro upstream a oportunidade de enviar novamente o último exemplo.

Se *lParam1* for **nulo** ou se o PIN não oferecer suporte a [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), ou se o método [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) falhar, o Gerenciador do grafo de filtro tratará o \_ evento Repaint do EC por si só. Seu comportamento depende do estado do grafo:

-   Em execução: ignora o evento. (O renderizador receberá o próximo exemplo no fluxo.)
-   Em pausa: procura o grafo em seu local atual, liberando, assim, o filtro e colocando os dados em fila novamente.
-   Parado: pausa e para o grafo, assim, colocando novamente os dados em fila.

Por padrão, o Gerenciador de gráfico de filtro não passa esse evento para o aplicativo.

## <a name="remarks"></a>Comentários

Os renderizadores de vídeo enviam essa mensagem quando recebem uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e não têm dados a serem exibidos.

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

 

