---
description: Referência de arquivo RIFF AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Referência de arquivo RIFF AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456831"
---
# <a name="avi-riff-file-reference"></a><span data-ttu-id="128a5-103">Referência de arquivo RIFF AVI</span><span class="sxs-lookup"><span data-stu-id="128a5-103">AVI RIFF File Reference</span></span>

<span data-ttu-id="128a5-104">O formato de arquivo AVI da Microsoft é uma especificação de arquivo RIFF usada com aplicativos que capturam, editam e reproduzem sequências de vídeo de áudio.</span><span class="sxs-lookup"><span data-stu-id="128a5-104">The Microsoft AVI file format is a RIFF file specification used with applications that capture, edit, and play back audio-video sequences.</span></span> <span data-ttu-id="128a5-105">Em geral, os arquivos AVI contêm vários fluxos de diferentes tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="128a5-105">In general, AVI files contain multiple streams of different types of data.</span></span> <span data-ttu-id="128a5-106">A maioria das sequências AVI usa fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="128a5-106">Most AVI sequences use both audio and video streams.</span></span> <span data-ttu-id="128a5-107">Uma variação simples para uma sequência AVI usa dados de vídeo e não requer um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="128a5-107">A simple variation for an AVI sequence uses video data and does not require an audio stream.</span></span>

<span data-ttu-id="128a5-108">Esta seção não descreve as extensões de formato de arquivo AVI OpenDML.</span><span class="sxs-lookup"><span data-stu-id="128a5-108">This section does not describe the OpenDML AVI file format extensions.</span></span> <span data-ttu-id="128a5-109">Para obter mais informações sobre essas extensões, consulte *extensões de formato de arquivo AVI OpenDML*, publicadas pelo Subcomitê OpenDML AVI M-JPEG File Format.</span><span class="sxs-lookup"><span data-stu-id="128a5-109">For further information on these extensions, see *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="fourccs"></a><span data-ttu-id="128a5-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="128a5-110">FOURCCs</span></span>

<span data-ttu-id="128a5-111">Um FOURCC (código de quatro caracteres) é um inteiro sem sinal de 32 bits criado com a concatenação de quatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="128a5-111">A FOURCC (four-character code) is a 32-bit unsigned integer created by concatenating four ASCII characters.</span></span> <span data-ttu-id="128a5-112">Por exemplo, o ' ABCD ' FOURCC é representado em um sistema de Little-Endian como 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="128a5-112">For example, the FOURCC 'abcd' is represented on a Little-Endian system as 0x64636261.</span></span> <span data-ttu-id="128a5-113">Os FOURCCs podem conter caracteres de espaço, portanto, ' abc ' é um FOURCC válido.</span><span class="sxs-lookup"><span data-stu-id="128a5-113">FOURCCs can contain space characters, so ' abc' is a valid FOURCC.</span></span> <span data-ttu-id="128a5-114">O formato de arquivo AVI usa códigos FOURCC para identificar tipos de fluxo, partes de dados, entradas de índice e outras informações.</span><span class="sxs-lookup"><span data-stu-id="128a5-114">The AVI file format uses FOURCC codes to identify stream types, data chunks, index entries, and other information.</span></span>

## <a name="riff-file-format"></a><span data-ttu-id="128a5-115">Formato de arquivo RIFF</span><span class="sxs-lookup"><span data-stu-id="128a5-115">RIFF File Format</span></span>

<span data-ttu-id="128a5-116">O formato de arquivo AVI é baseado no formato de documento RIFF (formato de arquivo de intercâmbio de recursos).</span><span class="sxs-lookup"><span data-stu-id="128a5-116">The AVI file format is based on the RIFF (resource interchange file format) document format.</span></span> <span data-ttu-id="128a5-117">Um arquivo RIFF consiste em um cabeçalho RIFF seguido por zero ou mais *listas* e *partes*.</span><span class="sxs-lookup"><span data-stu-id="128a5-117">A RIFF file consists of a RIFF header followed by zero or more *lists* and *chunks*.</span></span>

-   <span data-ttu-id="128a5-118">O cabeçalho RIFF tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="128a5-118">The RIFF header has the following form:</span></span>

    `'RIFF' fileSize fileType (data)`

    <span data-ttu-id="128a5-119">onde ' RIFF ' é o código FOURCC literal ' RIFF ', `fileSize` é um valor de 4 bytes fornecendo o tamanho dos dados no arquivo e `fileType` é um FOURCC que identifica o tipo de arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="128a5-119">where 'RIFF' is the literal FOURCC code 'RIFF', `fileSize` is a 4-byte value giving the size of the data in the file, and `fileType` is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="128a5-120">O valor de `fileSize` inclui o tamanho do `fileType` FOURCC mais o tamanho dos dados a seguir, mas não inclui o tamanho de ' riff ' FOURCC ou o tamanho de `fileSize` .</span><span class="sxs-lookup"><span data-stu-id="128a5-120">The value of `fileSize` includes the size of the `fileType` FOURCC plus the size of the data that follows, but does not include the size of the 'RIFF' FOURCC or the size of `fileSize`.</span></span> <span data-ttu-id="128a5-121">Os dados de arquivo consistem em partes e listas, em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="128a5-121">The file data consists of chunks and lists, in any order.</span></span>

-   <span data-ttu-id="128a5-122">Uma parte tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="128a5-122">A chunk has the following form:</span></span>

    `ckID ckSize ckData`

    <span data-ttu-id="128a5-123">onde `ckID` é um FOURCC que identifica os dados contidos na parte, `ckSize` é um valor de 4 bytes fornecendo o tamanho dos dados `ckData` e `ckData` é zero ou mais bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="128a5-123">where `ckID` is a FOURCC that identifies the data contained in the chunk, `ckSize` is a 4-byte value giving the size of the data in `ckData`, and `ckData` is zero or more bytes of data.</span></span> <span data-ttu-id="128a5-124">Os dados sempre são preenchidos para o limite de **palavras** mais próximo.</span><span class="sxs-lookup"><span data-stu-id="128a5-124">The data is always padded to nearest **WORD** boundary.</span></span> <span data-ttu-id="128a5-125">`ckSize` fornece o tamanho dos dados válidos na parte; Ele não inclui o preenchimento, o tamanho `ckID` ou o tamanho de `ckSize` .</span><span class="sxs-lookup"><span data-stu-id="128a5-125">`ckSize` gives the size of the valid data in the chunk; it does not include the padding, the size of `ckID`, or the size of `ckSize`.</span></span>

-   <span data-ttu-id="128a5-126">Uma lista tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="128a5-126">A list has the following form:</span></span>

    `'LIST' listSize listType listData`

    <span data-ttu-id="128a5-127">onde ' LIST ' é o código FOURCC literal ' LIST ', `listSize` é um valor de 4 bytes que dá o tamanho da lista, `listType` é um código FOURCC e `listData` consiste em partes ou listas, em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="128a5-127">where 'LIST' is the literal FOURCC code 'LIST', `listSize` is a 4-byte value giving the size of the list, `listType` is a FOURCC code, and `listData` consists of chunks or lists, in any order.</span></span> <span data-ttu-id="128a5-128">O valor de `listSize` inclui o tamanho de `listType` mais o tamanho de `listData` ; ele não inclui o FOURCC ' list ' ou o tamanho de `listSize` .</span><span class="sxs-lookup"><span data-stu-id="128a5-128">The value of `listSize` includes the size of `listType` plus the size of `listData`; it does not include the 'LIST' FOURCC or the size of `listSize`.</span></span>

<span data-ttu-id="128a5-129">O restante desta seção usa a seguinte notação para descrever as partes do RIFF:</span><span class="sxs-lookup"><span data-stu-id="128a5-129">The remainder of this section uses the following notation to describe RIFF chunks:</span></span>

`ckID ( ckData )`

<span data-ttu-id="128a5-130">onde o tamanho da parte é implícito.</span><span class="sxs-lookup"><span data-stu-id="128a5-130">where the chunk size is implicit.</span></span> <span data-ttu-id="128a5-131">Usando essa notação, uma lista pode ser representada como:</span><span class="sxs-lookup"><span data-stu-id="128a5-131">Using this notation, a list can be represented as:</span></span>

`'LIST' ( listType ( listData ) )`

<span data-ttu-id="128a5-132">Elementos opcionais são colocados entre colchetes: `[ optional element ]`</span><span class="sxs-lookup"><span data-stu-id="128a5-132">Optional elements are placed in brackets: `[ optional element ]`</span></span>

## <a name="avi-riff-form"></a><span data-ttu-id="128a5-133">Formulário RIFF AVI</span><span class="sxs-lookup"><span data-stu-id="128a5-133">AVI RIFF Form</span></span>

<span data-ttu-id="128a5-134">Os arquivos AVI são identificados pelo ' AVI ' FOURCC no cabeçalho RIFF.</span><span class="sxs-lookup"><span data-stu-id="128a5-134">AVI files are identified by the FOURCC 'AVI ' in the RIFF header.</span></span> <span data-ttu-id="128a5-135">Todos os arquivos AVI incluem duas partes de lista obrigatórias, que definem o formato dos fluxos e os dados de fluxo, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="128a5-135">All AVI files include two mandatory LIST chunks, which define the format of the streams and the stream data, respectively.</span></span> <span data-ttu-id="128a5-136">Um arquivo AVI também pode incluir uma parte de índice, que fornece o local das partes de dados dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="128a5-136">An AVI file might also include an index chunk, which gives the location of the data chunks within the file.</span></span> <span data-ttu-id="128a5-137">Um arquivo AVI com esses componentes tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="128a5-137">An AVI file with these components has the following form:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



<span data-ttu-id="128a5-138">A lista ' hdrl ' define o formato dos dados e é a primeira parte da lista necessária.</span><span class="sxs-lookup"><span data-stu-id="128a5-138">The 'hdrl' list defines the format of the data and is the first required LIST chunk.</span></span> <span data-ttu-id="128a5-139">A lista ' movi ' contém os dados para a sequência AVI e é a segunda parte de lista necessária.</span><span class="sxs-lookup"><span data-stu-id="128a5-139">The 'movi' list contains the data for the AVI sequence and is the second required LIST chunk.</span></span> <span data-ttu-id="128a5-140">A lista ' idx1 ' contém o índice.</span><span class="sxs-lookup"><span data-stu-id="128a5-140">The 'idx1' list contains the index.</span></span> <span data-ttu-id="128a5-141">Os arquivos AVI devem manter esses três componentes na sequência correta.</span><span class="sxs-lookup"><span data-stu-id="128a5-141">AVI files must keep these three components in the proper sequence.</span></span>

> [!Note]  
> <span data-ttu-id="128a5-142">As extensões OpenDML definem outro tipo de índice, identificado pelo ' INDX ' FOURCC.</span><span class="sxs-lookup"><span data-stu-id="128a5-142">The OpenDML extensions define another type of index, identified by the FOURCC 'indx'.</span></span>

 

<span data-ttu-id="128a5-143">As listas ' hdrl ' e ' movi ' usam subpartes para seus dados.</span><span class="sxs-lookup"><span data-stu-id="128a5-143">The 'hdrl' and 'movi' lists use subchunks for their data.</span></span> <span data-ttu-id="128a5-144">O exemplo a seguir mostra o formulário RIFF AVI expandido com as partes necessárias para concluir essas listas:</span><span class="sxs-lookup"><span data-stu-id="128a5-144">The following example shows the AVI RIFF form expanded with the chunks needed to complete these lists:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a><span data-ttu-id="128a5-145">Cabeçalho principal AVI</span><span class="sxs-lookup"><span data-stu-id="128a5-145">AVI Main Header</span></span>

<span data-ttu-id="128a5-146">A lista ' hdrl ' começa com o cabeçalho AVI principal, que está contido em uma parte ' avih '.</span><span class="sxs-lookup"><span data-stu-id="128a5-146">The 'hdrl' list begins with the main AVI header, which is contained in an 'avih' chunk.</span></span> <span data-ttu-id="128a5-147">O cabeçalho principal contém informações globais para todo o arquivo AVI, como o número de fluxos dentro do arquivo e a largura e a altura da sequência AVI.</span><span class="sxs-lookup"><span data-stu-id="128a5-147">The main header contains global information for the entire AVI file, such as the number of streams within the file and the width and height of the AVI sequence.</span></span> <span data-ttu-id="128a5-148">A parte do cabeçalho principal consiste em uma estrutura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="128a5-148">The main header chunk consists of an [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

## <a name="avi-stream-headers"></a><span data-ttu-id="128a5-149">Cabeçalhos de fluxo AVI</span><span class="sxs-lookup"><span data-stu-id="128a5-149">AVI Stream Headers</span></span>

<span data-ttu-id="128a5-150">Uma ou mais listas de ' strl ' seguem o cabeçalho principal.</span><span class="sxs-lookup"><span data-stu-id="128a5-150">One or more 'strl' lists follow the main header.</span></span> <span data-ttu-id="128a5-151">Uma lista ' strl ' é necessária para cada fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="128a5-151">A 'strl' list is required for each data stream.</span></span> <span data-ttu-id="128a5-152">Cada lista ' strl ' contém informações sobre um fluxo no arquivo e deve conter uma parte de cabeçalho de fluxo (' strh ') e uma parte de formato de fluxo (' strf ').</span><span class="sxs-lookup"><span data-stu-id="128a5-152">Each 'strl' list contains information about one stream in the file, and must contain a stream header chunk ('strh') and a stream format chunk ('strf').</span></span> <span data-ttu-id="128a5-153">Além disso, uma lista ' strl ' pode conter uma parte de dados de cabeçalho de fluxo (' strd ') e uma parte de nome de fluxo (' strn ').</span><span class="sxs-lookup"><span data-stu-id="128a5-153">In addition, a 'strl' list might contain a stream-header data chunk ('strd') and a stream name chunk ('strn').</span></span>

<span data-ttu-id="128a5-154">A parte do cabeçalho do fluxo (' strh ') consiste em uma estrutura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .</span><span class="sxs-lookup"><span data-stu-id="128a5-154">The stream header chunk ('strh') consists of an [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure.</span></span>

<span data-ttu-id="128a5-155">Uma parte do formato do fluxo (' strf ') deve seguir a parte do cabeçalho do fluxo.</span><span class="sxs-lookup"><span data-stu-id="128a5-155">A stream format chunk ('strf') must follow the stream header chunk.</span></span> <span data-ttu-id="128a5-156">A parte do formato do fluxo descreve o formato dos dados no fluxo.</span><span class="sxs-lookup"><span data-stu-id="128a5-156">The stream format chunk describes the format of the data in the stream.</span></span> <span data-ttu-id="128a5-157">Os dados contidos nessa parte dependem do tipo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="128a5-157">The data contained in this chunk depends on the stream type.</span></span> <span data-ttu-id="128a5-158">Para fluxos de vídeo, as informações são uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , incluindo informações de paleta, se apropriado.</span><span class="sxs-lookup"><span data-stu-id="128a5-158">For video streams, the information is a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, including palette information if appropriate.</span></span> <span data-ttu-id="128a5-159">Para fluxos de áudio, as informações são uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="128a5-159">For audio streams, the information is a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="128a5-160">Se a parte de dados de cabeçalho de fluxo (' strd ') estiver presente, ela seguirá a parte de formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="128a5-160">If the stream-header data ('strd') chunk is present, it follows the stream format chunk.</span></span> <span data-ttu-id="128a5-161">O formato e o conteúdo dessa parte são definidos pelo driver do codec.</span><span class="sxs-lookup"><span data-stu-id="128a5-161">The format and content of this chunk are defined by the codec driver.</span></span> <span data-ttu-id="128a5-162">Normalmente, os drivers usam essas informações para configuração.</span><span class="sxs-lookup"><span data-stu-id="128a5-162">Typically, drivers use this information for configuration.</span></span> <span data-ttu-id="128a5-163">Os aplicativos que lêem e gravam arquivos AVI não precisam interpretar essas informações; Eles a transferem de forma simples para e do driver como um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="128a5-163">Applications that read and write AVI files do not need to interpret this information; they simple transfer it to and from the driver as a memory block.</span></span>

<span data-ttu-id="128a5-164">O bloco ' strn ' opcional contém uma cadeia de caracteres de texto terminada em nulo que descreve o fluxo.</span><span class="sxs-lookup"><span data-stu-id="128a5-164">The optional 'strn' chunk contains a null-terminated text string describing the stream.</span></span>

<span data-ttu-id="128a5-165">Os cabeçalhos de fluxo na lista ' hdrl ' são associados aos dados de fluxo na lista ' movi ' de acordo com a ordem das partes ' strl '.</span><span class="sxs-lookup"><span data-stu-id="128a5-165">The stream headers in the 'hdrl' list are associated with the stream data in the 'movi' list according to the order of the 'strl' chunks.</span></span> <span data-ttu-id="128a5-166">O primeiro bloco ' strl ' se aplica ao fluxo 0, o segundo se aplica ao fluxo 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="128a5-166">The first 'strl' chunk applies to stream 0, the second applies to stream 1, and so forth.</span></span>

## <a name="stream-data-movi-list"></a><span data-ttu-id="128a5-167">Dados de fluxo (lista ' movi ')</span><span class="sxs-lookup"><span data-stu-id="128a5-167">Stream Data ('movi' List)</span></span>

<span data-ttu-id="128a5-168">Seguir as informações de cabeçalho é uma lista ' movi ' que contém os dados reais nos fluxos, ou seja, os quadros de vídeo e amostras de áudio.</span><span class="sxs-lookup"><span data-stu-id="128a5-168">Following the header information is a 'movi' list that contains the actual data in the streams—that is, the video frames and audio samples.</span></span> <span data-ttu-id="128a5-169">As partes de dados podem residir diretamente na lista ' movi ' ou podem ser agrupadas em listas de ' Rec '.</span><span class="sxs-lookup"><span data-stu-id="128a5-169">The data chunks can reside directly in the 'movi' list, or they might be grouped within 'rec ' lists.</span></span> <span data-ttu-id="128a5-170">O agrupamento ' Rec ' implica que as partes agrupadas devem ser lidas do disco de uma só vez e destinam-se a arquivos intercalados para reprodução a partir do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="128a5-170">The 'rec ' grouping implies that the grouped chunks should be read from disk all at once, and is intended for files that are interleaved to play from CD-ROM.</span></span>

<span data-ttu-id="128a5-171">O FOURCC que identifica cada parte de dados consiste em um número de fluxo de dois dígitos seguido por um código de dois caracteres que define o tipo de informação na parte.</span><span class="sxs-lookup"><span data-stu-id="128a5-171">The FOURCC that identifies each data chunk consists of a two-digit stream number followed by a two-character code that defines the type of information in the chunk.</span></span>



| <span data-ttu-id="128a5-172">Código de dois caracteres</span><span class="sxs-lookup"><span data-stu-id="128a5-172">Two-character code</span></span> | <span data-ttu-id="128a5-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="128a5-173">Description</span></span>              |
|--------------------|--------------------------|
| <span data-ttu-id="128a5-174">db</span><span class="sxs-lookup"><span data-stu-id="128a5-174">db</span></span>                 | <span data-ttu-id="128a5-175">Quadro de vídeo descompactado</span><span class="sxs-lookup"><span data-stu-id="128a5-175">Uncompressed video frame</span></span> |
| <span data-ttu-id="128a5-176">dc</span><span class="sxs-lookup"><span data-stu-id="128a5-176">dc</span></span>                 | <span data-ttu-id="128a5-177">Quadro de vídeo compactado</span><span class="sxs-lookup"><span data-stu-id="128a5-177">Compressed video frame</span></span>   |
| <span data-ttu-id="128a5-178">pc</span><span class="sxs-lookup"><span data-stu-id="128a5-178">pc</span></span>                 | <span data-ttu-id="128a5-179">Alteração da paleta</span><span class="sxs-lookup"><span data-stu-id="128a5-179">Palette change</span></span>           |
| <span data-ttu-id="128a5-180">WB</span><span class="sxs-lookup"><span data-stu-id="128a5-180">wb</span></span>                 | <span data-ttu-id="128a5-181">Dados de áudio</span><span class="sxs-lookup"><span data-stu-id="128a5-181">Audio data</span></span>               |



 

<span data-ttu-id="128a5-182">Por exemplo, se o fluxo 0 contiver áudio, as partes de dados desse fluxo teriam o FOURCC ' 00wb '.</span><span class="sxs-lookup"><span data-stu-id="128a5-182">For example, if stream 0 contains audio, the data chunks for that stream would have the FOURCC '00wb'.</span></span> <span data-ttu-id="128a5-183">Se o fluxo 1 contiver vídeo, as partes de dados desse fluxo teriam o FOURCC ' 01dB ' ou ' 01dc '.</span><span class="sxs-lookup"><span data-stu-id="128a5-183">If stream 1 contains video, the data chunks for that stream would have the FOURCC '01db' or '01dc'.</span></span> <span data-ttu-id="128a5-184">As partes de dados de vídeo também podem definir novas entradas de paleta para atualizar a paleta durante uma sequência AVI.</span><span class="sxs-lookup"><span data-stu-id="128a5-184">Video data chunks can also define new palette entries to update the palette during an AVI sequence.</span></span> <span data-ttu-id="128a5-185">Cada bloco de alteração de paleta (' xxpc ') contém uma estrutura [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) .</span><span class="sxs-lookup"><span data-stu-id="128a5-185">Each palette-change chunk ('xxpc') contains an [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) structure.</span></span> <span data-ttu-id="128a5-186">Se um fluxo contiver alterações de paleta, defina o sinalizador **AVISF de \_ vídeo \_ PALCHANGES** no membro **dwFlags** da estrutura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="128a5-186">If a stream contains palette changes, set the **AVISF\_VIDEO\_PALCHANGES** flag in the **dwFlags** member of the [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure for that stream.</span></span>

<span data-ttu-id="128a5-187">Os fluxos de texto podem usar códigos de dois caracteres arbitrários.</span><span class="sxs-lookup"><span data-stu-id="128a5-187">Text streams can use arbitrary two-character codes.</span></span>

## <a name="avi-index-entries"></a><span data-ttu-id="128a5-188">Entradas de índice AVI</span><span class="sxs-lookup"><span data-stu-id="128a5-188">AVI Index Entries</span></span>

<dl> <dt>

<span data-ttu-id="128a5-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Índice AVI 1,0</span><span class="sxs-lookup"><span data-stu-id="128a5-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 index</span></span>
</dt> <dd>

<span data-ttu-id="128a5-190">Um bloco de índice (' idx1 ') opcional pode seguir a lista ' movi '.</span><span class="sxs-lookup"><span data-stu-id="128a5-190">An optional index ('idx1') chunk can follow the 'movi' list.</span></span> <span data-ttu-id="128a5-191">O índice contém uma lista de partes de dados e sua localização no arquivo.</span><span class="sxs-lookup"><span data-stu-id="128a5-191">The index contains a list of the data chunks and their location in the file.</span></span> <span data-ttu-id="128a5-192">Ele consiste em uma estrutura [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) com entradas para cada parte de dados, incluindo partes ' Rec '.</span><span class="sxs-lookup"><span data-stu-id="128a5-192">It consists of an [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) structure with entries for each data chunk, including 'rec ' chunks.</span></span> <span data-ttu-id="128a5-193">Se o arquivo contiver um índice, defina o sinalizador **AVIF \_ HASINDEX** no membro **dwFlags** da estrutura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="128a5-193">If the file contains an index, set the **AVIF\_HASINDEX** flag in the **dwFlags** member of the [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="128a5-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Índice AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="128a5-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 index</span></span>
</dt> <dd>

<span data-ttu-id="128a5-195">Um índice AVI 2,0 pode aparecer como uma única parte.</span><span class="sxs-lookup"><span data-stu-id="128a5-195">An AVI 2.0 index can appear as a single chunk.</span></span> <span data-ttu-id="128a5-196">Como alternativa, os segmentos de índice podem ser intercalados na parte ' movi '.</span><span class="sxs-lookup"><span data-stu-id="128a5-196">Alternatively, index segments can be interleaved within the 'movi' chunk.</span></span> <span data-ttu-id="128a5-197">Se os segmentos de índice forem colocados na parte ' movi ', um superíndice conterá um índice dos segmentos de índice.</span><span class="sxs-lookup"><span data-stu-id="128a5-197">If the index segments are placed in the 'movi' chunk, a super index contains an index of the index segments.</span></span> <span data-ttu-id="128a5-198">A estrutura [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) é a estrutura base para os segmentos de índice e o superindex.</span><span class="sxs-lookup"><span data-stu-id="128a5-198">The [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) structure is the base structure for both the index segments and the super index.</span></span> <span data-ttu-id="128a5-199">Para obter mais informações, consulte as *extensões de formato de arquivo AVI OpenDML*, publicadas pelo Subcomitê de formato de arquivo AVI M-JPEG OpenDML.</span><span class="sxs-lookup"><span data-stu-id="128a5-199">For more information, see the *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span> <span data-ttu-id="128a5-200">(Esse recurso pode não estar disponível em alguns idiomas e países.)</span><span class="sxs-lookup"><span data-stu-id="128a5-200">(This resource may not be available in some languages and countries.)</span></span>

</dd> </dl>

## <a name="other-data-chunks"></a><span data-ttu-id="128a5-201">Outras partes de dados</span><span class="sxs-lookup"><span data-stu-id="128a5-201">Other Data Chunks</span></span>

<span data-ttu-id="128a5-202">Os dados podem ser alinhados em um arquivo AVI inserindo partes "lixo eletrônico" conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="128a5-202">Data can be aligned in an AVI file by inserting 'JUNK' chunks as needed.</span></span> <span data-ttu-id="128a5-203">Os aplicativos devem ignorar o conteúdo de uma parte ' lixo '.</span><span class="sxs-lookup"><span data-stu-id="128a5-203">Applications should ignore the contents of a 'JUNK' chunk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="128a5-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="128a5-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="128a5-205">Formato de arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="128a5-205">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
