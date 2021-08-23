---
description: Visualizando um Project
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Visualizando um Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159303c175c459b4d5d93ba4c7b4b2622caddac2a35d3474a3059ac703d62645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583548"
---
# <a name="previewing-a-project"></a>Visualizando um Project

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Para visualizar um projeto, primeiro chame **CoCreateInstance** para criar uma instância do mecanismo de renderização básico. O identificador de classe é CLSID \_ RenderEngine. Em seguida, chame o método [**IRenderEngine:: Settimelineobject**](irenderengine-settimelineobject.md) para especificar a linha do tempo que você está renderizando.

Na primeira vez que você visualizar a linha do tempo, execute as seguintes chamadas na ordem listada:

1.  Chame [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md) para especificar qual parte da linha do tempo será visualizada. (Opcional)
2.  Chame [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo.
3.  Chame [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md). Esse método conecta cada pino de saída a um processador de vídeo ou processador de áudio, concluindo o grafo.

O exemplo de código a seguir mostra estas etapas:


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Agora, execute o gráfico de filtro. primeiro, chame o método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) para recuperar um ponteiro para o filtro Graph interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do gerenciador. em seguida, consulte o filtro Graph Manager para a interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), conforme mostrado no código a seguir:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



Use o filtro Graph interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) do gerenciador para aguardar a conclusão da visualização. você também pode buscar o grafo usando o filtro Graph interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do gerenciador, assim como faria com um grafo de reprodução de arquivo.

Para visualizar o projeto novamente, busque o grafo de volta para o tempo zero e chame a **execução** novamente. Se você alterar o conteúdo da linha do tempo, faça o seguinte:

1.  Chame **SetRenderRange**. (Opcional)
2.  Chame **ConnectFrontEnd**.
3.  Se o método **ConnectFrontEnd** retornar S \_ \_ OUTPUTRESET de aviso, chame **RenderOutputPins**. (Se **ConnectFrontEnd** retornar S \_ OK, você pode ignorar esta etapa.)
4.  Busque o grafo de volta para o tempo zero.
5.  Execute o grafo.

O exemplo a seguir mostra estas etapas:


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



Para obter um exemplo completo que carrega e visualiza um arquivo de projeto, consulte [carregando e visualizando um Project](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando projetos de edição de vídeo](managing-video-editing-projects.md)
</dt> <dt>

[Renderizando um Project](rendering-a-project.md)
</dt> </dl>

 

 



