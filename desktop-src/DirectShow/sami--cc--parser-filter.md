---
description: Filtro do analisador SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtro do analisador SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77f0aa2d913b7f0295a078c8174ae483bb1cb62
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909674"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="5b2e4-103">Filtro do analisador SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="5b2e4-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="5b2e4-104">Analisa dados de legendas de arquivos de SAMI (intercâmbio de mídia acessível) sincronizados.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="5b2e4-105">SAMI é um formato de texto semelhante a HTML e é usado para codificar legendas baseadas em tempo.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="5b2e4-106">Esse filtro converte dados SAMI em um fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="5b2e4-107">Cada exemplo no fluxo contém uma entrada de legenda, juntamente com informações de formato.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="5b2e4-108">Os carimbos de data/hora nos exemplos são gerados a partir das informações de hora no arquivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="5b2e4-109">Esse filtro foi projetado para ser usado com o filtro de [processador de comandos de script interno](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5b2e4-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="5b2e4-110">O renderizador de comando de script interno recebe exemplos de texto e os envia para o aplicativo, na forma de notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="5b2e4-111">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-111">For more information, see the Remarks section.</span></span>



| <span data-ttu-id="5b2e4-112">Label</span><span class="sxs-lookup"><span data-stu-id="5b2e4-112">Label</span></span> | <span data-ttu-id="5b2e4-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5b2e4-113">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2e4-114">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="5b2e4-114">Filter Interfaces</span></span>                        | <span data-ttu-id="5b2e4-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="5b2e4-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="5b2e4-116">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5b2e4-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="5b2e4-117">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5b2e4-117">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="5b2e4-118">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5b2e4-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="5b2e4-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5b2e4-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="5b2e4-120">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="5b2e4-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="5b2e4-121">\_Texto de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="5b2e4-121">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="5b2e4-122">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="5b2e4-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="5b2e4-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5b2e4-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="5b2e4-124">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="5b2e4-124">Filter CLSID</span></span>                             | <span data-ttu-id="5b2e4-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="5b2e4-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="5b2e4-126">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="5b2e4-126">Property Page CLSID</span></span>                      | <span data-ttu-id="5b2e4-127">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="5b2e4-127">No property page</span></span>                                                                                         |
| <span data-ttu-id="5b2e4-128">Executável</span><span class="sxs-lookup"><span data-stu-id="5b2e4-128">Executable</span></span>                               | <span data-ttu-id="5b2e4-129">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="5b2e4-129">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="5b2e4-130">Núcleo</span><span class="sxs-lookup"><span data-stu-id="5b2e4-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="5b2e4-131">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="5b2e4-131">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="5b2e4-132">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="5b2e4-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5b2e4-133">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="5b2e4-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="5b2e4-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b2e4-134">Remarks</span></span>

<span data-ttu-id="5b2e4-135">Este é um arquivo SAMI simples:</span><span class="sxs-lookup"><span data-stu-id="5b2e4-135">The following is a simple SAMI file:</span></span>


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



<span data-ttu-id="5b2e4-136">A marca de **estilo** define duas configurações de idioma, inglês (. ENCC) e francês (. FRCC).</span><span class="sxs-lookup"><span data-stu-id="5b2e4-136">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="5b2e4-137">Ele também define dois estilos, \# normal e \# GREENTEXT.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-137">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="5b2e4-138">Cada marca de **sincronização** define a hora de início de uma legenda, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-138">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="5b2e4-139">As marcas **P** contêm o texto de legenda, enquanto o atributo de **classe** especifica a configuração de idioma à qual a legenda se aplica.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-139">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="5b2e4-140">Para cada idioma e estilo, o filtro cria um fluxo lógico.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-140">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="5b2e4-141">A qualquer momento, exatamente uma transmissão de fluxo de idioma e um estilo são habilitados.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-141">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="5b2e4-142">Quando o filtro gera um exemplo, ele seleciona a legenda para o idioma atual e aplica o estilo atual.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-142">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="5b2e4-143">Por padrão, o primeiro idioma e estilo declarados no arquivo são habilitados.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-143">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="5b2e4-144">Um aplicativo pode usar o método [**IAMStreamSelect:: Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) para habilitar um fluxo diferente.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-144">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="5b2e4-145">Com as configurações padrão, a primeira legenda no arquivo de exemplo produz a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="5b2e4-145">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="5b2e4-146">Se a saída for para o processador de comandos de script interno, esse filtro enviará uma notificação de evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="5b2e4-146">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="5b2e4-147">O segundo parâmetro de evento é um BSTR com o texto de legenda.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-147">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="5b2e4-148">O aplicativo pode recuperar o evento e exibir a legenda.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-148">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="5b2e4-149">O exemplo a seguir mostra como renderizar um arquivo SAMI, recuperar informações de fluxo, habilitar fluxos e exibir texto de legenda.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-149">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="5b2e4-150">O exemplo supõe que o arquivo SAMI anterior seja salvo como C: \\ Sami \_ test \_ File. Sami.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-150">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="5b2e4-151">Para resumir, este exemplo usou índices de fluxo embutidos em código quando chama o método **IAMStreamSelect:: Enable** .</span><span class="sxs-lookup"><span data-stu-id="5b2e4-151">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="5b2e4-152">Ele também executa a verificação mínima de erros.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-152">It also performs minimal error checking.</span></span>


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



<span data-ttu-id="5b2e4-153">Esse filtro usa a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) para extrair amostras do filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-153">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="5b2e4-154">Portanto, ele não dá suporte à interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) em seu pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b2e4-154">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b2e4-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b2e4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b2e4-156">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="5b2e4-156">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



