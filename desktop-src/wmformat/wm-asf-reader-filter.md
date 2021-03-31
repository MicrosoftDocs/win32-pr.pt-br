---
title: Filtro de leitor ASF do WM (SDK do Windows Media Format 11)
description: Filtro de leitor ASF do WM
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- SDK do Windows Media Format, leitor de ASF do WM
- DirectShow, leitor de ASF do WM
- Filtros de QASF, leitor de ASF do WM
- Leitor ASF do WM
- ASF (Advanced Systems Format), leitor ASF do WM
- ASF (formato de sistemas avançados), leitor ASF do WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644120"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="9db85-109">Filtro de leitor ASF do WM (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="9db85-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="9db85-110">Ao receber o nome de um arquivo ASF ou uma URL, o leitor ASF do WM lê o conteúdo compactado, analisa os fluxos e expõe um pino de saída para cada um.</span><span class="sxs-lookup"><span data-stu-id="9db85-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="9db85-111">Esse filtro conecta o downstream ao vídeo do Windows Media Audio ou Windows Media DMOs, que faz a descompactação.</span><span class="sxs-lookup"><span data-stu-id="9db85-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="9db85-112">A busca será suportada se o arquivo ASF for pesquisável.</span><span class="sxs-lookup"><span data-stu-id="9db85-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="9db85-113">O leitor de ASF do WM aplica carimbos de data/hora aos exemplos de mídia com base no carimbo de data/hora no arquivo ASF, mas não modifica os carimbos de data/hora de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="9db85-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="9db85-114">Internamente, o filtro usa o objeto leitor de formato de mídia do Windows para ler o conteúdo baseado no Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9db85-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="9db85-115">No SDK do DirectX, esse filtro não é o filtro de origem padrão para arquivos ASF, de modo que com esse SDK você não pode usar esse filtro com o método **RenderFile** ; Você deve adicioná-lo explicitamente ao grafo de filtro usando seu CLSID (identificador de classe).</span><span class="sxs-lookup"><span data-stu-id="9db85-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="9db85-116">Esse comportamento é diferente com o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="9db85-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="9db85-117">Quando você instala as bibliotecas de tempo de execução do SDK do Windows Media Format, o leitor ASF do WM é registrado como filtro padrão para arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="9db85-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="9db85-118">A tabela a seguir contém informações sobre o filtro de leitor ASF do WM, como as interfaces e os tipos de mídia aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="9db85-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db85-119">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="9db85-119">Filter interfaces</span></span>      | <span data-ttu-id="9db85-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (parcialmente implementado.</span><span class="sxs-lookup"><span data-stu-id="9db85-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="9db85-121">Consulte comentários.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (por meio de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="9db85-121">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="9db85-122">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9db85-122">Input pin media types</span></span>  | <span data-ttu-id="9db85-123">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9db85-123">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="9db85-124">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9db85-124">Input pin interfaces</span></span>   | <span data-ttu-id="9db85-125">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9db85-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="9db85-126">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="9db85-126">Output pin media types</span></span> | <span data-ttu-id="9db85-127">\_Vídeo de MediaType, \_ áudio de MEDIATYPE, MediaType \_ ScriptCommand, \_ FileTransfer de MediaType</span><span class="sxs-lookup"><span data-stu-id="9db85-127">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="9db85-128">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="9db85-128">Format type</span></span>            | <span data-ttu-id="9db85-129">**VIDEOINFOHEADER2** se o conteúdo estiver [*entrelaçado*](wmformat-glossary.md), caso contrário **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="9db85-129">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="9db85-130">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="9db85-130">Output pin interfaces</span></span>  | <span data-ttu-id="9db85-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (por meio de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="9db85-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="9db85-132">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="9db85-132">Filter CLSID</span></span>           | <span data-ttu-id="9db85-133">\_WMASFREADER CLSID</span><span class="sxs-lookup"><span data-stu-id="9db85-133">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="9db85-134">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="9db85-134">Property Page CLSID</span></span>    | <span data-ttu-id="9db85-135">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="9db85-135">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="9db85-136">Executável</span><span class="sxs-lookup"><span data-stu-id="9db85-136">Executable</span></span>             | <span data-ttu-id="9db85-137">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="9db85-137">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="9db85-138">Núcleo</span><span class="sxs-lookup"><span data-stu-id="9db85-138">Merit</span></span>                  | <span data-ttu-id="9db85-139">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="9db85-139">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9db85-140">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="9db85-140">Filter Category</span></span>        | <span data-ttu-id="9db85-141">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="9db85-141">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="9db85-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="9db85-142">Remarks</span></span>

<span data-ttu-id="9db85-143">O leitor ASF do WM implementa parcialmente as interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** para fornecer aos aplicativos acesso aos métodos informativos no objeto Reader.</span><span class="sxs-lookup"><span data-stu-id="9db85-143">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="9db85-144">A implementação do filtro simplesmente passa as chamadas para a interface no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="9db85-144">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="9db85-145">Os métodos de streaming não são implementados porque o filtro deve ter controle total sobre o processo de streaming.</span><span class="sxs-lookup"><span data-stu-id="9db85-145">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="9db85-146">Os seguintes métodos **IWMReaderAdvanced** e **IWMReaderAdvanced2** são implementados:</span><span class="sxs-lookup"><span data-stu-id="9db85-146">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="9db85-147">**IWMReaderAdvanced:: getstatistics**</span><span class="sxs-lookup"><span data-stu-id="9db85-147">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="9db85-148">**IWMReaderAdvanced:: SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="9db85-148">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="9db85-149">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="9db85-149">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="9db85-150">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="9db85-150">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="9db85-151">**IWMReaderAdvanced2:: getplaymode**</span><span class="sxs-lookup"><span data-stu-id="9db85-151">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="9db85-152">**IWMReaderAdvanced2:: getprotocolname**</span><span class="sxs-lookup"><span data-stu-id="9db85-152">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="9db85-153">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="9db85-153">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="9db85-154">**IWMReaderAdvanced2:: SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="9db85-154">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="9db85-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9db85-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9db85-156">**Referência do QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="9db85-156">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="9db85-157">**Lendo arquivos ASF no DirectShow**</span><span class="sxs-lookup"><span data-stu-id="9db85-157">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




