---
title: Implementando DoProcessOutput
description: Implementando DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, DoProcessOutput
- Plug-ins do DSP, DoProcessOutput
- plug-ins do DSP de áudio, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364109"
---
# <a name="implementing-doprocessoutput"></a><span data-ttu-id="b1797-108">Implementando DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="b1797-108">Implementing DoProcessOutput</span></span>

<span data-ttu-id="b1797-109">Para processar dados de áudio, você precisará executar várias etapas em **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="b1797-109">To process audio data, you'll need to perform several steps in **DoProcessOutput**.</span></span> <span data-ttu-id="b1797-110">As etapas a seguir usam o código de exemplo do assistente de plug-in como exemplos.</span><span class="sxs-lookup"><span data-stu-id="b1797-110">The following steps use the plug-in wizard sample code as examples.</span></span> <span data-ttu-id="b1797-111">Se você quiser criar um plug-in de DSP de áudio que processa o conteúdo de mídia do mesmo tipo que o código de exemplo do assistente de plug-in, você só precisará alterar o código de processamento real mencionado na etapa 6.</span><span class="sxs-lookup"><span data-stu-id="b1797-111">If you want to create an audio DSP plug-in that processes media content of the same type that the plug-in wizard sample code does, you'll only need to change the actual processing code referred to in step 6.</span></span> <span data-ttu-id="b1797-112">A seguir estão todas as etapas implementadas no **DoProcessOutput**:</span><span class="sxs-lookup"><span data-stu-id="b1797-112">Following are all the steps implemented in **DoProcessOutput**:</span></span>

-   <span data-ttu-id="b1797-113">Se o plug-in não estiver habilitado no momento, basta copiar os dados inalterados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="b1797-113">If the plug-in is not currently enabled, simply copy the data unchanged into the output buffer.</span></span> <span data-ttu-id="b1797-114">Se o seu plug-in converter os dados em um formato diferente, você também deverá fazer o processamento de conversão aqui.</span><span class="sxs-lookup"><span data-stu-id="b1797-114">If your plug-in converts the data into a different format, you must also do the conversion processing here.</span></span>

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   <span data-ttu-id="b1797-115">Recupere um ponteiro para a estrutura de formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="b1797-115">Retrieve a pointer to the input format structure.</span></span> <span data-ttu-id="b1797-116">Você precisará recuperar dados do membro dessa estrutura, portanto, copie o ponteiro de *m \_ mtInput*.**pbFormat** para uma variável de ponteiro local de um tipo que corresponde ao tipo de estrutura de formato.</span><span class="sxs-lookup"><span data-stu-id="b1797-116">You'll need to retrieve member data from this structure, so copy the pointer from *m\_mtInput*.**pbformat** to a local pointer variable of a type that matches the format structure type.</span></span> <span data-ttu-id="b1797-117">O exemplo a seguir armazena um ponteiro para uma estrutura de formato de entrada **WAVEFORMATEX** :</span><span class="sxs-lookup"><span data-stu-id="b1797-117">The following example stores a pointer to a **WAVEFORMATEX** input format structure:</span></span>

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   <span data-ttu-id="b1797-118">Calcule o número de amostras a serem processadas.</span><span class="sxs-lookup"><span data-stu-id="b1797-118">Calculate the number of samples to process.</span></span> <span data-ttu-id="b1797-119">O código de exemplo gerado pelo assistente de plug-in executa essa etapa dividindo o número de bytes a serem processados pelo membro **nBlockAlign** da estrutura de formato de entrada WAVEFORMATEX e, em seguida, multiplicando o resultado pelo número de canais, que foi armazenado no membro **nChannels** .</span><span class="sxs-lookup"><span data-stu-id="b1797-119">The sample code that the plug-in wizard generates performs this step by dividing the number of bytes to process by the **nBlockAlign** member of the WAVEFORMATEX input format structure, and then multiplying the result by the number of channels, which was stored in the **nChannels** member.</span></span> <span data-ttu-id="b1797-120">O exemplo a seguir é do código de exemplo do assistente de plug-in:</span><span class="sxs-lookup"><span data-stu-id="b1797-120">The following example is from the plug-in wizard sample code:</span></span>

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  <span data-ttu-id="b1797-121">Determine a profundidade de bits do áudio.</span><span class="sxs-lookup"><span data-stu-id="b1797-121">Determine the bit depth of the audio.</span></span> <span data-ttu-id="b1797-122">O código de exemplo do assistente de plug-in determina o áudio de 8 ou 16 bits inspecionando o membro **wBitsPerSample** da estrutura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b1797-122">The plug-in wizard sample code determines 8-bit or 16-bit audio by inspecting the **wBitsPerSample** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="b1797-123">Em seguida, ele usa esse valor em uma instrução switch para fornecer rotinas de processamento separadas para cada profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="b1797-123">It then uses that value in a switch statement to provide separate processing routines for each bit depth.</span></span> <span data-ttu-id="b1797-124">Talvez seja necessário usar uma técnica diferente ao lidar com outros tipos de formato e profundidades de bits.</span><span class="sxs-lookup"><span data-stu-id="b1797-124">You may need to use a different technique when dealing with other format types and bit depths.</span></span>
    2.  <span data-ttu-id="b1797-125">Crie um loop para percorrer os exemplos de áudio no buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b1797-125">Create a loop to step through the audio samples in the input buffer.</span></span>
    3.  <span data-ttu-id="b1797-126">Recupere um exemplo do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b1797-126">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="b1797-127">Você faz isso desreferenciando o ponteiro de dados de entrada e armazenando o resultado em uma variável do tipo int. Para áudio de 16 bits, você deve reconverter o ponteiro de BYTE para um ponteiro curto para lidar com a precisão de amostra de áudio maior.</span><span class="sxs-lookup"><span data-stu-id="b1797-127">You do this by dereferencing the input data pointer and storing the result in a variable of type int. For 16-bit audio, you must recast the BYTE pointer to a short pointer to handle the greater audio sample precision.</span></span> <span data-ttu-id="b1797-128">Quando tiver o valor, você poderá incrementar imediatamente o ponteiro *pbInputData* para que ele aponte para o próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="b1797-128">Once you have the value, you can immediately increment the *pbInputData* pointer so that it points to the next sample.</span></span> <span data-ttu-id="b1797-129">Os exemplos a seguir demonstram isso:</span><span class="sxs-lookup"><span data-stu-id="b1797-129">The following examples demonstrate this:</span></span>

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    <span data-ttu-id="b1797-130">– ou –</span><span class="sxs-lookup"><span data-stu-id="b1797-130">-or-</span></span>

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  <span data-ttu-id="b1797-131">Execute o processamento.</span><span class="sxs-lookup"><span data-stu-id="b1797-131">Perform the processing.</span></span> <span data-ttu-id="b1797-132">É aqui que você aplica os algoritmos que alteram o exemplo de alguma forma.</span><span class="sxs-lookup"><span data-stu-id="b1797-132">This is where you apply the algorithms that change the sample somehow.</span></span> <span data-ttu-id="b1797-133">O que você faz aqui é para você.</span><span class="sxs-lookup"><span data-stu-id="b1797-133">What you do here is up to you.</span></span>
    2.  <span data-ttu-id="b1797-134">Grave os dados processados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="b1797-134">Write the processed data to the output buffer.</span></span> <span data-ttu-id="b1797-135">Incrementar imediatamente o ponteiro para o buffer de saída, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b1797-135">Immediately increment the pointer to the output buffer, as in the following example:</span></span>

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  <span data-ttu-id="b1797-136">Repita o loop até que todos os exemplos tenham sido processados.</span><span class="sxs-lookup"><span data-stu-id="b1797-136">Repeat the loop until all the samples have been processed.</span></span>
    2.  <span data-ttu-id="b1797-137">Retornar um **HRESULT** apropriado.</span><span class="sxs-lookup"><span data-stu-id="b1797-137">Return an appropriate **HRESULT**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1797-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1797-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1797-139">**Implementando um plug-in do DSP de áudio**</span><span class="sxs-lookup"><span data-stu-id="b1797-139">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




