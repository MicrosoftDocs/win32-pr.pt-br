---
description: Esta visão geral descreve o formato de arquivo de intercâmbio de recursos (RIFF), que é usado em arquivos. wav. O RIFF é o formato típico do qual os dados de áudio para XAudio2 serão carregados.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: RIFF (Resource Interchange File Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772495"
---
# <a name="resource-interchange-file-format-riff"></a><span data-ttu-id="388a9-104">RIFF (Resource Interchange File Format)</span><span class="sxs-lookup"><span data-stu-id="388a9-104">Resource Interchange File Format (RIFF)</span></span>

<span data-ttu-id="388a9-105">Esta visão geral descreve o formato de arquivo de intercâmbio de recursos (RIFF), que é usado em arquivos. wav.</span><span class="sxs-lookup"><span data-stu-id="388a9-105">This overview describes the Resource Interchange File Format (RIFF), which is used in .wav files.</span></span> <span data-ttu-id="388a9-106">O RIFF é o formato típico do qual os dados de áudio para XAudio2 serão carregados.</span><span class="sxs-lookup"><span data-stu-id="388a9-106">RIFF is the typical format from which audio data for XAudio2 will be loaded.</span></span>

## <a name="riff"></a><span data-ttu-id="388a9-107">RIFF</span><span class="sxs-lookup"><span data-stu-id="388a9-107">RIFF</span></span>

<span data-ttu-id="388a9-108">Um arquivo RIFF é composto por várias seções discretas de dados chamada *partes*.</span><span class="sxs-lookup"><span data-stu-id="388a9-108">A RIFF file is composed of multiple discrete sections of data called *chunks*.</span></span>

## <a name="fourcc-identifiers"></a><span data-ttu-id="388a9-109">Identificadores FOURCC</span><span class="sxs-lookup"><span data-stu-id="388a9-109">FOURCC Identifiers</span></span>

<span data-ttu-id="388a9-110">O tipo de dados em uma parte é indicado por um identificador de código de quatro caracteres (FOURCC).</span><span class="sxs-lookup"><span data-stu-id="388a9-110">The type of data in a chunk is indicated by a four-character code (FOURCC) identifier.</span></span> <span data-ttu-id="388a9-111">Um FOURCC é um inteiro sem sinal de 32 bits criado pela concatenação de quatro caracteres ASCII usados para identificar tipos de bloco em um arquivo RIFF.</span><span class="sxs-lookup"><span data-stu-id="388a9-111">A FOURCC is a 32-bit unsigned integer created by concatenating four ASCII characters used to identify chunk types in a RIFF file.</span></span> <span data-ttu-id="388a9-112">Por exemplo, o "abcd" FOURCC é representado em um sistema little-endian como 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="388a9-112">For example, the FOURCC "abcd" is represented on a little-endian system as 0x64636261.</span></span> <span data-ttu-id="388a9-113">Os FOURCCs podem conter caracteres de espaço, portanto, "ABC" é um FOURCC válido.</span><span class="sxs-lookup"><span data-stu-id="388a9-113">FOURCCs can contain space characters, so " abc" is a valid FOURCC.</span></span> <span data-ttu-id="388a9-114">Os arquivos de áudio usam códigos FOURCC para identificar partes de formato de áudio, partes de dados de áudio e quaisquer outras partes específicas do formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="388a9-114">Audio files use FOURCC codes to identify audio format chunks, audio data chunks, and any other chunks specific to the audio format.</span></span>

<span data-ttu-id="388a9-115">A tabela a seguir mostra os identificadores FOURCC que podem ser esperados nos formatos de áudio com suporte do XAudio2.</span><span class="sxs-lookup"><span data-stu-id="388a9-115">The following table shows the FOURCC identifiers that can be expected in the audio formats supported by XAudio2.</span></span> 

| <span data-ttu-id="388a9-116">Formatar</span><span class="sxs-lookup"><span data-stu-id="388a9-116">Format</span></span> | <span data-ttu-id="388a9-117">Identificadores FOURCC</span><span class="sxs-lookup"><span data-stu-id="388a9-117">FOURCC identifiers</span></span>                     | <span data-ttu-id="388a9-118">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="388a9-118">Additional information</span></span>                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="388a9-119">PCM</span><span class="sxs-lookup"><span data-stu-id="388a9-119">PCM</span></span>    | <span data-ttu-id="388a9-120">"RIFF", "fmt", "dados"</span><span class="sxs-lookup"><span data-stu-id="388a9-120">"RIFF", "fmt" , "data"</span></span>                 |                                                                                                      |
| <span data-ttu-id="388a9-121">ADPCM</span><span class="sxs-lookup"><span data-stu-id="388a9-121">ADPCM</span></span>  | <span data-ttu-id="388a9-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span><span class="sxs-lookup"><span data-stu-id="388a9-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span></span> | <span data-ttu-id="388a9-123">Consulte [visão geral de ADPCM](adpcm-overview.md) para obter uma descrição dos identificadores FOURCC específicos de ADPCM.</span><span class="sxs-lookup"><span data-stu-id="388a9-123">See [ADPCM Overview](adpcm-overview.md) for a description of the ADPCM-specific FOURCC identifiers.</span></span> |



 

<span data-ttu-id="388a9-124">Os identificadores FOURCC "RIFF", "fmt" e "data" são comuns a todos os formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="388a9-124">The FOURCC identifiers "RIFF", "fmt", and "data" are common to all of the supported formats.</span></span> <span data-ttu-id="388a9-125">A tabela a seguir descreve os identificadores FOURCC que são encontrados em todos os formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="388a9-125">The following table describes the FOURCC identifiers that are found in all of the supported formats.</span></span> 

| <span data-ttu-id="388a9-126">Identificador FOURCC</span><span class="sxs-lookup"><span data-stu-id="388a9-126">FOURCC identifier</span></span> | <span data-ttu-id="388a9-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="388a9-127">Description</span></span>                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="388a9-128">"RIFF"</span><span class="sxs-lookup"><span data-stu-id="388a9-128">"RIFF"</span></span>            | <span data-ttu-id="388a9-129">A parte padrão do RIFF que contém um tipo de arquivo com o valor de "WAVE" ou "XWMA" nos primeiros quatro bytes de sua seção de dados e as outras partes no arquivo no restante de sua seção de dados.</span><span class="sxs-lookup"><span data-stu-id="388a9-129">Standard RIFF chunk containing a file type with the value of "WAVE" or "XWMA" in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                   |
| <span data-ttu-id="388a9-130">"fmt"</span><span class="sxs-lookup"><span data-stu-id="388a9-130">"fmt"</span></span>             | <span data-ttu-id="388a9-131">Contém o cabeçalho de formato do arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="388a9-131">Contains the format header for the audio file.</span></span> <span data-ttu-id="388a9-132">Os dados nessa parte correspondem a uma das seguintes estruturas: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span><span class="sxs-lookup"><span data-stu-id="388a9-132">The data in this chunk corresponds to one of the following structures: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span></span>                                                  |
| <span data-ttu-id="388a9-133">"data"</span><span class="sxs-lookup"><span data-stu-id="388a9-133">"data"</span></span>            | <span data-ttu-id="388a9-134">Contém dados de áudio para o arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="388a9-134">Contains audio data for the audio file.</span></span> <span data-ttu-id="388a9-135">No XAudio2, o conteúdo da parte de dados será lido em um buffer e passado para uma voz de origem como o membro **pAudioData** de uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="388a9-135">In XAudio2, the contents of the data chunk will be read into a buffer and passed to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> |



 

## <a name="chunks"></a><span data-ttu-id="388a9-136">Chunks</span><span class="sxs-lookup"><span data-stu-id="388a9-136">Chunks</span></span>

<span data-ttu-id="388a9-137">Um arquivo RIFF consiste em uma parte de RIFF que contém zero ou mais partes.</span><span class="sxs-lookup"><span data-stu-id="388a9-137">A RIFF file consists of a RIFF chunk containing zero or more other chunks.</span></span>

-   <span data-ttu-id="388a9-138">A parte do RIFF tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="388a9-138">The RIFF chunk has the following form:</span></span>

    <span data-ttu-id="388a9-139">"RIFF", fileSize, fileType, dados</span><span class="sxs-lookup"><span data-stu-id="388a9-139">"RIFF", fileSize, fileType, data</span></span>

    <span data-ttu-id="388a9-140">Onde "RIFF" é o código FOURCC literal "RIFF", *fileSize* é um valor de 4 bytes fornecendo o tamanho dos dados no arquivo e *FILETYPE* é um FOURCC que identifica o tipo de arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="388a9-140">Where "RIFF" is the literal FOURCC code "RIFF", *fileSize* is a 4-byte value giving the size of the data in the file, and *fileType* is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="388a9-141">O valor de *fileSize* inclui o tamanho de *filetype* FOURCC mais o tamanho dos dados a seguir, mas não inclui o tamanho de "riff" FOURCC ou o tamanho de *fileSize*.</span><span class="sxs-lookup"><span data-stu-id="388a9-141">The value of *fileSize* includes the size of *fileType* FOURCC plus the size of the data that follows, but does not include the size of the "RIFF" FOURCC or the size of *fileSize*.</span></span> <span data-ttu-id="388a9-142">Os dados consistem em partes em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="388a9-142">The data consists of chunks in any order.</span></span>

-   <span data-ttu-id="388a9-143">Outras partes têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="388a9-143">Other chunks have the following form:</span></span>

    ```
    chunkID, chunkSize, data
    ```

    

    <span data-ttu-id="388a9-144">Em que *chunkid* é um FOURCC que identifica os dados contidos na parte, *ChunkSize* é um valor de 4 bytes fornecendo o tamanho da seção de dados da parte e os dados são zero ou mais bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="388a9-144">Where *chunkID* is a FOURCC that identifies the data contained in the chunk, *chunkSize* is a 4-byte value giving the size of the data section of the chunk, and data is zero or more bytes of data.</span></span> <span data-ttu-id="388a9-145">Os dados são sempre preenchidos para o limite de palavras mais próximo.</span><span class="sxs-lookup"><span data-stu-id="388a9-145">The data is always padded to the nearest WORD boundary.</span></span> <span data-ttu-id="388a9-146">*ChunkSize* fornece o tamanho dos dados válidos na parte.</span><span class="sxs-lookup"><span data-stu-id="388a9-146">*chunkSize* gives the size of the valid data in the chunk.</span></span> <span data-ttu-id="388a9-147">Ele não inclui o preenchimento, o tamanho de *chunkid* ou o tamanho de *ChunkSize*.</span><span class="sxs-lookup"><span data-stu-id="388a9-147">It does not include the padding, the size of *chunkID*, or the size of *chunkSize*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="388a9-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="388a9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="388a9-149">Introdução</span><span class="sxs-lookup"><span data-stu-id="388a9-149">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="388a9-150">Como: Reproduzir um som com o XAudio2</span><span class="sxs-lookup"><span data-stu-id="388a9-150">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="388a9-151">Referência de programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="388a9-151">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 



