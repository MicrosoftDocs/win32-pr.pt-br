---
description: Manipulando eventos de repintar na Captura de Vídeo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Manipulando eventos de repintar na Captura de Vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433a9897c7c69119eb54d088aff2d22536e20ae43760cc6b4c9430f9a44f6814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999755"
---
# <a name="handling-repaint-events-in-video-capture"></a>Manipulando eventos de repintar na Captura de Vídeo

Se você criar um grafo de captura de vídeo sem usar a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) e visualizar o vídeo usando o filtro antigo do Renderador de Vídeo, deverá substituir a manipulação padrão para eventos [**\_ EC REPAINT.**](ec-repaint.md) Consulte o Gerenciador de Graph Filtro para a interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) e chame o método [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) com o valor EC \_ REPAINT:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Isso impede um possível erro que pode corromper o arquivo de captura. Se o usuário cobrir e descobrir a janela de visualização, o filtro do Renderador de Vídeo receberá uma mensagem WM \_ PAINT. Por padrão, o Renderador de Vídeo solicita um novo quadro e o Gerenciador de filtros Graph pausa o grafo para indicação de outro quadro de vídeo. Se isso acontecer enquanto o grafo estiver escrevendo um arquivo, ele corrompe o arquivo. A substituição do comportamento \_ PADRÃO DE REPAINT da EC impede que o renderizado solicite um novo quadro.

Você não precisa executar esta etapa se estiver usando a interface **ICaptureGraphBuilder2,** pois o Construtor Graph Capture faz isso automaticamente. Além disso, não será necessário se você estiver usando o VMR (Video Mixing Renderer) para visualização. A VMR sempre tem o quadro mais recente disponível, portanto, não envia eventos \_ EC REPAINT.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



