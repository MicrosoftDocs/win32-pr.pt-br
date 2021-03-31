---
title: Criando o efeito de eco
description: Criando o efeito de eco
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in de eco do DSP, criando efeito de eco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004956"
---
# <a name="creating-the-echo-effect"></a><span data-ttu-id="1ad9f-109">Criando o efeito de eco</span><span class="sxs-lookup"><span data-stu-id="1ad9f-109">Creating the Echo Effect</span></span>

<span data-ttu-id="1ad9f-110">Primeiro, você deve remover o código do exemplo de assistente que dimensiona o áudio.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-110">You must first remove the code from the wizard sample that scales the audio.</span></span> <span data-ttu-id="1ad9f-111">Na seção de 8 bits, remova o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-111">From the 8-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="1ad9f-112">(Lembre-se de que m \_ fScaleFactor foi substituído por m \_ dwDelayTime.)</span><span class="sxs-lookup"><span data-stu-id="1ad9f-112">(Remember that m\_fScaleFactor was replaced by m\_dwDelayTime.)</span></span>

<span data-ttu-id="1ad9f-113">Na seção de 16 bits, remova o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-113">From the 16-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="1ad9f-114">A implementação de **DoProcessOutput** fornecida pelo código de exemplo do assistente de plug-in cria um loop while que itera uma vez para cada amostra no buffer de entrada fornecido pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-114">The implementation of **DoProcessOutput** provided by the plug-in wizard sample code creates a while loop that iterates one time for each sample in the input buffer provided by Windows Media Player.</span></span> <span data-ttu-id="1ad9f-115">Esse loop funciona da mesma maneira para áudio de 8 e 16 bits, embora um loop separado seja necessário para cada um.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-115">This loop works the same way for both 8-bit and 16-bit audio, although a separate loop is required for each.</span></span> <span data-ttu-id="1ad9f-116">Em cada caso, o loop é iniciado com o teste a seguir:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-116">In each case, the loop initiates with the following test:</span></span>


```C++
while (dwSamplesToProcess--)

```



<span data-ttu-id="1ad9f-117">Uma vez dentro do loop, as rotinas de processamento são muito semelhantes para áudio de 8 e 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-117">Once inside the loop, the processing routines are very similar for 8-bit and 16-bit audio.</span></span> <span data-ttu-id="1ad9f-118">A principal diferença é que o código na seção de 8 bits altera o intervalo de valores de dados para-128 até 127 e, em seguida, converte o intervalo novamente antes de gravar os dados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-118">The main difference is that the code in the 8-bit section changes the range of data values to -128 through 127, and then converts the range back again before writing the data to the output buffer.</span></span> <span data-ttu-id="1ad9f-119">Isso é importante para manter a simetria da onda de áudio durante o processamento.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-119">This is important to retain the symmetry of the audio waveform during processing.</span></span>

<span data-ttu-id="1ad9f-120">Agora você pode começar a adicionar e substituir o código no loop de processamento.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-120">Now you can begin to add and replace code in the processing loop.</span></span>

## <a name="retrieve-a-sample-from-the-input-buffer"></a><span data-ttu-id="1ad9f-121">Recuperar um exemplo do buffer de entrada</span><span class="sxs-lookup"><span data-stu-id="1ad9f-121">Retrieve a Sample from the Input Buffer</span></span>

<span data-ttu-id="1ad9f-122">Durante cada iteração do loop, um único exemplo é recuperado do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-122">During each iteration of the loop, a single sample is retrieved from the input buffer.</span></span> <span data-ttu-id="1ad9f-123">Para áudio de 8 bits, o exemplo é deslocado para o novo intervalo e, em seguida, o ponteiro para o buffer de entrada é avançado para o próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-123">For 8-bit audio, the sample is shifted into the new range, and then the pointer to the input buffer is advanced to the next sample.</span></span> <span data-ttu-id="1ad9f-124">O código a seguir é do assistente de plug-in:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-124">The following code is from the plug-in wizard:</span></span>


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



<span data-ttu-id="1ad9f-125">Para áudio de 16 bits, o processo é o mesmo, exceto para a normalização:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-125">For 16-bit audio, the process is the same except for the normalization:</span></span>


```C++
// Get the input sample.
int i = *pwInputData++;

```



<span data-ttu-id="1ad9f-126">Lembre-se de que os ponteiros no código de 16 bits foram convertidos em tipo **curto**.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-126">Remember that the pointers in the 16-bit code have been converted to type **short**.</span></span>

## <a name="retrieve-a-sample-from-the-delay-buffer"></a><span data-ttu-id="1ad9f-127">Recuperar um exemplo do buffer de atraso</span><span class="sxs-lookup"><span data-stu-id="1ad9f-127">Retrieve a Sample from the Delay Buffer</span></span>

<span data-ttu-id="1ad9f-128">Em seguida, recupere um único exemplo do buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-128">Next, retrieve a single sample from the delay buffer.</span></span> <span data-ttu-id="1ad9f-129">Para o código de 8 bits, os exemplos de atraso são armazenados em seu intervalo nativo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-129">For 8-bit code, the delay samples are stored in their native range of 0 to 255.</span></span> <span data-ttu-id="1ad9f-130">O código a seguir, que você deve adicionar, recupera um exemplo de atraso de 8 bits:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-130">The following code, which you must add, retrieves an 8-bit delay sample:</span></span>


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



<span data-ttu-id="1ad9f-131">Para áudio de 16 bits, o processo é semelhante:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-131">For 16-bit audio, the process is similar:</span></span>


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a><span data-ttu-id="1ad9f-132">Gravar a amostra de entrada no buffer de atraso</span><span class="sxs-lookup"><span data-stu-id="1ad9f-132">Write the Input Sample to the Delay Buffer</span></span>

<span data-ttu-id="1ad9f-133">Agora, você deve armazenar o exemplo de entrada no buffer de atraso no mesmo local do qual você recuperou o exemplo de atraso.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-133">Now, you must store the input sample in the delay buffer in the same location from which you retrieved the delay sample.</span></span> <span data-ttu-id="1ad9f-134">Este é o código que você deve adicionar para áudio de 8 bits:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-134">The following is the code you must add for 8-bit audio:</span></span>


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



<span data-ttu-id="1ad9f-135">Este é o código a ser adicionado para a seção de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-135">This is the code to add for the 16-bit section:</span></span>


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a><span data-ttu-id="1ad9f-136">Mover o ponteiro de buffer de atraso</span><span class="sxs-lookup"><span data-stu-id="1ad9f-136">Move the Delay Buffer Pointer</span></span>

<span data-ttu-id="1ad9f-137">Agora que o trabalho no buffer de atrasos foi concluído para essa iteração, você pode avançar o ponteiro móvel para o buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-137">Now that the work in the delay buffer is finished for this iteration, you can advance the movable pointer to the delay buffer.</span></span> <span data-ttu-id="1ad9f-138">Se o ponteiro atingir o final do buffer circular, você deverá alterar seu valor para apontar para o cabeçalho do buffer.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-138">If the pointer reaches the end of the circular buffer, you must change its value to point to the head of the buffer.</span></span> <span data-ttu-id="1ad9f-139">Para fazer isso para áudio de 8 bits, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-139">To do this for 8-bit audio, use the following code:</span></span>


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



<span data-ttu-id="1ad9f-140">Este é o código para a seção de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-140">Here is the code for the 16-bit section:</span></span>


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



<span data-ttu-id="1ad9f-141">Como o ponteiro na seção de 16 bits é realmente uma cópia da variável de membro, você deve se lembrar de atualizar o valor na variável de membro com o novo endereço.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-141">Since the pointer in the 16-bit section is really a copy of the member variable, you must remember to update the value in the member variable with the new address.</span></span> <span data-ttu-id="1ad9f-142">Se você não conseguir fazer isso, o ponteiro de buffer de atraso apontará para o cabeçalho do buffer repetidamente e o efeito de eco não funcionará conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-142">If you fail to do this, the delay buffer pointer will point to the head of the buffer repeatedly and your echo effect will not work as expected.</span></span> <span data-ttu-id="1ad9f-143">Adicione o seguinte código à seção de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-143">Add the following code to the 16-bit section:</span></span>


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a><span data-ttu-id="1ad9f-144">Misturar o exemplo de entrada com a amostra de atraso</span><span class="sxs-lookup"><span data-stu-id="1ad9f-144">Mix the Input Sample with the Delay Sample</span></span>

<span data-ttu-id="1ad9f-145">É aqui que você usa os valores de mistura úmida e seca de misturas para criar o exemplo de saída final.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-145">This is where you use the wet mix and dry mix values to create the final output sample.</span></span> <span data-ttu-id="1ad9f-146">Basta multiplicar cada amostra pelo valor de ponto flutuante que representa a porcentagem do sinal final para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-146">You simply multiply each sample by the floating-point value that represents the percentage of the final signal for the sample.</span></span> <span data-ttu-id="1ad9f-147">Multiplique a amostra de entrada pelo valor armazenado em m \_ fDryMix; multiplique a amostra de atraso pelo valor armazenado em m \_ fWetMix.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-147">Multiply the input sample by the value stored in m\_fDryMix; multiply the delay sample by the value stored in m\_fWetMix.</span></span> <span data-ttu-id="1ad9f-148">Em seguida, adicione os dois valores.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-148">Then, add the two values.</span></span> <span data-ttu-id="1ad9f-149">O código que você deve adicionar é idêntico para as seções de 8 e 16 bits:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-149">The code you must add is identical for the 8-bit and 16-bit sections:</span></span>


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a><span data-ttu-id="1ad9f-150">Gravar os dados no buffer de saída</span><span class="sxs-lookup"><span data-stu-id="1ad9f-150">Write the Data to the Output Buffer</span></span>

<span data-ttu-id="1ad9f-151">Por fim, copie o exemplo misto para o buffer de saída e, em seguida, avance o ponteiro de buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="1ad9f-151">Finally, copy the mixed sample to the output buffer, and then advance the output buffer pointer.</span></span> <span data-ttu-id="1ad9f-152">Para áudio de 8 bits, o assistente de plug-in usa o seguinte código para retornar o exemplo ao seu intervalo original:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-152">For 8-bit audio, the plug-in wizard uses the following code to return the sample to its original range:</span></span>


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



<span data-ttu-id="1ad9f-153">Para áudio de 16 bits, o assistente usa o seguinte código como a etapa final no loop de processamento:</span><span class="sxs-lookup"><span data-stu-id="1ad9f-153">For 16-bit audio, the wizard uses the following code as the final step in the processing loop:</span></span>


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a><span data-ttu-id="1ad9f-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ad9f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad9f-155">**Implementando CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="1ad9f-155">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




