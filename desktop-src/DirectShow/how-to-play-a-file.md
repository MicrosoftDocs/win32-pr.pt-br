---
description: Como reproduzir um arquivo
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Como reproduzir um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d20a021ec5053746c279598d08117c6b25a5fe6a52946fed56f19eda3cafe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401144"
---
# <a name="how-to-play-a-file"></a>Como reproduzir um arquivo

Este artigo destina-se a dar a você o tipo de DirectShow programação. Ele apresenta um aplicativo de console simples que reproduz um arquivo de áudio ou vídeo. O programa tem apenas algumas linhas de comprimento, mas demonstra parte do poder da DirectShow programação.

Como descreve o artigo [Introdução DirectShow programação](introduction-to-directshow-application-programming.md) de aplicativos, um DirectShow aplicativo sempre executa as mesmas etapas básicas:

1.  Crie uma instância do [Gerenciador Graph Filtro](filter-graph-manager.md).
2.  Use o Gerenciador de Graph filtro para criar um grafo de filtro.
3.  Execute o grafo, fazendo com que os dados se movam pelos filtros.

Para compilar e vincular o código neste tópico, inclua o arquivo de título Dshow.h e o link para o arquivo de biblioteca estática strmiids.lib. Para obter mais informações, consulte [Building DirectShow Applications](setting-up-the-build-environment.md).

Comece chamando [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca COM:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Para manter as coisas simples, este exemplo ignora o valor de retorno, mas você sempre deve verificar o valor **HRESULT** de qualquer chamada de método.

Em seguida, [**chame CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o Gerenciador Graph Filter:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Conforme mostrado, o CLSID (identificador de classe) é ClSID \_ FilterGraph. O Gerenciador Graph Filtro é fornecido por uma DLL em processo, portanto, o contexto de execução é **CLSCTX \_ INPROC \_ SERVER**. DirectShow dá suporte ao modelo de threading livre, portanto, você também pode chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) com o sinalizador **COINIT \_ MULTITHREADED.**

A chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retorna a interface [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) que contém principalmente métodos para criar o grafo de filtro. Duas outras interfaces são necessárias para este exemplo:

-   [**IMediaControl controla**](/windows/desktop/api/Control/nn-control-imediacontrol) o streaming. Ele contém métodos para parar e iniciar o grafo.
-   [**O IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) tem métodos para obter eventos do Gerenciador de Graph Filtro. Neste exemplo, a interface é usada para aguardar a conclusão da reprodução.

Ambas as interfaces são expostas pelo Gerenciador de Graph Filtro. Use o ponteiro [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) retornado para consulta-los:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Agora você pode criar o grafo de filtro. Para reprodução de arquivo, isso é feito por uma única chamada de método:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



O [**método IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) cria um grafo de filtro que pode reproduzir o arquivo especificado. O primeiro parâmetro é o nome do arquivo, representado como uma cadeia de caracteres largo (2 byte). O segundo parâmetro é reservado e deve ser igual a **NULL.**

Esse método poderá falhar se o arquivo especificado não existir ou se o formato de arquivo não for reconhecido. Supondo que o método seja bem-sucedido, no entanto, o grafo de filtro agora está pronto para reprodução. Para executar o grafo, chame o [**método IMediaControl::Run:**](/windows/desktop/api/Control/nf-control-imediacontrol-run)


```C++
hr = pControl->Run();
```



Quando o grafo de filtro é executado, os dados se movem pelos filtros e são renderizados como vídeo e áudio. A reprodução ocorre em um thread separado. Você pode aguardar a conclusão da reprodução chamando o [**método IMediaEvent::WaitForCompletion:**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion)


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Esse método bloqueia até que o arquivo seja terminado de ser a reprodução ou até que o intervalo de tempo-out especificado seja desastrado. O valor INFINITE significa que o aplicativo é bloco indefinidamente até que o arquivo seja terminado de ser a reprodução. Para obter um exemplo mais realista de manipulação de eventos, consulte [Respondendo a eventos](responding-to-events.md).

Quando o aplicativo for concluído, libere os ponteiros de interface e feche a biblioteca COM:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Código de exemplo

Este é o código completo para o exemplo descrito neste artigo:


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas DirectShow básicas](basic-directshow-tasks.md)
</dt> </dl>

 

 
