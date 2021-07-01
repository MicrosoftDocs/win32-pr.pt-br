---
title: Filtro de Leitor do WM ASF (Windows Media Format SDK 11)
description: Saiba mais sobre o filtro leitor do WM ASF para o SDK Windows Media Format 11. Revise as informações de filtro e consulte os tópicos relacionados.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, Leitor do WM ASF
- DirectShow, Leitor do WM ASF
- Filtros QASF, Leitor do WM ASF
- Leitor do WM ASF
- AsF (Advanced Systems Format), WM ASF Reader
- ASF (formato de sistemas avançados), leitor do WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bde36b1b2cfa7644d6e75d8d1ff96260b2e457
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119641"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="a5648-110">Filtro de Leitor do WM ASF (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="a5648-110">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a5648-111">Quando dado o nome de um arquivo ASF ou uma URL, o Leitor do WM ASF lê o conteúdo compactado, analisado os fluxos e expõe um pino de saída para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="a5648-111">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="a5648-112">Esse filtro conecta-se downstream aos DMOs de Áudio de Mídia do Windows ou Vídeo de Mídia do Windows, que fazem a descompactação.</span><span class="sxs-lookup"><span data-stu-id="a5648-112">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="a5648-113">A busca será suportada se o arquivo ASF for buscado.</span><span class="sxs-lookup"><span data-stu-id="a5648-113">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="a5648-114">O Leitor do WM ASF aplica carimbos de data/hora aos exemplos de mídia com base no carimbo de data/hora no arquivo ASF, mas não modifica os carimbos de data/hora de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="a5648-114">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="a5648-115">Internamente, o filtro usa o Windows Media Format de leitura para ler o conteúdo baseado em Mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="a5648-115">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="a5648-116">No SDK do DirectX, esse filtro não é o filtro de origem padrão para arquivos ASF, portanto, com esse SDK, você não pode usar esse filtro com o **método RenderFile;** você deve adicioná-lo explicitamente ao grafo de filtro usando seu CLSID (identificador de classe).</span><span class="sxs-lookup"><span data-stu-id="a5648-116">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="a5648-117">Esse comportamento é diferente com o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a5648-117">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="a5648-118">Quando você instala as bibliotecas de runtime Windows Media Format SDK, o Leitor do WM ASF é registrado como o filtro padrão para arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="a5648-118">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="a5648-119">A tabela a seguir contém informações sobre o filtro leitor do WM ASF, como as interfaces e tipos de mídia aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="a5648-119">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="a5648-120">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="a5648-120">Filter Information</span></span>                      |  <span data-ttu-id="a5648-121">Tipos</span><span class="sxs-lookup"><span data-stu-id="a5648-121">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5648-122">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="a5648-122">Filter interfaces</span></span>      | <span data-ttu-id="a5648-123">**IBaseFilter,** **IFileSourceFilter,** **IServiceProvider,** **IWMHeaderInfo,** **IWMReaderAdvanced** (parcialmente implementado.</span><span class="sxs-lookup"><span data-stu-id="a5648-123">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="a5648-124">Consulte Comentários.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (por **meio de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="a5648-124">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="a5648-125">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a5648-125">Input pin media types</span></span>  | <span data-ttu-id="a5648-126">Não se aplica</span><span class="sxs-lookup"><span data-stu-id="a5648-126">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="a5648-127">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a5648-127">Input pin interfaces</span></span>   | <span data-ttu-id="a5648-128">Não se aplica</span><span class="sxs-lookup"><span data-stu-id="a5648-128">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="a5648-129">Tipos de mídia de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a5648-129">Output pin media types</span></span> | <span data-ttu-id="a5648-130">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="a5648-130">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="a5648-131">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="a5648-131">Format type</span></span>            | <span data-ttu-id="a5648-132">**VIDEOINFOHEADER2** se o conteúdo estiver [*entrelaçado;*](wmformat-glossary.md)caso contrário, **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="a5648-132">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="a5648-133">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a5648-133">Output pin interfaces</span></span>  | <span data-ttu-id="a5648-134">**IMediaSeeking,** **IAMWMBufferPass,** **IServiceProvider,** **IWMStreamConfig2** (por **meio de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="a5648-134">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="a5648-135">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="a5648-135">Filter CLSID</span></span>           | <span data-ttu-id="a5648-136">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="a5648-136">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="a5648-137">CLSID da página de propriedades</span><span class="sxs-lookup"><span data-stu-id="a5648-137">Property Page CLSID</span></span>    | <span data-ttu-id="a5648-138">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="a5648-138">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="a5648-139">Executável</span><span class="sxs-lookup"><span data-stu-id="a5648-139">Executable</span></span>             | <span data-ttu-id="a5648-140">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="a5648-140">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="a5648-141">Mérito</span><span class="sxs-lookup"><span data-stu-id="a5648-141">Merit</span></span>                  | <span data-ttu-id="a5648-142">IMPROVÁVEL DE \_ VERÃO</span><span class="sxs-lookup"><span data-stu-id="a5648-142">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a5648-143">Categoria de filtro</span><span class="sxs-lookup"><span data-stu-id="a5648-143">Filter Category</span></span>        | <span data-ttu-id="a5648-144">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a5648-144">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a5648-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5648-145">Remarks</span></span>

<span data-ttu-id="a5648-146">O Leitor do WM ASF implementa parcialmente as interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** para dar aos aplicativos acesso aos métodos informacionais no objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="a5648-146">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="a5648-147">A implementação do filtro simplesmente passa as chamadas para a interface no objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="a5648-147">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="a5648-148">Os métodos de streaming não são implementados porque o filtro deve ter controle total sobre o processo de streaming.</span><span class="sxs-lookup"><span data-stu-id="a5648-148">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="a5648-149">Os seguintes **métodos IWMReaderAdvanced** **e IWMReaderAdvanced2** são implementados:</span><span class="sxs-lookup"><span data-stu-id="a5648-149">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="a5648-150">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="a5648-150">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="a5648-151">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="a5648-151">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="a5648-152">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="a5648-152">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="a5648-153">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="a5648-153">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="a5648-154">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="a5648-154">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="a5648-155">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="a5648-155">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="a5648-156">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="a5648-156">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="a5648-157">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="a5648-157">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="a5648-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5648-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5648-159">**Referência de QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="a5648-159">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="a5648-160">**Lendo arquivos ASF no DirectShow**</span><span class="sxs-lookup"><span data-stu-id="a5648-160">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




