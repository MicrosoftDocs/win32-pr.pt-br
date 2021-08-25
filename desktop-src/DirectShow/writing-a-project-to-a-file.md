---
description: Escrevendo um Project em um arquivo
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Escrevendo um Project em um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efea1d0949c419ba6f595e7a381b689d8a8ce69836609d328b555ee695743b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051366"
---
# <a name="writing-a-project-to-a-file"></a>Escrevendo um Project em um arquivo

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Este artigo descreve como gravar um projeto [DirectShow Editing Services](directshow-editing-services.md) em um arquivo. Primeiro, ele descreve como gravar um arquivo com o mecanismo de renderização básico. Em seguida, ele descreve a recompactação inteligente com o mecanismo de renderização inteligente.

Para ter uma visão geral de como DirectShow Serviços de Edição renderiza projetos, consulte [Sobre os Mecanismos de Renderização](about-the-render-engines.md).

**Usando o mecanismo de renderização básico**

Comece criando o front-end do grafo, da seguinte forma:

1.  Crie o mecanismo de renderização.
2.  Especifique a linha do tempo.
3.  Definir o intervalo de renderização. (Opcional)
4.  Crie o front-end do grafo.

O exemplo de código a seguir mostra estas etapas.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



Em seguida, adicione filtros multiplexador e de escrita de arquivo ao grafo de filtro. A maneira mais fácil de fazer isso é com o [Capture Graph Builder](capture-graph-builder.md), um componente DirectShow para a criação de grafos de captura. O construtor de grafo de captura expõe a interface [**ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) Execute as seguintes etapas:

1.  Crie uma instância do construtor de grafo de captura.
2.  Obtenha um ponteiro para o grafo e passe-o para o construtor de grafo.
3.  Especifique o nome e o tipo de mídia do arquivo de saída. Essa etapa também obtém um ponteiro para o filtro mux, que é necessário posteriormente.

O exemplo de código a seguir mostra estas etapas.


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



Por fim, conecte os pinos de saída no front-end ao filtro mux.

1.  Recupere o número de grupos.
2.  Para cada pino, obtenha um ponteiro para o pino.
3.  Opcionalmente, crie uma instância de um filtro de compactação para compactar o fluxo. O tipo de group dependerá do tipo de mídia do grupo. Você pode usar o [Enumerador de Dispositivo do Sistema](system-device-enumerator.md) para enumerar os filtros de compactação disponíveis. Para obter mais informações, consulte [Enumerando dispositivos e filtros.](enumerating-devices-and-filters.md)
4.  Opcionalmente, de definir parâmetros de compactação, como a taxa de quadros-chave. Esta etapa será discutida em detalhes posteriormente neste artigo.
5.  Chame [**ICaptureGraphBuilder2::RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Esse método leva ponteiros para o pino, o filtro de compactação (se algum) e o multiplexador.

O exemplo de código a seguir mostra como conectar os pinos de saída.


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



Para definir parâmetros de compactação (etapa 4, anteriormente), use a interface [**IAMVideoCompression.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) Essa interface é exposta nos pinos de saída dos filtros de compactação. Enumerar os pinos do filtro de compactação e consultar cada pino de saída para **IAMVideoCompression**. (Para obter informações sobre como enumerar pinos, consulte [Enumerando pinos](enumerating-pins.md).) Certifique-se de liberar todos os ponteiros de interface obtidos durante esta etapa.

Depois de criar o grafo de filtro, chame o [**método IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) no gerenciador de grafo de filtro. À medida que o grafo de filtro é executado, ele grava os dados em um arquivo. Use a notificação de evento para aguardar a conclusão da reprodução. (Consulte [Respondendo a eventos](responding-to-events.md).) Quando a reprodução for final, você deverá chamar [**explicitamente IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) para interromper o grafo de filtro. Caso contrário, o arquivo não será gravado corretamente.

**Usando o Mecanismo de Renderização Inteligente**

Para obter os benefícios da recompactação inteligente, use o mecanismo de renderização inteligente no lugar do mecanismo de renderização básico. As etapas na criação do grafo são quase as mesmas. A principal diferença é que a compactação é tratada no front-end do grafo, não na seção de escrita de arquivo.

> [!IMPORTANT]
> Não use o mecanismo de renderização inteligente para ler ou gravar Windows mídia.

 

Cada grupo de vídeos tem uma propriedade que especifica o formato de compactação para esse grupo. O formato de compactação deve corresponder exatamente ao formato descompactado do grupo em altura, largura, profundidade de bits e taxa de quadros. O mecanismo de renderização inteligente usa o formato de compactação quando constrói o grafo. Antes de definir o formato de compactação, certifique-se de definir o formato descompactado para esse grupo chamando [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).

Para definir o formato de compactação de um grupo, chame o [**método IAMTimelineGroup::SetSmartRecompressFormat.**](iamtimelinegroup-setsmartrecompressformat.md) Esse método leva um ponteiro para uma [**estrutura SCompFmt0.**](scompfmt0.md) A **estrutura SCompFmt0** tem dois membros: **nFormatId**, que deve ser zero, e **MediaType**, que é uma estrutura [**AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Inicialize a **estrutura AM \_ MEDIA \_ TYPE** com as informações de formato.

> [!Note]  
> Se você quiser que o projeto final tenha o mesmo formato que um de seus arquivos de origem, poderá obter a estrutura AM MEDIA TYPE diretamente do arquivo de origem, usando o \_ \_ detector de mídia. Consulte [**IMediaDet::get \_ StreamMediaType**](imediadet-get-streammediatype.md).

 

Caste [**a variável SCompFmt0**](scompfmt0.md) em um ponteiro do **tipo long**, conforme mostrado no exemplo a seguir.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



O mecanismo de renderização inteligente pesquisa automaticamente um filtro de compactação compatível. Você também pode especificar um filtro de compactação para um grupo chamando [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).

Para criar o grafo, use as mesmas etapas descritas para o Mecanismo de Renderização Básico na seção anterior. As únicas diferenças são as seguintes:

-   Use o mecanismo de renderização inteligente, não o mecanismo de renderização básico. O identificador de classe é CLSID \_ SmartRenderEngine.
-   Definir parâmetros de compactação depois de criar o front-end, mas antes de renderizar os pinos de saída. Chame o [**método ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) para obter um ponteiro para o filtro de compactação de um grupo. Em seguida, consulte a interface [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) conforme descrito anteriormente.
-   Quando você renderiza os pinos de saída, não é necessário inserir um filtro de compactação. O fluxo já está compactado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizar um Project](rendering-a-project.md)
</dt> </dl>

 

 



