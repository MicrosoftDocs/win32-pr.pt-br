---
description: Um renderador de vídeo requer uma reint.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edd498d84aaace460a10c88d5579c2f5a87bba42e1a5f393786134bbe727af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102786"
---
# <a name="ec_repaint"></a>EC \_ REPAINT

Um renderador de vídeo requer uma reint.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada do renderador de vídeo ou **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O *parâmetro lParam1* pode especificar o pino de entrada do renderador de vídeo. Nesse caso, o gerenciador de grafo de filtro localiza o pino de saída conectado a esse pino e o consulta para a interface [**IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) Se o pino de saída for compatível com **IMediaEventSink,** o gerenciador de grafo de filtro chamará [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) com o código de evento EC \_ REPAINT. Isso oferece ao filtro upstream a oportunidade de enviar o último exemplo.

Se *lParam1* for **NULL** ou se o pino não der suporte a [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)ou se o método [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) falhar, o gerenciador de grafo de filtro manipulará o evento EC \_ REPAINT sozinho. Seu comportamento depende do estado do grafo:

-   Em execução: ignora o evento . (O renderador receberá o próximo exemplo no fluxo.)
-   Pausado: busca o grafo para seu local atual, liberando o filtro e ensoando os dados.
-   Parado: pausa e interrompe o grafo, ressando os dados na fila.

Por padrão, o gerenciador de grafo de filtro não passa esse evento para o aplicativo.

## <a name="remarks"></a>Comentários

Os renderadores de vídeo enviam essa mensagem quando recebem uma mensagem [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) e não têm dados a exibir.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

