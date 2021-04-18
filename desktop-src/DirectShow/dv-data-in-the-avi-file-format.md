---
description: Dados de DV no formato de arquivo AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Dados de DV no formato de arquivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456792"
---
# <a name="dv-data-in-the-avi-file-format"></a><span data-ttu-id="cf734-103">Dados de DV no formato de arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="cf734-103">DV Data in the AVI File Format</span></span>

<span data-ttu-id="cf734-104">A Microsoft especificou o formato de armazenamento de dados de vídeo digital (DV) em arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="cf734-104">Microsoft has specified the format for storage of digital video (DV) data in AVI files.</span></span> <span data-ttu-id="cf734-105">Em conformidade com essa especificação, você garantirá que os arquivos AVI criados nesse formato serão compatíveis com as versões futuras da arquitetura de vídeo digital do DirectShow para o Windowsplatform.</span><span class="sxs-lookup"><span data-stu-id="cf734-105">Conforming to this specification will ensure that the AVI files authored in this format will be compatible with future versions of the DirectShow digital video architecture for the Windowsplatform.</span></span>

<span data-ttu-id="cf734-106">Este artigo descreve o formato dos arquivos AVI que contêm dados DV.</span><span class="sxs-lookup"><span data-stu-id="cf734-106">This article describes the format of AVI files containing DV data.</span></span> <span data-ttu-id="cf734-107">Os FOURCC (códigos de quatro caracteres) específicos para os fluxos de dados de DV e os manipuladores de fluxo do DV compressor/descompactador estão definidos.</span><span class="sxs-lookup"><span data-stu-id="cf734-107">Specific FOURCCs (four-character codes) for interleaved DV data streams and DV compressor/decompressor stream handlers are defined.</span></span> <span data-ttu-id="cf734-108">A estrutura de formato de fluxo para dados DV está definida.</span><span class="sxs-lookup"><span data-stu-id="cf734-108">The stream format structure for DV data is defined.</span></span> <span data-ttu-id="cf734-109">As especificações para dois métodos de armazenamento de dados DV no formato de arquivo AVI são especificadas.</span><span class="sxs-lookup"><span data-stu-id="cf734-109">Specifications for two methods of storing DV data in the AVI file format are specified.</span></span>

<span data-ttu-id="cf734-110">Supõe-se que o leitor esteja familiarizado com o formato de dados DV.</span><span class="sxs-lookup"><span data-stu-id="cf734-110">It is assumed that the reader is familiar with the DV data format.</span></span> <span data-ttu-id="cf734-111">(Esse formato é definido na *especificação de uso do consumidor digital VCRs*, também chamado de livro azul.)</span><span class="sxs-lookup"><span data-stu-id="cf734-111">(This format is defined in the *Specification of Consumer-use Digital VCRs*, also called the Blue Book.)</span></span>

<span data-ttu-id="cf734-112">Há dois tipos de arquivos AVI do DV: arquivos AVI que contêm um fluxo de dados DV, chamado arquivos do *tipo 1* ; e arquivos AVI que contêm vídeo DV como um fluxo ' vids ' e áudio DV como fluxos ' auds ', chamados *de arquivos de tipo 2* .</span><span class="sxs-lookup"><span data-stu-id="cf734-112">There are two types of DV AVI files: AVI files that contain one DV data stream, called *type-1* files; and AVI files that contain DV video as a 'vids' stream and DV audio as 'auds' streams, called *type-2* files.</span></span>

<span data-ttu-id="cf734-113">**Arquivos AVI contendo um fluxo de dados DV (tipo 1)**</span><span class="sxs-lookup"><span data-stu-id="cf734-113">**AVI Files Containing One DV Data Stream (Type-1)**</span></span>

<span data-ttu-id="cf734-114">Os dados intercalados de DV podem ser armazenados em seu formato nativo como um único fluxo dentro de um arquivo RIFF AVI.</span><span class="sxs-lookup"><span data-stu-id="cf734-114">Interleaved DV data can be stored in its native format as a single stream within an AVI RIFF file.</span></span> <span data-ttu-id="cf734-115">Isso tem a vantagem de usar a quantidade mínima de armazenamento de dados para DV.</span><span class="sxs-lookup"><span data-stu-id="cf734-115">This has the advantage of using the minimum amount of data storage for DV.</span></span> <span data-ttu-id="cf734-116">A desvantagem principal é que esse formato de arquivo não é compatível com versões anteriores com vídeo para Windows, porque ele não contém um vídeo "vids" ou um fluxo "auds" de áudio.</span><span class="sxs-lookup"><span data-stu-id="cf734-116">The primary disadvantage is that this file format is not backward-compatible with Video for Windows, because it doesn't contain either a video 'vids' or an audio 'auds' stream.</span></span> <span data-ttu-id="cf734-117">O suporte é fornecido para o fluxo DV intercalado por meio dos filtros [DV Muxer](dv-muxer-filter.md) e [DV Splitter](dv-splitter-filter.md) fornecidos com o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cf734-117">Support is provided for the interleaved DV stream through the [DV Muxer](dv-muxer-filter.md) and [DV Splitter](dv-splitter-filter.md) filters provided with DirectShow.</span></span>

<span data-ttu-id="cf734-118">Os dados de DV podem ser armazenados em um único fluxo dentro de um arquivo RIFF AVI especificando o "iAVS" (fluxo de áudio e vídeo intercalado) FOURCC (código de quatro caracteres) no membro **fccType** e qualquer um dos "dvsd", "dvhd" ou "DVSL" FOURCC no membro **fccHandler** da parte de cabeçalho de fluxo "strh".</span><span class="sxs-lookup"><span data-stu-id="cf734-118">DV data can be stored in a single stream within an AVI RIFF file by specifying the 'iavs' (interleaved audio and video stream) FOURCC (four-character code) in the **fccType** member and either of the 'dvsd', 'dvhd', or 'dvsl' FOURCCs in the **fccHandler** member of the 'strh' stream header chunk.</span></span> <span data-ttu-id="cf734-119">Os quadros por segundo do fluxo de vídeo devem ser especificados nos membros **dwRate** e **dwScale** e o número total de blocos de vídeo na parte ' movi ' no membro **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="cf734-119">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="cf734-120">O manipulador de fluxo ' dvsd ' FOURCC especifica que os dados de DV estão conforme definidos na parte 2 da *especificação de uso de consumidor digital VCRs*.</span><span class="sxs-lookup"><span data-stu-id="cf734-120">The 'dvsd' stream handler FOURCC specifies that the DV data is as defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="cf734-121">O vídeo está no formato de 525 linhas às 29,97 Hz (525-60) ou 625 linhas às 25, 0 Hz (625-50).</span><span class="sxs-lookup"><span data-stu-id="cf734-121">Video is in the format of 525 lines at 29.97 Hz (525-60) or 625 lines at 25.00 Hz (625-50).</span></span>

<span data-ttu-id="cf734-122">O manipulador de fluxo ' dvhd ' FOURCC especifica que os dados de DV estão conforme definidos na parte 3 da *especificação de uso de consumidor digital VCRs*.</span><span class="sxs-lookup"><span data-stu-id="cf734-122">The 'dvhd' stream handler FOURCC specifies that the DV data is as defined in Part 3 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="cf734-123">O vídeo está no formato de 1125 linhas às 30, 0 Hz (1125-60) ou 1250 linhas às 25, 0 Hz (1250-50).</span><span class="sxs-lookup"><span data-stu-id="cf734-123">Video is in the format of 1125 lines at 30.00 Hz (1125-60) or 1250 lines at 25.00 Hz (1250-50).</span></span>

<span data-ttu-id="cf734-124">O manipulador de fluxo ' dvsl ' FOURCC especifica que os dados de DV são os mesmos definidos na parte 6 da *especificação de uso do consumidor digital VCRs*.</span><span class="sxs-lookup"><span data-stu-id="cf734-124">The 'dvsl' stream handler FOURCC specifies that the DV data is as defined in Part 6 of *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="cf734-125">O vídeo está no formato de alta compactação SD (SDL).</span><span class="sxs-lookup"><span data-stu-id="cf734-125">Video is in the format of high-compression SD (SDL).</span></span>

> [!Note]  
> <span data-ttu-id="cf734-126">O restante deste artigo fornece definições para fluxos ' dvsd '.</span><span class="sxs-lookup"><span data-stu-id="cf734-126">The remainder of this article provides definitions for 'dvsd' streams.</span></span>

 

<span data-ttu-id="cf734-127">A parte do cabeçalho do fluxo deve ser seguida por uma parte do formato de fluxo [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="cf734-127">The stream header chunk must be followed by a [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) stream format chunk.</span></span>

<span data-ttu-id="cf734-128">Os dados reais de DV são armazenados como \# \# partes ' DC ' na parte ' movi ' (o \# \# no formato representa o identificador de fluxo).</span><span class="sxs-lookup"><span data-stu-id="cf734-128">The actual DV data is stored as '\#\#dc' chunks in the 'movi' chunk (the \#\# in the format represents the stream identifier).</span></span> <span data-ttu-id="cf734-129">Cada parte contém um quadro de dados, de 10 ou 12 seqüências de DV DIF para sistemas 525-60 ou 625-50, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cf734-129">Each chunk contains one frame of data, either 10 or 12 DV DIF sequences for 525-60 or 625-50 systems, respectively.</span></span> <span data-ttu-id="cf734-130">O formato de sequência DIF DV SD (' dvsd ') é definido na parte 2 da *especificação de uso de consumidor VCRs digital*.</span><span class="sxs-lookup"><span data-stu-id="cf734-130">The DV SD ('dvsd') DIF sequence format is defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span>

<span data-ttu-id="cf734-131">O exemplo a seguir mostra o formato de RIFF AIFF para um arquivo AVI com um fluxo de dados DV, expandido com partes de cabeçalho concluídas.</span><span class="sxs-lookup"><span data-stu-id="cf734-131">The following example shows the AIFF RIFF form for an AVI file with one DV data stream, expanded with completed header chunks.</span></span>


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



<span data-ttu-id="cf734-132">**Arquivos AVI que contêm vídeo DV e fluxos de áudio DV (tipo 2)**</span><span class="sxs-lookup"><span data-stu-id="cf734-132">**AVI Files Containing DV Video and DV Audio Streams (Type-2)**</span></span>

<span data-ttu-id="cf734-133">Os dados intercalados de DV podem ser divididos em um fluxo de vídeo e de um a quatro fluxos de áudio em um arquivo RIFF AVI.</span><span class="sxs-lookup"><span data-stu-id="cf734-133">Interleaved DV data can be split into a video stream and one to four audio streams within an AVI RIFF file.</span></span> <span data-ttu-id="cf734-134">Isso tem a vantagem de ser compatível com versões anteriores com vídeo para Windows, pois contém um fluxo de vídeo "vids" padrão e pelo menos um fluxo de áudio "auds" padrão. a desvantagem principal é que esse formato de arquivo requer que os dados de áudio sejam armazenados de forma redundante como fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="cf734-134">This has the advantage of being backward-compatible with Video for Windows, because it contains a standard video 'vids' stream and at least one standard audio 'auds' stream The primary disadvantage is that this file format requires the audio data to be redundantly stored as audio streams.</span></span> <span data-ttu-id="cf734-135">O fluxo de "vídeo" é, na verdade, o fluxo de dados de DV intercalado nativo.</span><span class="sxs-lookup"><span data-stu-id="cf734-135">The "video" stream is actually the native interleaved DV data stream.</span></span> <span data-ttu-id="cf734-136">No entanto, como um fluxo "vids" padrão com um tipo de manipulador de "dvsd", o [decodificador de vídeo DV](dv-video-decoder-filter.md) é usado.</span><span class="sxs-lookup"><span data-stu-id="cf734-136">However, as a standard 'vids' stream with a handler type of 'dvsd', the [DV Video Decoder](dv-video-decoder-filter.md) is used.</span></span> <span data-ttu-id="cf734-137">Esse formato também requer o uso do filtro de [Splitter DV](dv-splitter-filter.md) para dividir arquivos "capturados" antes de gravá-los como arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="cf734-137">This format also requires using the [DV Splitter](dv-splitter-filter.md) filter to split "captured" files before writing them as AVI files.</span></span>

<span data-ttu-id="cf734-138">Os dados DV podem ser armazenados como um fluxo de vídeo com um número separado de fluxos de áudio em um arquivo RIFF AVI.</span><span class="sxs-lookup"><span data-stu-id="cf734-138">DV data can be stored as a video stream with a separate number of audio streams in an AVI RIFF file.</span></span> <span data-ttu-id="cf734-139">O fluxo de vídeo é especificado com um cabeçalho de fluxo de vídeo padrão (o valor do membro **fccType** é ' vids ').</span><span class="sxs-lookup"><span data-stu-id="cf734-139">The video stream is specified with a standard video stream header (the **fccType** member value is 'vids').</span></span> <span data-ttu-id="cf734-140">O membro **fccHandler** é especificado como ' dvsd ', ' dvhd ' ou ' dvsl '.</span><span class="sxs-lookup"><span data-stu-id="cf734-140">The **fccHandler** member is specified as 'dvsd', 'dvhd', or 'dvsl'.</span></span> <span data-ttu-id="cf734-141">Os quadros por segundo do fluxo de vídeo devem ser especificados nos membros **dwRate** e **dwScale** e o número total de blocos de vídeo na parte ' movi ' no membro **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="cf734-141">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="cf734-142">Neste arquivo AVI que contém vídeo DV como um fluxo ' vids ' e áudio DV como forma de fluxos ' auds ' de DV, a parte do formato de fluxo de vídeo é uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) padrão.</span><span class="sxs-lookup"><span data-stu-id="cf734-142">In this AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams form of DV, the video stream format chunk is a standard [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="cf734-143">A parte de formato de fluxo pode ser estendida opcionalmente para incluir a parte [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , aumentando o tamanho da parte do formato de fluxo de 40 bytes (tamanho da estrutura **BITMAPINFOHEADER** ) para 72 bytes (tamanho das estruturas **BITMAPINFOHEADER** mais **DVINFO** ) e imediatamente após a estrutura de dados **BITMAPINFOHEADER** com uma estrutura de dados **DVINFO** .</span><span class="sxs-lookup"><span data-stu-id="cf734-143">The stream format chunk can be optionally extended to include the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) chunk, by increasing the stream format chunk size from 40 bytes (size of the **BITMAPINFOHEADER** structure) to 72 bytes (size of **BITMAPINFOHEADER** plus **DVINFO** structures) and immediately following the **BITMAPINFOHEADER** data structure with a **DVINFO** data structure.</span></span>

<span data-ttu-id="cf734-144">Os fluxos de áudio são especificados com um cabeçalho de fluxo de áudio padrão (o valor do membro **fccType** é ' auds ').</span><span class="sxs-lookup"><span data-stu-id="cf734-144">The audio stream(s) is specified with a standard audio stream header (the **fccType** member value is 'auds').</span></span> <span data-ttu-id="cf734-145">O membro **fccHandler** não é usado para fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="cf734-145">The **fccHandler** member is not used for audio streams.</span></span>

<span data-ttu-id="cf734-146">Os dados de vídeo DV são armazenados como \# \# partes ' DC ', conforme definido na descrição anterior de um arquivo AVI com um dado DV, e os dados de áudio são armazenados como \# \# partes ' WB ' na parte ' movi '.</span><span class="sxs-lookup"><span data-stu-id="cf734-146">The DV video data is stored as '\#\#dc' chunks, as defined in the preceding description of an AVI file with one DV data, and the audio data is stored as '\#\#wb' chunks in the 'movi' chunk.</span></span>

> [!Note]  
> <span data-ttu-id="cf734-147">A *especificação do VCRs digital de uso do consumidor* pode não estar disponível em alguns idiomas e países.</span><span class="sxs-lookup"><span data-stu-id="cf734-147">The *Specification of Consumer-use Digital VCRs* may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="cf734-148">O exemplo a seguir mostra o formato de RIFF AIFF para um arquivo AVI que contém o vídeo DV como um fluxo ' vids ' e áudio DV como fluxos ' auds ' expandidos com fragmentos de cabeçalho concluídos (incluindo dados [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) opcionais que seguem o [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) na subparte ' strf ' para o fluxo ' vids ').</span><span class="sxs-lookup"><span data-stu-id="cf734-148">The following example shows the AIFF RIFF form for an AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams expanded with completed header chunks (including optional [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) data following the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) in the 'strf' sub-chunk for the 'vids' stream).</span></span>


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a><span data-ttu-id="cf734-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf734-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf734-150">Formato de arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="cf734-150">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
