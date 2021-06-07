---
title: Filtro de Leitor do WM ASF (Windows Media Format SDK 11)
description: Saiba mais sobre o filtro leitor do WM ASF.
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
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444277"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="7f105-109">Filtro de Leitor do WM ASF (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="7f105-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="7f105-110">Quando dado o nome de um arquivo ASF ou uma URL, o Leitor do WM ASF lê o conteúdo compactado, analisado os fluxos e expõe um pino de saída para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="7f105-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="7f105-111">Esse filtro conecta-se downstream aos DMOs de Áudio de Mídia do Windows ou Vídeo de Mídia do Windows, que fazem a descompactação.</span><span class="sxs-lookup"><span data-stu-id="7f105-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="7f105-112">A busca será suportada se o arquivo ASF for buscado.</span><span class="sxs-lookup"><span data-stu-id="7f105-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="7f105-113">O Leitor do WM ASF aplica carimbos de data/hora aos exemplos de mídia com base no carimbo de data/hora no arquivo ASF, mas não modifica os carimbos de data/hora de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="7f105-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="7f105-114">Internamente, o filtro usa o Windows Media Format de leitura para ler o conteúdo baseado em Mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f105-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="7f105-115">No SDK do DirectX, esse filtro não é o filtro de origem padrão para arquivos ASF, portanto, com esse SDK, você não pode usar esse filtro com o **método RenderFile;** você deve adicioná-lo explicitamente ao grafo de filtro usando seu CLSID (identificador de classe).</span><span class="sxs-lookup"><span data-stu-id="7f105-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="7f105-116">Esse comportamento é diferente com o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="7f105-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="7f105-117">Quando você instala as bibliotecas de runtime Windows Media Format SDK, o Leitor do WM ASF é registrado como o filtro padrão para arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="7f105-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="7f105-118">A tabela a seguir contém informações sobre o filtro leitor do WM ASF, como as interfaces e tipos de mídia aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="7f105-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="7f105-119">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="7f105-119">Filter Information</span></span>                      |  <span data-ttu-id="7f105-120">Tipos</span><span class="sxs-lookup"><span data-stu-id="7f105-120">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f105-121">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="7f105-121">Filter interfaces</span></span>      | <span data-ttu-id="7f105-122">**IBaseFilter,** **IFileSourceFilter,** **IServiceProvider,** **IWMHeaderInfo,** **IWMReaderAdvanced** (parcialmente implementado.</span><span class="sxs-lookup"><span data-stu-id="7f105-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="7f105-123">Consulte Comentários.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (por **meio de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="7f105-123">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="7f105-124">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7f105-124">Input pin media types</span></span>  | <span data-ttu-id="7f105-125">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="7f105-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="7f105-126">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7f105-126">Input pin interfaces</span></span>   | <span data-ttu-id="7f105-127">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="7f105-127">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="7f105-128">Tipos de mídia de pino de saída</span><span class="sxs-lookup"><span data-stu-id="7f105-128">Output pin media types</span></span> | <span data-ttu-id="7f105-129">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="7f105-129">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="7f105-130">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="7f105-130">Format type</span></span>            | <span data-ttu-id="7f105-131">**VIDEOINFOHEADER2** se o conteúdo estiver [*entrelaçado;*](wmformat-glossary.md)caso contrário, **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="7f105-131">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="7f105-132">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="7f105-132">Output pin interfaces</span></span>  | <span data-ttu-id="7f105-133">**IMediaSeeking,** **IAMWMBufferPass,** **IServiceProvider,** **IWMStreamConfig2** (por **meio de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="7f105-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="7f105-134">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="7f105-134">Filter CLSID</span></span>           | <span data-ttu-id="7f105-135">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="7f105-135">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="7f105-136">CLSID da página de propriedades</span><span class="sxs-lookup"><span data-stu-id="7f105-136">Property Page CLSID</span></span>    | <span data-ttu-id="7f105-137">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="7f105-137">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="7f105-138">Executável</span><span class="sxs-lookup"><span data-stu-id="7f105-138">Executable</span></span>             | <span data-ttu-id="7f105-139">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="7f105-139">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="7f105-140">Mérito</span><span class="sxs-lookup"><span data-stu-id="7f105-140">Merit</span></span>                  | <span data-ttu-id="7f105-141">IMPROVÁVEL DE \_ VERÃO</span><span class="sxs-lookup"><span data-stu-id="7f105-141">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="7f105-142">Categoria de filtro</span><span class="sxs-lookup"><span data-stu-id="7f105-142">Filter Category</span></span>        | <span data-ttu-id="7f105-143">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7f105-143">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="7f105-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f105-144">Remarks</span></span>

<span data-ttu-id="7f105-145">O Leitor do WM ASF implementa parcialmente as interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** para dar aos aplicativos acesso aos métodos informacionais no objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="7f105-145">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="7f105-146">A implementação do filtro simplesmente passa as chamadas para a interface no objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="7f105-146">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="7f105-147">Os métodos de streaming não são implementados porque o filtro deve ter controle total sobre o processo de streaming.</span><span class="sxs-lookup"><span data-stu-id="7f105-147">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="7f105-148">Os seguintes **métodos IWMReaderAdvanced** **e IWMReaderAdvanced2** são implementados:</span><span class="sxs-lookup"><span data-stu-id="7f105-148">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="7f105-149">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="7f105-149">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="7f105-150">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="7f105-150">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="7f105-151">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="7f105-151">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="7f105-152">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="7f105-152">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="7f105-153">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="7f105-153">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="7f105-154">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="7f105-154">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="7f105-155">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="7f105-155">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="7f105-156">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="7f105-156">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="7f105-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f105-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f105-158">**Referência de QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="7f105-158">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="7f105-159">**Lendo arquivos ASF no DirectShow**</span><span class="sxs-lookup"><span data-stu-id="7f105-159">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




