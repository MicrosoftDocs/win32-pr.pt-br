---
title: Reprodução de fluxo da Web no DirectShow
description: Reprodução de fluxo da Web no DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- SDK do Windows Media Format, DirectShow
- Windows Media Format SDK, reprodução de fluxo da Web
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), reprodução de fluxo da Web
- ASF (formato de sistemas avançados), reprodução de fluxo da Web
- DirectShow, reprodução de fluxo da Web
- Fluxos da Web, DirectShow
- Fluxos da Web, reprodução no DirectShow
- fluxos, reprodução de fluxo da Web no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916093"
---
# <a name="web-stream-playback-in-directshow"></a><span data-ttu-id="3b71c-113">Reprodução de fluxo da Web no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3b71c-113">Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="3b71c-114">O Microsoft DirectShow dá suporte a fluxos da Web (consulte [Web streams](web-streams.md) para obter mais informações) em cenários de reprodução de arquivos por meio do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) , mas você deve escrever seu próprio filtro do DirectShow para capturar e manter o fluxo.</span><span class="sxs-lookup"><span data-stu-id="3b71c-114">Microsoft DirectShow supports Web streams (see [Web Streams](web-streams.md) for more information) in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="3b71c-115">Para reproduzir fluxos da Web no conteúdo que está sendo transmitido de um servidor que executa os serviços de mídia do Windows, use o controle de® do ActiveX do Windows Media Player 9 Series inserido em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="3b71c-115">To play back Web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a Web page.</span></span>

 

<span data-ttu-id="3b71c-116">Ao receber um arquivo contendo fluxos do tipo WMMEDIATYPE \_ FileTransfer, o leitor ASF do WM criará um PIN de saída para ele.</span><span class="sxs-lookup"><span data-stu-id="3b71c-116">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="3b71c-117">O bloco de formato será uma estrutura de [**\_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) .</span><span class="sxs-lookup"><span data-stu-id="3b71c-117">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="3b71c-118">Se não houver um filtro downstream disponível que possa lidar com esse tipo de mídia, o PIN permanecerá desconectado, mas o arquivo ainda reproduzirá os fluxos de áudio e/ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b71c-118">If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="3b71c-119">É importante entender que cada exemplo de mídia em um fluxo da Web contém uma estrutura de [**cabeçalho de \_ \_ exemplo \_ do webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , que tem um comprimento variável, dependendo do comprimento de seu membro **wszURL** .</span><span class="sxs-lookup"><span data-stu-id="3b71c-119">It is important to understand that each media sample in a Web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="3b71c-120">O ponteiro para os dados de exemplo aponta inicialmente para essa estrutura, e você deve avançar o ponteiro após a estrutura para acessar os dados reais no fluxo.</span><span class="sxs-lookup"><span data-stu-id="3b71c-120">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span> <span data-ttu-id="3b71c-121">O filtro do manipulador de fluxo da Web deve ser baseado na classe **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="3b71c-121">Your Web stream handler filter should be based on the **CBaseRenderer** class.</span></span> <span data-ttu-id="3b71c-122">No método **DoRenderSample** , o filtro precisará analisar a estrutura para obter informações sobre o fluxo da Web e, em seguida, executar a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="3b71c-122">In the **DoRenderSample** method, the filter will need to parse the structure for information about the Web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="3b71c-123">Normalmente, isso envolverá salvar o arquivo em disco e, em seguida, chamar **CommitUrlCacheEntry** e **CreateUrlCacheEntry** para colocar os arquivos no cache do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3b71c-123">Typically, this will involve saving the file to disk, and then calling **CommitUrlCacheEntry** and **CreateUrlCacheEntry** to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="3b71c-124">O filtro deve tratar arquivos com várias partes, ou seja, arquivos que são maiores que um exemplo, e também deve manipular comandos de renderização, que são especificados pelo membro **\_ \_ \_ header. WSAMPLETYPE de exemplo webstream WMT** .</span><span class="sxs-lookup"><span data-stu-id="3b71c-124">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="3b71c-125">O filtro envia um **\_ \_ evento OLE do EC** para o aplicativo, junto com o texto do **cabeçalho de \_ exemplo webstream do WMT \_ \_ .** cadeia de caracteres wszURL que contém o nome do arquivo a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="3b71c-125">The filter sends an **EC\_OLE\_EVENT** to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="3b71c-126">O aplicativo faz com que o navegador exiba a página especificada.</span><span class="sxs-lookup"><span data-stu-id="3b71c-126">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="3b71c-127">Se o fluxo da Web tiver sido criado corretamente, o arquivo já deverá estar no cache.</span><span class="sxs-lookup"><span data-stu-id="3b71c-127">If the Web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="3b71c-128">Para obter mais informações sobre o **\_ \_ evento OLE** **CBaseRenderer**, **DoRenderSample** e EC, consulte a documentação do SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3b71c-128">For more information on **CBaseRenderer**, **DoRenderSample**, and **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b71c-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b71c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b71c-130">**Fluxos da Web**</span><span class="sxs-lookup"><span data-stu-id="3b71c-130">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




