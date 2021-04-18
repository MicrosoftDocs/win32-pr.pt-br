---
title: Filtro de gravador ASF do WM (SDK do Windows Media Format 11)
description: Filtro de gravador ASF do WM
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- SDK do Windows Media Format, gravador ASF do WM
- DirectShow, gravador ASF do WM
- Filtros do QASF, gravador ASF do WM
- Gravador ASF do WM, sobre
- ASF (Advanced Systems Format), gravador ASF do WM
- ASF (formato de sistemas avançados), gravador ASF do WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105760105"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="22c66-109">Filtro de gravador ASF do WM (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="22c66-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="22c66-110">O filtro do gravador ASF do WM aceita um número variável de fluxos de entrada e cria um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="22c66-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="22c66-111">O filtro manipula toda a compactação e a multiplexação (embora o mecanismo de compactação possa ser ignorado).</span><span class="sxs-lookup"><span data-stu-id="22c66-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="22c66-112">Você pode usar o filtro do gravador ASF do WM em vários cenários, incluindo captura Audio-Video de vídeo digital (DV), recompactação de áudio e conversão de arquivos de mídia digital intercalados (AVI) ou MPEG para streaming de rede.</span><span class="sxs-lookup"><span data-stu-id="22c66-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="22c66-113">Esse filtro fornece a única maneira de criar arquivos de vídeo do Windows Media e áudio do Microsoft Windows no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="22c66-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="22c66-114">Para obter mais informações, consulte [criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="22c66-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="22c66-115">A tabela a seguir contém informações sobre o filtro de gravador ASF do WM, como as interfaces e os tipos de mídia aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="22c66-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c66-116">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="22c66-116">Filter interfaces</span></span>      | <span data-ttu-id="22c66-117">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="22c66-117">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="22c66-118">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="22c66-118">Input pin media types</span></span>  | <span data-ttu-id="22c66-119">Dependente do perfil.</span><span class="sxs-lookup"><span data-stu-id="22c66-119">Dependent on the profile.</span></span> <span data-ttu-id="22c66-120">Normalmente, tipos descompactados como \_ vídeo de áudio de MediaType ou MediaType \_ , embora tipos compactados possam ser aceitos se corresponderem ao perfil</span><span class="sxs-lookup"><span data-stu-id="22c66-120">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="22c66-121">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="22c66-121">Input pin interfaces</span></span>   | <span data-ttu-id="22c66-122">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (por meio de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="22c66-122">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="22c66-123">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="22c66-123">Output pin media types</span></span> | <span data-ttu-id="22c66-124">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="22c66-124">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="22c66-125">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="22c66-125">Output pin interfaces</span></span>  | <span data-ttu-id="22c66-126">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="22c66-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="22c66-127">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="22c66-127">Filter CLSID</span></span>           | <span data-ttu-id="22c66-128">\_WMASFWRITER CLSID</span><span class="sxs-lookup"><span data-stu-id="22c66-128">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="22c66-129">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="22c66-129">Property page CLSID</span></span>    | <span data-ttu-id="22c66-130">\_WMASFWRITERPROPERTIES CLSID</span><span class="sxs-lookup"><span data-stu-id="22c66-130">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="22c66-131">Executável</span><span class="sxs-lookup"><span data-stu-id="22c66-131">Executable</span></span>             | <span data-ttu-id="22c66-132">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="22c66-132">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="22c66-133">Núcleo</span><span class="sxs-lookup"><span data-stu-id="22c66-133">Merit</span></span>                  | <span data-ttu-id="22c66-134">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="22c66-134">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="22c66-135">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="22c66-135">Filter Category</span></span>        | <span data-ttu-id="22c66-136">Não especificado</span><span class="sxs-lookup"><span data-stu-id="22c66-136">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="22c66-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="22c66-137">Remarks</span></span>

<span data-ttu-id="22c66-138">O número de Pins de entrada no filtro depende do perfil que é passado para o filtro.</span><span class="sxs-lookup"><span data-stu-id="22c66-138">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="22c66-139">Um PIN do tipo de mídia apropriado é criado para cada fluxo definido no perfil.</span><span class="sxs-lookup"><span data-stu-id="22c66-139">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="22c66-140">Os Pins de entrada dão suporte a um método da interface **IAMStreamConfig** : **IAMStreamConfig:: GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="22c66-140">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="22c66-141">Todos os outros métodos retornam E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="22c66-141">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="22c66-142">Chame o método **GetFormat** para consultar o formato de compactação de destino do PIN, que é definido pelo perfil atual.</span><span class="sxs-lookup"><span data-stu-id="22c66-142">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="22c66-143">Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para definir o perfil.</span><span class="sxs-lookup"><span data-stu-id="22c66-143">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="22c66-144">A interface **IServiceProvider** do filtro permite que os aplicativos recuperem a interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , que é definida no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="22c66-144">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="22c66-145">A interface **IWMWriterAdvanced2** controla o desentrelaçamento de vídeo e será útil se a entrada for uma fonte [*entrelaçada*](wmformat-glossary.md) , como DV (Digital Video).</span><span class="sxs-lookup"><span data-stu-id="22c66-145">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="22c66-146">Use os métodos **GetInputSetting** e **SetInputSetting** para controlar o desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="22c66-146">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="22c66-147">Não é recomendável que os clientes usem qualquer um dos outros métodos nessa interface.</span><span class="sxs-lookup"><span data-stu-id="22c66-147">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="22c66-148">Essa interface só pode ser obtida depois que o filtro tiver sido adicionado ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="22c66-148">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="22c66-149">O exemplo a seguir mostra como consultar essa interface:</span><span class="sxs-lookup"><span data-stu-id="22c66-149">The following example shows how to query for this interface:</span></span>


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="22c66-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22c66-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c66-151">**Referência do QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="22c66-151">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
