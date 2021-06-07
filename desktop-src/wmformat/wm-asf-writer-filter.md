---
title: Filtro do Wm ASF Writer (Windows Media Format SDK 11)
description: Saiba mais sobre o filtro Wm ASF Writer.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, Wm ASF Writer
- DirectShow, Wm ASF Writer
- Filtros QASF, Wm ASF Writer
- WM ASF Writer,about
- AsF (Advanced Systems Format), WM ASF Writer
- ASF (Formato de Sistemas Avançados), Wm ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444697"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="a460e-109">Filtro do Wm ASF Writer (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="a460e-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a460e-110">O filtro Wm ASF Writer aceita um número variável de fluxos de entrada e cria um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="a460e-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="a460e-111">O filtro lida com toda a compactação e multiplexação (embora o mecanismo de compactação possa ser ignorado).</span><span class="sxs-lookup"><span data-stu-id="a460e-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="a460e-112">Você pode usar o filtro gravador WM ASF em vários cenários, incluindo captura de DV (vídeo digital), re Audio-Video compactação de áudio e conversão de arquivos de mídia digital INTERcalados (AVI) ou MPEG para streaming de rede.</span><span class="sxs-lookup"><span data-stu-id="a460e-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="a460e-113">Esse filtro fornece a única maneira de criar arquivos de Áudio de Mídia do Microsoft Windows e vídeo de mídia do Windows no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a460e-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="a460e-114">Para obter mais informações, consulte [Criando arquivos ASF no DirectShow.](creating-asf-files-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="a460e-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="a460e-115">A tabela a seguir contém informações sobre o filtro Wm ASF Writer, como as interfaces e tipos de mídia aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="a460e-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="a460e-116">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="a460e-116">Filter Information</span></span>                       |  <span data-ttu-id="a460e-117">Tipos</span><span class="sxs-lookup"><span data-stu-id="a460e-117">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a460e-118">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="a460e-118">Filter interfaces</span></span>      | <span data-ttu-id="a460e-119">**IAMFilterMiscFlags,** **IBaseFilter,** **IConfigAsfWriter,** **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="a460e-119">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="a460e-120">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a460e-120">Input pin media types</span></span>  | <span data-ttu-id="a460e-121">Dependendo do perfil.</span><span class="sxs-lookup"><span data-stu-id="a460e-121">Dependent on the profile.</span></span> <span data-ttu-id="a460e-122">Normalmente, tipos descompactados, como Áudio MEDIATYPE ou Vídeo MEDIATYPE, embora os tipos compactados possam ser aceitos se corresponderem \_ \_ ao perfil</span><span class="sxs-lookup"><span data-stu-id="a460e-122">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="a460e-123">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a460e-123">Input pin interfaces</span></span>   | <span data-ttu-id="a460e-124">**IPin,** **IMemInputPin,** **IAMStreamConfig,** **IServiceProvider,** **IAMWMBufferPass,** **IWMStreamConfig2** (por **meio de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="a460e-124">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="a460e-125">Tipos de mídia de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a460e-125">Output pin media types</span></span> | <span data-ttu-id="a460e-126">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="a460e-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="a460e-127">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a460e-127">Output pin interfaces</span></span>  | <span data-ttu-id="a460e-128">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="a460e-128">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="a460e-129">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="a460e-129">Filter CLSID</span></span>           | <span data-ttu-id="a460e-130">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="a460e-130">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="a460e-131">CLSID da página de propriedades</span><span class="sxs-lookup"><span data-stu-id="a460e-131">Property page CLSID</span></span>    | <span data-ttu-id="a460e-132">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="a460e-132">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="a460e-133">Executável</span><span class="sxs-lookup"><span data-stu-id="a460e-133">Executable</span></span>             | <span data-ttu-id="a460e-134">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="a460e-134">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="a460e-135">Mérito</span><span class="sxs-lookup"><span data-stu-id="a460e-135">Merit</span></span>                  | <span data-ttu-id="a460e-136">NÃO USE O NÃO \_ \_ USO \_ DE LIMITED</span><span class="sxs-lookup"><span data-stu-id="a460e-136">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="a460e-137">Categoria de filtro</span><span class="sxs-lookup"><span data-stu-id="a460e-137">Filter Category</span></span>        | <span data-ttu-id="a460e-138">Não especificado</span><span class="sxs-lookup"><span data-stu-id="a460e-138">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="a460e-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="a460e-139">Remarks</span></span>

<span data-ttu-id="a460e-140">O número de pinos de entrada no filtro depende do perfil passado para o filtro.</span><span class="sxs-lookup"><span data-stu-id="a460e-140">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="a460e-141">Um pino do tipo de mídia apropriado é criado para cada fluxo definido no perfil.</span><span class="sxs-lookup"><span data-stu-id="a460e-141">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="a460e-142">Os pinos de entrada suportam um método da interface **IAMStreamConfig:** **IAMStreamConfig::GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="a460e-142">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="a460e-143">Todos os outros métodos retornam E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a460e-143">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="a460e-144">Chame o **método GetFormat** para consultar o formato de compactação de destino do pino, que é definido pelo perfil atual.</span><span class="sxs-lookup"><span data-stu-id="a460e-144">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="a460e-145">Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para definir o perfil.</span><span class="sxs-lookup"><span data-stu-id="a460e-145">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="a460e-146">A interface **IServiceProvider** do filtro permite que os aplicativos recuperem a interface [**IWMWriterAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) que é definida no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a460e-146">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="a460e-147">A interface **IWMWriterAdvanced2** controla [*a*](wmformat-glossary.md) desintervalação de vídeo e é útil se a entrada for uma fonte entrelaçada, como DV (vídeo digital).</span><span class="sxs-lookup"><span data-stu-id="a460e-147">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="a460e-148">Use os **métodos GetInputSetting** **e SetInputSetting** para controlar a desintercalação.</span><span class="sxs-lookup"><span data-stu-id="a460e-148">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="a460e-149">Não é recomendável que os clientes usem qualquer um dos outros métodos nessa interface.</span><span class="sxs-lookup"><span data-stu-id="a460e-149">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="a460e-150">Essa interface só poderá ser obtida depois que o filtro tiver sido adicionado ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a460e-150">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="a460e-151">O exemplo a seguir mostra como consultar essa interface:</span><span class="sxs-lookup"><span data-stu-id="a460e-151">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a460e-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a460e-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a460e-153">**Referência de QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="a460e-153">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
