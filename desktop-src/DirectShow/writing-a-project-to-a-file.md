---
description: Gravando um projeto em um arquivo
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Gravando um projeto em um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757831"
---
# <a name="writing-a-project-to-a-file"></a>Gravando um projeto em um arquivo

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Este artigo descreve como gravar um projeto de [serviços de edição do DirectShow](directshow-editing-services.md) em um arquivo. Primeiro, ele descreve como gravar um arquivo com o mecanismo de processamento básico. Em seguida, ele descreve a recompactação inteligente com o mecanismo de processamento inteligente.

Para obter uma visão geral de como os serviços de edição do DirectShow renderizam projetos, consulte [sobre os mecanismos de renderização](about-the-render-engines.md).

**Usando o mecanismo de renderização básico**

Comece criando o front-end do grafo, da seguinte maneira:

1.  Crie o mecanismo de renderização.
2.  Especifique a linha do tempo.
3.  Defina o intervalo de renderização. (Opcional)
4.  Crie o front-end do grafo.

O exemplo de código a seguir mostra essas etapas.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



Em seguida, adicione os filtros Multiplexador e gravação de arquivo ao grafo de filtro. A maneira mais fácil de fazer isso é com o [Construtor de grafo de captura](capture-graph-builder.md), um componente do DirectShow para criar grafos de captura. O construtor do grafo de captura expõe a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Execute as seguintes etapas:

1.  Crie uma instância do construtor de gráficos de captura.
2.  Obtenha um ponteiro para o grafo e passe-o para o construtor de gráficos.
3.  Especifique o nome e o tipo de mídia do arquivo de saída. Essa etapa também obtém um ponteiro para o filtro Mux, que é necessário posteriormente.

O exemplo de código a seguir mostra essas etapas.


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



Por fim, conecte os Pins de saída no front-end ao filtro Mux.

1.  Recupere o número de grupos.
2.  Para cada PIN, obtenha um ponteiro para o PIN.
3.  Opcionalmente, crie uma instância de um filtro de compactação para compactar o fluxo. O tipo de compressor dependerá do tipo de mídia do grupo. Você pode usar o [enumerador de dispositivo do sistema](system-device-enumerator.md) para enumerar os filtros de compactação disponíveis. Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).
4.  Opcionalmente, defina os parâmetros de compactação, como a taxa de quadro-chave. Esta etapa será discutida em detalhes posteriormente neste artigo.
5.  Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Esse método usa ponteiros para o pino, o filtro de compactação (se houver) e o multiplexador.

O exemplo de código a seguir mostra como conectar os Pins de saída.


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



Para definir os parâmetros de compactação (etapa 4, anteriormente), use a interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . Essa interface é exposta nos Pins de saída dos filtros de compactação. Enumere os Pins do filtro de compactação e consulte cada PIN de saída para **IAMVideoCompression**. (Para obter informações sobre como enumerar Pins, consulte [enumerando Pins](enumerating-pins.md).) Certifique-se de liberar todos os ponteiros de interface que você obteve durante esta etapa.

Depois de criar o grafo de filtro, chame o método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) no Gerenciador do grafo de filtro. À medida que o gráfico de filtro é executado, ele grava os dados em um arquivo. Use a notificação de eventos para aguardar a reprodução ser concluída. (Consulte [respondendo a eventos](responding-to-events.md).) Quando a reprodução for concluída, você deverá chamar explicitamente [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) para parar o grafo de filtro. Caso contrário, o arquivo não será gravado corretamente.

**Usando o mecanismo de processamento inteligente**

Para obter os benefícios da recompactação inteligente, use o mecanismo de processamento inteligente no lugar do mecanismo de renderização básico. As etapas na criação do grafo são quase iguais. A principal diferença é que a compactação é tratada no front-end do grafo, não na seção de gravação de arquivos.

> [!IMPORTANT]
> Não use o mecanismo de processamento inteligente para ler ou gravar arquivos de mídia do Windows.

 

Cada grupo de vídeos tem uma propriedade que especifica o formato de compactação para esse grupo. O formato de compactação deve corresponder exatamente ao formato descompactado do grupo em altura, largura, profundidade de bits e taxa de quadros. O mecanismo de processamento inteligente usa o formato de compactação quando constrói o grafo. Antes de definir o formato de compactação, certifique-se de definir o formato descompactado para esse grupo chamando [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md).

Para definir o formato de compactação de um grupo, chame o método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) . Esse método usa um ponteiro para uma estrutura [**SCompFmt0**](scompfmt0.md) . A estrutura **SCompFmt0** tem dois membros: **nFormatId**, que deve ser zero e **MediaType**, que é uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Inicialize a estrutura do **\_ \_ tipo de mídia am** com as informações de formato.

> [!Note]  
> Se você quiser que o projeto final tenha o mesmo formato que um dos seus arquivos de origem, você pode obter a \_ estrutura do tipo de mídia am \_ diretamente do arquivo de origem, usando o detector de mídia. Consulte [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md).

 

Converta a variável [**SCompFmt0**](scompfmt0.md) para um ponteiro do tipo **Long**, conforme mostrado no exemplo a seguir.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



O mecanismo de processamento inteligente procura automaticamente por um filtro de compactação compatível. Você também pode especificar um filtro de compactação para um grupo chamando [**ISmartRenderEngine:: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).

Para criar o grafo, use as mesmas etapas que foram descritas para o mecanismo de renderização básico na seção anterior. As únicas diferenças são as seguintes:

-   Use o mecanismo de processamento inteligente, não o mecanismo de renderização básico. O identificador de classe é CLSID \_ SmartRenderEngine.
-   Defina os parâmetros de compactação depois de criar o front-end, mas antes de renderizar os Pins de saída. Chame o método [**ISmartRenderEngine:: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) para obter um ponteiro para o filtro de compactação de um grupo. Em seguida, consulte a interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , conforme descrito anteriormente.
-   Quando você renderiza os Pins de saída, não é necessário inserir um filtro de compactação. O fluxo já está compactado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um projeto](rendering-a-project.md)
</dt> </dl>

 

 



