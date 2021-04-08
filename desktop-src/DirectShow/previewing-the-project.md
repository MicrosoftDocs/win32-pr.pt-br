---
description: Visualizando o projeto
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Visualizando o projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920000"
---
# <a name="previewing-the-project"></a>Visualizando o projeto

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Para visualizar o projeto, você precisa de um componente chamado *mecanismo de renderização*, que cria um grafo de filtro do DirectShow a partir de uma linha do tempo. O grafo de filtro é o que realmente renderiza o projeto. Você pode usar o mecanismo de renderização para visualizar um projeto ou gravar o arquivo de saída final.

Este artigo não entra em detalhes sobre o mecanismo de renderização. Para visualização, você só precisa de algumas chamadas de método. Você pode encontrar uma discussão mais completa, incluindo como gravar arquivos de saída, na [renderização de um projeto](rendering-a-project.md). O exemplo de código a seguir mostra como construir um grafo de visualização.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Crie o mecanismo de renderização usando a função **CoCreateInstance** . Em seguida, chame os seguintes métodos na interface [**IRenderEngine**](irenderengine.md) do mecanismo de renderização:

-   [**Settimelineobject**](irenderengine-settimelineobject.md). Especifica a linha do tempo a ser usada.
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md). Cria um gráfico de filtro parcial, com um pino de saída para cada grupo na linha do tempo.
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md). Conclui o grafo de visualização conectando cada pino de saída a um processador de áudio ou vídeo.

Depois que o grafo for criado, você poderá visualizar o projeto executando o grafo, como faria com qualquer grafo de filtro do DirectShow. Primeiro, obtenha um ponteiro para o grafo de filtro chamando o método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) .


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Consulte o grafo de filtro para as interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) . Use essas duas interfaces para executar o grafo e aguardar a reprodução ser concluída. Para obter uma explicação de como usar essas interfaces, consulte [como reproduzir um arquivo](how-to-play-a-file.md) e [responder a eventos](responding-to-events.md). O código a seguir mostra uma maneira de usar essas interfaces.


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



O código neste exemplo bloqueia a execução do programa até que a reprodução seja concluída, devido ao parâmetro infinito na chamada do método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) . No entanto, se algo der errado durante a reprodução, isso poderá fazer com que o programa pare de responder. Em um aplicativo real, use um loop de mensagem para aguardar a reprodução ser concluída. Também é recomendável que você forneça ao usuário uma maneira de interromper a reprodução.

Quando você terminar de usar o mecanismo de renderização, chame sempre o método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) . Esse método exclui o gráfico de filtro e libera todos os recursos mantidos pelo mecanismo de renderização.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Carregando e visualizando um projeto](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



