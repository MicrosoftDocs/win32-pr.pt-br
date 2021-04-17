---
title: Processando os dados de áudio
description: Processando os dados de áudio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in do eco DSP, dados de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811636"
---
# <a name="processing-the-audio-data"></a><span data-ttu-id="94078-109">Processando os dados de áudio</span><span class="sxs-lookup"><span data-stu-id="94078-109">Processing the Audio Data</span></span>

<span data-ttu-id="94078-110">A implementação padrão de **DoProcessOutput** começa pela recuperação de um ponteiro para uma estrutura **WAVEFORMATEX** válida, exatamente como foi feita em **AllocateStreamingResources**.</span><span class="sxs-lookup"><span data-stu-id="94078-110">The default implementation of **DoProcessOutput** begins by retrieving a pointer to a valid **WAVEFORMATEX** structure, exactly like was done in **AllocateStreamingResources**.</span></span> <span data-ttu-id="94078-111">Em seguida, ele usa as informações nessa estrutura para calcular o número de amostras no buffer de entrada aguardando processamento.</span><span class="sxs-lookup"><span data-stu-id="94078-111">It then uses the information in that structure to calculate the number of samples in the input buffer waiting to be processed.</span></span> <span data-ttu-id="94078-112">O código a seguir é da implementação padrão:</span><span class="sxs-lookup"><span data-stu-id="94078-112">The following code is from the default implementation:</span></span>


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



<span data-ttu-id="94078-113">Em seguida, o código inspeciona o membro **wBitsPerSample** para determinar a profundidade de bits do áudio.</span><span class="sxs-lookup"><span data-stu-id="94078-113">Then, the code inspects the **wBitsPerSample** member to determine the bit depth of the audio.</span></span> <span data-ttu-id="94078-114">Esse valor é usado em uma instrução switch para fornecer processamento separado para áudio de 8 e 16 bits.</span><span class="sxs-lookup"><span data-stu-id="94078-114">This value is used in a switch statement to provide separate processing for 8-bit and 16-bit audio.</span></span>

## <a name="differences-between-8-bit-and-16-bit-audio"></a><span data-ttu-id="94078-115">Diferenças entre áudio de 8 e 16 bits</span><span class="sxs-lookup"><span data-stu-id="94078-115">Differences Between 8-bit and 16-bit Audio</span></span>

<span data-ttu-id="94078-116">Há diferenças importantes entre áudio de 8 e 16 bits.</span><span class="sxs-lookup"><span data-stu-id="94078-116">There are important differences between 8-bit and 16-bit audio.</span></span> <span data-ttu-id="94078-117">Portanto, as rotinas de processamento para criar o efeito de eco são diferentes.</span><span class="sxs-lookup"><span data-stu-id="94078-117">Therefore, the processing routines to create the echo effect are different.</span></span> <span data-ttu-id="94078-118">Os dois formatos diferem das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="94078-118">The two formats differ in the following ways:</span></span>

-   <span data-ttu-id="94078-119">Cada formato tem um tamanho de amostra diferente: amostras de 8 bits cada ocupam um byte de memória, enquanto os exemplos de 16 bits ocupam dois bytes.</span><span class="sxs-lookup"><span data-stu-id="94078-119">Each format has a different sample size: 8-bit samples each occupy one byte of memory, while 16-bit samples each occupy two bytes.</span></span>
-   <span data-ttu-id="94078-120">Cada formato representa a amplitude de áudio de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="94078-120">Each format represents the audio amplitude differently.</span></span> <span data-ttu-id="94078-121">o áudio de 8 bits é representado por um inteiro sem sinal com um intervalo de 0 a 255; um valor de 128 representa silêncio.</span><span class="sxs-lookup"><span data-stu-id="94078-121">8-bit audio is represented by an unsigned integer with a range from 0 to 255; a value of 128 represents silence.</span></span> <span data-ttu-id="94078-122">áudio de 16 bits é representado por um inteiro assinado com um intervalo de-32768 a 32767; um valor de zero representa silêncio.</span><span class="sxs-lookup"><span data-stu-id="94078-122">16-bit audio is represented by a signed integer with a range from -32768 to 32767; a value of zero represents silence.</span></span>

<span data-ttu-id="94078-123">Embora o processo de criação do efeito de eco seja fundamentalmente idêntico para cada formato, os detalhes devem ser ligeiramente diferentes.</span><span class="sxs-lookup"><span data-stu-id="94078-123">While the process of creating the echo effect is fundamentally identical for each format, the details must differ slightly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94078-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94078-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94078-125">**Implementando CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="94078-125">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




