---
description: Como reproduzir um arquivo
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Como reproduzir um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370299"
---
# <a name="how-to-play-a-file"></a>Como reproduzir um arquivo

Este artigo destina-se a dar o tipo de programação do DirectShow. Ele apresenta um aplicativo de console simples que reproduz um arquivo de áudio ou de vídeo. O programa tem apenas algumas linhas, mas demonstra algumas das eficiências da programação do DirectShow.

Como descreve o artigo [introdução à programação de aplicativo do DirectShow](introduction-to-directshow-application-programming.md) , um aplicativo do DirectShow sempre executa as mesmas etapas básicas:

1.  Crie uma instância do [Gerenciador de gráfico de filtro](filter-graph-manager.md).
2.  Use o Gerenciador de gráfico de filtro para criar um grafo de filtro.
3.  Execute o grafo, fazendo com que os dados passem pelos filtros.

Para compilar e vincular o código neste tópico, inclua o arquivo de cabeçalho DShow. h e vincule ao arquivo de biblioteca estática strmiids. lib. Para obter mais informações, consulte [criando aplicativos do DirectShow](setting-up-the-build-environment.md).

Comece chamando [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Para simplificar as coisas, este exemplo ignora o valor de retorno, mas você sempre deve verificar o valor **HRESULT** de qualquer chamada de método.

Em seguida, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o Gerenciador de gráfico de filtro:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Como mostrado, o identificador de classe (CLSID) é CLSID \_ FilterGraph. O Gerenciador de gráfico de filtro é fornecido por uma DLL em processo, portanto, o contexto de execução é o **\_ \_ servidor CLSCTX InProc**. O DirectShow dá suporte ao modelo de Threading livre, de modo que você também pode chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) com o sinalizador de **\_ vários threads de coinit** .

A chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retorna a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , que basicamente contém métodos para criar o grafo de filtro. Duas outras interfaces são necessárias para este exemplo:

-   Streaming de controles [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) . Ele contém métodos para parar e iniciar o grafo.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) tem métodos para obter eventos do Gerenciador de gráficos de filtro. Neste exemplo, a interface é usada para aguardar a conclusão da reprodução.

Ambas as interfaces são expostas pelo Gerenciador do grafo de filtro. Use o ponteiro [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) retornado para consultá-los:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Agora você pode criar o gráfico de filtro. Para a reprodução de arquivos, isso é feito por uma única chamada de método:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



O método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) cria um gráfico de filtro que pode reproduzir o arquivo especificado. O primeiro parâmetro é o nome do arquivo, representado como uma cadeia de caracteres de caractere largo (2 bytes). O segundo parâmetro é reservado e deve ser igual a **NULL**.

Esse método pode falhar se o arquivo especificado não existir ou o formato de arquivo não for reconhecido. Supondo que o método tenha sucesso, no entanto, o gráfico de filtro agora está pronto para reprodução. Para executar o grafo, chame o método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :


```C++
hr = pControl->Run();
```



Quando o grafo de filtro é executado, os dados passam pelos filtros e são renderizados como vídeo e áudio. A reprodução ocorre em um thread separado. Você pode aguardar a reprodução ser concluída chamando o método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Esse método é bloqueado até que o arquivo seja executado ou até que o intervalo de tempo limite especificado decorra. O valor infinito significa que o aplicativo é bloqueado indefinidamente até que o arquivo seja executado. Para obter um exemplo mais realista de manipulação de eventos, consulte [respondendo a eventos](responding-to-events.md).

Quando o aplicativo for concluído, libere os ponteiros de interface e feche a biblioteca COM:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Código de exemplo

Este é o código completo do exemplo descrito neste artigo:


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

[Tarefas básicas do DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 
