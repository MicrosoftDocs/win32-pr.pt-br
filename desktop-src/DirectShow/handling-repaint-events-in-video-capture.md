---
description: Manipulando eventos redesenhados na captura de vídeo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Manipulando eventos redesenhados na captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920047"
---
# <a name="handling-repaint-events-in-video-capture"></a>Manipulando eventos redesenhados na captura de vídeo

Se você criar um grafo de captura de vídeo sem usar a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) e visualizar o vídeo usando o filtro antigo de processamento de vídeo, deverá substituir o tratamento padrão para [**eventos \_ Repaints do EC**](ec-repaint.md) . Consulte o Gerenciador do grafo de filtro para a interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) e chame o método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) com o valor EC \_ Repaint:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Isso impede um possível erro que pode corromper o arquivo de captura. Se o usuário cobrir e descobrir a janela de visualização, o filtro de processamento de vídeo receberá uma mensagem de pintura do WM \_ . Por padrão, o processador de vídeo solicita um novo quadro e o Gerenciador de gráficos de filtro pausa o grafo para marcar outro quadro de vídeo. Se isso acontecer enquanto o grafo estiver gravando um arquivo, ele corromperá o arquivo. Substituir o comportamento padrão de \_ redesenho do EC impede que o renderizador solicite um novo quadro.

Você não precisará executar esta etapa se estiver usando a interface **ICaptureGraphBuilder2** , pois o construtor do grafo de captura faz isso para você automaticamente. Além disso, ele não será necessário se você estiver usando o VMR (processador de mixagem de vídeo) para visualização. O VMR sempre tem o quadro mais recente disponível, portanto, não envia eventos de \_ redesenho de EC.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



