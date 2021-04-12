---
title: Implementando IMediaObject AllocateStreamingResources
description: Implementando IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Plug-ins do Windows Media Player, recursos de streaming de amostra de eco
- plug-ins, amostras de eco de recursos de streaming
- plug-ins de processamento de sinal digital, Echo amostras de recursos de streaming
- Plug-ins do DSP, amostras de eco de recursos de streaming
- Exemplo de plug-in de eco do DSP, recursos de streaming
- Exemplo de plug-in do eco DSP, buffer de atraso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364129"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a><span data-ttu-id="07ba7-109">Implementando IMediaObject:: AllocateStreamingResources</span><span class="sxs-lookup"><span data-stu-id="07ba7-109">Implementing IMediaObject::AllocateStreamingResources</span></span>

<span data-ttu-id="07ba7-110">No exemplo de eco, o método **AllocateStreamingResources** cria o buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="07ba7-110">In the Echo sample, the **AllocateStreamingResources** method creates the delay buffer.</span></span> <span data-ttu-id="07ba7-111">Ele faz isso fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="07ba7-111">It does this by doing the following:</span></span>

1.  <span data-ttu-id="07ba7-112">Calculando um tamanho para o buffer que corresponde ao tempo de atraso especificado para o tipo de mídia fornecido.</span><span class="sxs-lookup"><span data-stu-id="07ba7-112">Calculating a size for the buffer that corresponds to the specified delay time for the given media type.</span></span>
2.  <span data-ttu-id="07ba7-113">Alocar uma nova memória ou realocar o tamanho do buffer se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="07ba7-113">Either allocating new memory or reallocating the buffer size if it already exists.</span></span>
3.  <span data-ttu-id="07ba7-114">Chamar um método que preenche o buffer com valores que representam silêncio.</span><span class="sxs-lookup"><span data-stu-id="07ba7-114">Calling a method that fills the buffer with values representing silence.</span></span>

<span data-ttu-id="07ba7-115">O valor de silêncio é diferente, dependendo da profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="07ba7-115">The value for silence is different depending upon the bit depth.</span></span> <span data-ttu-id="07ba7-116">Para áudio de 8 bits, o silêncio é representado pelo valor hexadecimal 80; para áudio de 16 bits, o silêncio é representado por zero.</span><span class="sxs-lookup"><span data-stu-id="07ba7-116">For 8-bit audio, silence is represented by the hex value 80; for 16-bit audio, silence is represented by zero.</span></span>

## <a name="calculating-the-delay-buffer-size"></a><span data-ttu-id="07ba7-117">Calculando o tamanho do buffer de atraso</span><span class="sxs-lookup"><span data-stu-id="07ba7-117">Calculating the Delay Buffer Size</span></span>

<span data-ttu-id="07ba7-118">Para calcular o tamanho necessário para o buffer de atraso, você deve primeiro recuperar uma estrutura **WAVEFORMATEX** que contém informações sobre os dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="07ba7-118">In order to calculate the size required for the delay buffer, you must first retrieve a **WAVEFORMATEX** structure that contains information about the audio data.</span></span> <span data-ttu-id="07ba7-119">O exemplo a seguir recupera um ponteiro para essa estrutura da estrutura **de \_ \_ tipo de mídia DMO** de entrada:</span><span class="sxs-lookup"><span data-stu-id="07ba7-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span></span>


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



<span data-ttu-id="07ba7-120">Depois de armazenar um ponteiro para a estrutura **WAVEFORMATEX** apropriada, você pode inspecionar seus membros e usá-los para calcular o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="07ba7-120">Once you have stored a pointer to the proper **WAVEFORMATEX** structure, you can inspect its members and use them to calculate the required buffer size.</span></span> <span data-ttu-id="07ba7-121">O exemplo de código a seguir demonstra isso:</span><span class="sxs-lookup"><span data-stu-id="07ba7-121">The following code example demonstrates this:</span></span>


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



<span data-ttu-id="07ba7-122">Esse algoritmo computa o tamanho do buffer multiplicando o tempo de atraso, em milissegundos, pelo número de amostras por milissegundo, multiplicando o resultado pelo número de canais e, em seguida, multiplicando o resultado pelo número de bytes por amostra.</span><span class="sxs-lookup"><span data-stu-id="07ba7-122">This algorithm computes the buffer size by multiplying the delay time, in milliseconds, by the number of samples per millisecond, then multiplying the result by the number of channels, and then multiplying the result by the number of bytes per sample.</span></span> <span data-ttu-id="07ba7-123">O número de canais e o número de bytes por amostra não são óbvios; Eles são codificados no membro nBlockAlign.</span><span class="sxs-lookup"><span data-stu-id="07ba7-123">The number of channels and the number of bytes per sample are not obvious; they are encoded in the nBlockAlign member.</span></span> <span data-ttu-id="07ba7-124">Dividir por 1000 reduz o valor de nSamplesPerSec para amostras por milissegundo; o milissegundo é a unidade desejada porque o tempo de atraso é expresso em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="07ba7-124">Dividing by 1000 reduces the nSamplesPerSec value to samples per millisecond; the millisecond is the desired unit because the delay time is expressed in milliseconds.</span></span>

## <a name="allocating-the-delay-buffer-memory"></a><span data-ttu-id="07ba7-125">Alocando a memória de buffer de atraso</span><span class="sxs-lookup"><span data-stu-id="07ba7-125">Allocating the Delay Buffer Memory</span></span>

<span data-ttu-id="07ba7-126">Depois de calcular os requisitos de memória, você pode alocar o buffer.</span><span class="sxs-lookup"><span data-stu-id="07ba7-126">Once you have calculated the memory requirements, you can allocate the buffer.</span></span> <span data-ttu-id="07ba7-127">O buffer pode precisar ser excluído se existir, por exemplo, quando o usuário chamar a página de propriedades para alterar o valor do tempo de atraso.</span><span class="sxs-lookup"><span data-stu-id="07ba7-127">The buffer may need to be deleted if it exists, such as when the user invokes the property page to change the delay time value.</span></span> <span data-ttu-id="07ba7-128">O código a seguir demonstra a alocação do buffer de atraso:</span><span class="sxs-lookup"><span data-stu-id="07ba7-128">The following code demonstrates allocating the delay buffer:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



<span data-ttu-id="07ba7-129">Se o buffer for alocado com êxito, você deverá mover o ponteiro móvel para o cabeçalho do buffer, conforme demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="07ba7-129">If the buffer is successfully allocated, you should move the movable pointer to the head of the buffer, as demonstrated in the following example:</span></span>


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a><span data-ttu-id="07ba7-130">Preenchendo o buffer de atraso com silêncio</span><span class="sxs-lookup"><span data-stu-id="07ba7-130">Filling the Delay Buffer with Silence</span></span>

<span data-ttu-id="07ba7-131">É conveniente escrever um método para preencher o buffer de atraso com valores que representam silêncio.</span><span class="sxs-lookup"><span data-stu-id="07ba7-131">It is convenient to write a method to fill the delay buffer with values representing silence.</span></span> <span data-ttu-id="07ba7-132">O método deve receber o ponteiro para a estrutura WAVEFORMATEX válida e, em seguida, inspecionar o membro wBitsPerSample para determinar se o áudio é de 8 bits ou superior.</span><span class="sxs-lookup"><span data-stu-id="07ba7-132">The method should receive the pointer to the valid WAVEFORMATEX structure and then inspect the wBitsPerSample member to determine whether the audio is 8-bit or higher.</span></span> <span data-ttu-id="07ba7-133">O exemplo a seguir preenche o buffer de atraso com o valor correto para silêncio:</span><span class="sxs-lookup"><span data-stu-id="07ba7-133">The following example fills the delay buffer with the correct value for silence:</span></span>


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



<span data-ttu-id="07ba7-134">Lembre-se de adicionar a declaração de encaminhamento da função ao arquivo de cabeçalho Echo. h na seção particular:</span><span class="sxs-lookup"><span data-stu-id="07ba7-134">Remember to add the forward declaration for the function to the header file Echo.h in the private section:</span></span>


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



<span data-ttu-id="07ba7-135">Você deve adicionar o código ao final de AllocateStreamingResources para chamar esse método sempre que o buffer de atraso for criado ou redimensionado.</span><span class="sxs-lookup"><span data-stu-id="07ba7-135">You should add code at the end of AllocateStreamingResources to call this method each time the delay buffer is created or resized.</span></span> <span data-ttu-id="07ba7-136">O código de exemplo a seguir passa o ponteiro WAVEFORMATEX chamado pWave para o novo método:</span><span class="sxs-lookup"><span data-stu-id="07ba7-136">The following example code passes the WAVEFORMATEX pointer named pWave to the new method:</span></span>


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a><span data-ttu-id="07ba7-137">Realocando a memória de buffer de atraso</span><span class="sxs-lookup"><span data-stu-id="07ba7-137">Reallocating the Delay Buffer Memory</span></span>

<span data-ttu-id="07ba7-138">Quando o usuário altera o tempo de atraso usando a página de propriedades, o tamanho do buffer de atraso também deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="07ba7-138">When the user changes the delay time by using the property page, the size of the delay buffer must change as well.</span></span> <span data-ttu-id="07ba7-139">Você já adicionou o código a AllocateStreamingResources para redimensionar o buffer, mas precisa adicionar uma linha de código ao CEcho::p o \_ atraso de UT para chamar o método de alocação de recursos sempre que o valor da propriedade for alterado.</span><span class="sxs-lookup"><span data-stu-id="07ba7-139">You've already added the code to AllocateStreamingResources to resize the buffer, but you need to add a line of code to CEcho::put\_delay to call the resource allocation method each time the property value changes.</span></span> <span data-ttu-id="07ba7-140">Eis o código:</span><span class="sxs-lookup"><span data-stu-id="07ba7-140">Here is the code:</span></span>


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a><span data-ttu-id="07ba7-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07ba7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07ba7-142">**Trabalhando com recursos de streaming**</span><span class="sxs-lookup"><span data-stu-id="07ba7-142">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




