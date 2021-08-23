---
description: Recuperando eventos
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Recuperando eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1132b2b0140c86c2be1e7916e8d1de28e231b2eca50596714aaa82346aaf83eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072720"
---
# <a name="retrieving-events"></a>Recuperando eventos

o filtro Graph Manager expõe três interfaces que dão suporte à notificação de eventos.

-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contém o método para filtros para postar eventos.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contém métodos para aplicativos para recuperar eventos.
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) herda de e estende a interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .

os filtros postam notificações de evento chamando o método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) no filtro Graph Manager. Uma notificação de evento consiste em um código de evento, que define o tipo de evento e dois parâmetros que fornecem informações adicionais. Dependendo do código do evento, os parâmetros podem conter ponteiros, códigos de retorno, tempos de referência ou outras informações. Para obter uma lista completa de códigos de eventos e parâmetros, consulte [códigos de notificação de eventos](event-notification-codes.md).

para recuperar um evento da fila, o aplicativo chama o método [**IMediaEvent:: getregular**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) no filtro Graph Manager. Esse método é bloqueado até que haja um evento a ser retornado ou até que um tempo especificado decorra. Supondo que haja um evento em fila, o método retorna com o código do evento e os dois parâmetros de evento. Depois de chamar **GetEvent**, um aplicativo sempre deve chamar o método [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar todos os recursos associados aos parâmetros do evento. Por exemplo, um parâmetro pode ser um valor **BSTR** que foi alocado pelo grafo de filtro.

O exemplo de código a seguir fornece uma descrição de como recuperar eventos da fila.


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



para substituir o filtro padrão do Graph do gerenciador de um evento, chame o método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) com o código do evento como um parâmetro. Você pode restabelecer o tratamento padrão chamando o método [**IMediaEvent:: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) . Se o grafo de filtro não executar nenhum tratamento padrão para o código de evento especificado, chamar esses métodos não terá nenhum efeito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



