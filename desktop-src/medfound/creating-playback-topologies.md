---
description: Este tópico descreve como criar uma topologia para reprodução de áudio ou vídeo.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Criando topologias de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763281"
---
# <a name="creating-playback-topologies"></a>Criando topologias de reprodução

Este tópico descreve como criar uma topologia para reprodução de áudio ou vídeo. Para a reprodução básica, você pode criar uma topologia parcial, na qual os nós de origem estão conectados diretamente aos nós de saída. Você não precisa inserir nenhum nó para as transformações intermediárias, como decodificadores ou conversores de cor. A sessão de mídia usará o carregador de topologia para resolver a topologia e o carregador de topologia irá inserir as transformações necessárias.

-   [Criando a topologia](#creating-the-topology)
-   [Conectando fluxos a coletores de mídia](#connecting-streams-to-media-sinks)
-   [Criando o coletor de mídia](#creating-the-media-sink)
-   [Próximas etapas](#next-steps)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-the-topology"></a>Criando a topologia

Aqui estão as etapas gerais para criar uma topologia de reprodução parcial de uma fonte de mídia:

1.  Crie a origem da mídia. Na maioria dos casos, você usará o resolvedor de origem para criar a origem da mídia. Para obter mais informações, consulte [resolvedor de origem](source-resolver.md).
2.  Obtenha o descritor de apresentação da fonte de mídia.
3.  Crie uma topologia vazia.
4.  Use o descritor de apresentação para enumerar os descritores de fluxo. Para cada descritor de fluxo:
    1.  Obtenha o tipo de mídia principal do fluxo, como áudio ou vídeo.
    2.  Verifique se o fluxo está selecionado no momento. (Opcionalmente, você pode selecionar ou desmarcar um fluxo, com base no tipo de mídia.)
    3.  Se o fluxo for selecionado, crie um objeto de ativação para o coletor de mídia, com base no tipo de mídia do fluxo.
    4.  Adicione um nó de origem para o fluxo e um nó de saída para o coletor de mídia.
    5.  Conecte o nó de origem ao nó de saída.

Para facilitar o acompanhamento desse processo, o código de exemplo neste tópico é organizado em várias funções. A função de nível superior é denominada `CreatePlaybackTopology` . São necessários três parâmetros:

-   Um ponteiro para uma interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.
-   Um ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação. Obtenha esse ponteiro chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Para fontes com várias apresentações, os descritores de apresentação das apresentações subsequentes são entregues no evento [MENewPresentation](menewpresentation.md) .
-   Um identificador para uma janela de aplicativo. Se a fonte tiver um fluxo de vídeo, o vídeo será exibido nessa janela.

A função retorna um ponteiro para uma topologia de reprodução parcial no parâmetro *ppTopology* .


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



Esta função realiza as seguintes etapas:

1.  Chame [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) para criar a topologia. Inicialmente, a topologia não contém nenhum nó.
2.  Chame [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obter o número de fluxos na apresentação.
3.  Para cada fluxo, chame a função definida pelo aplicativo `AddBranchToPartialTopology` para uma ramificação na topologia. Essa função é mostrada na próxima seção.

## <a name="connecting-streams-to-media-sinks"></a>Conectando fluxos a coletores de mídia

Para cada fluxo selecionado, adicione um nó de origem e um nó de saída e conecte os dois nós. O nó de origem representa o fluxo. O nó de saída representa o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) ou o [renderizador de áudio de streaming](streaming-audio-renderer.md) (SAR).

A `AddBranchToPartialTopology` função, mostrada no próximo exemplo, usa os seguintes parâmetros:

-   Um ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia.
-   Um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.
-   Um ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação.
-   O índice de base zero do fluxo.
-   Um identificador para a janela de vídeo. Esse identificador é usado apenas para o fluxo de vídeo.


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



A função faz o seguinte:

1.  Chama [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passa o índice de fluxo. Esse método retorna um ponteiro para o descritor de fluxo para esse fluxo, juntamente com um valor booliano que indica se o fluxo está selecionado.
2.  Se o fluxo não estiver selecionado, a função será encerrada e retornará S \_ OK, pois o aplicativo não precisa criar uma ramificação de topologia para um fluxo, a menos que esteja selecionado.
3.  Se o fluxo for selecionado, a função concluirá a ramificação de topologia da seguinte maneira:
    1.  Cria um objeto de ativação para o coletor, chamando a função CreateMediaSinkActivate definida pelo aplicativo. Essa função é mostrada na próxima seção.
    2.  Adiciona um nó de origem à topologia. O código para essa etapa é mostrado no tópico [criando nós de origem](creating-source-nodes.md).
    3.  Adiciona um nó de saída à topologia. O código para essa etapa é mostrado no tópico [criando nós de saída](creating-output-nodes.md).
    4.  Conecta os dois nós chamando [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) no nó de origem. Conectando os nós, o aplicativo indica que o nó upstream deve entregar dados ao nó downstream. Um nó de origem tem uma saída e um nó de saída tem uma entrada, portanto os dois índices de fluxo são zero.

Aplicativos mais avançados podem selecionar ou desmarcar fluxos, em vez de usar a configuração padrão da origem. Uma origem pode ter vários fluxos e qualquer um deles pode ser selecionado por padrão. O descritor de apresentação da origem de mídia tem um conjunto padrão de seleções de fluxo. Em um arquivo de vídeo simples com um fluxo de áudio único e fluxo de vídeo, a origem da mídia geralmente seleciona os dois fluxos por padrão. No entanto, um arquivo pode ter vários fluxos de áudio para diferentes idiomas ou vários fluxos de vídeo codificados em diferentes taxas de bits. Nesse caso, alguns dos fluxos serão desmarcados por padrão. O aplicativo pode alterar a seleção chamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) no descritor de apresentação.

## <a name="creating-the-media-sink"></a>Criando o coletor de mídia

A função Next cria um objeto de ativação para o coletor de mídia EVR ou SAR.


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



Esta função realiza as seguintes etapas:

1.  Chama [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo. Esse método retorna um ponteiro de interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

2.  Chama [**IMFMediaTypeHandler:: Getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Esse método retorna o GUID de tipo principal para o fluxo.

3.  Se o tipo de fluxo for áudio, a função chamará [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) para criar o objeto de ativação do processador de áudio. Se o tipo de fluxo for vídeo, a função chamará [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar o objeto de ativação do processador de vídeo. Ambas as funções retornam um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Esse ponteiro é usado para inicializar o nó de saída para o coletor, conforme mostrado anteriormente.

Para qualquer outro tipo de fluxo, este exemplo retorna um código de erro. Como alternativa, você poderia simplesmente anular a seleção do fluxo.

## <a name="next-steps"></a>Próximas etapas

Para reproduzir um arquivo de mídia de cada vez, enfileirar a topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). A sessão de mídia usará o carregador de topologia para resolver a topologia. Para obter um exemplo completo, consulte [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como reproduzir arquivos de mídia desprotegidos](how-to-play-unprotected-media-files.md)
</dt> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Topologias](topologies.md)
</dt> </dl>

 

 



