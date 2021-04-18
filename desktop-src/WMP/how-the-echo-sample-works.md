---
title: Como funciona o exemplo de eco
description: Como funciona o exemplo de eco
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Plug-ins do Windows Media Player, visão geral do eco de exemplo
- plug-ins, visão geral do eco de exemplo
- plug-ins de processamento de sinal digital, visão geral do eco de exemplo
- Plug-ins do DSP, visão geral do eco de exemplo
- Exemplo de plug-in do eco DSP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760257"
---
# <a name="how-the-echo-sample-works"></a><span data-ttu-id="87381-108">Como funciona o exemplo de eco</span><span class="sxs-lookup"><span data-stu-id="87381-108">How the Echo Sample Works</span></span>

<span data-ttu-id="87381-109">O código cria o efeito de eco alocando um buffer grande o suficiente para conter exatamente a quantidade de dados de áudio que podem ser processados no período especificado pelo valor de tempo de atraso.</span><span class="sxs-lookup"><span data-stu-id="87381-109">The code creates the echo effect by allocating a buffer large enough to contain exactly the amount of audio data that can be rendered in the time frame specified by the delay time value.</span></span> <span data-ttu-id="87381-110">O tamanho do buffer é calculado, em bytes, pela seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="87381-110">The size of the buffer is calculated, in bytes, by the following formula:</span></span>

<span data-ttu-id="87381-111">tamanho do buffer = tempo de atraso \* /taxa de amostragem/alinhamento de bloco de 1000 \*</span><span class="sxs-lookup"><span data-stu-id="87381-111">buffer size = delay time \* sample rate / 1000 \* block alignment</span></span>

<span data-ttu-id="87381-112">O tempo de atraso é em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="87381-112">The delay time is in milliseconds.</span></span> <span data-ttu-id="87381-113">Os valores de taxa de amostra e alinhamento de bloco são fornecidos em uma estrutura WAVEFORMATEX.</span><span class="sxs-lookup"><span data-stu-id="87381-113">The sample rate and block alignment values are given in a WAVEFORMATEX structure.</span></span> <span data-ttu-id="87381-114">A taxa de amostra está em exemplos por segundo; dividir por 1000 produz amostras por milissegundo.</span><span class="sxs-lookup"><span data-stu-id="87381-114">The sample rate is in samples per second; dividing by 1000 yields samples per millisecond.</span></span> <span data-ttu-id="87381-115">O alinhamento de bloco é igual ao produto do número de canais (1 para mono, 2 para estéreo) e o número de bits por amostra (8 ou 16) dividido por 8 (bits por byte).</span><span class="sxs-lookup"><span data-stu-id="87381-115">The block alignment is equal to the product of the number of channels (1 for mono, 2 for stereo) and the number of bits per sample (8 or 16) divided by 8 (bits per byte).</span></span>

<span data-ttu-id="87381-116">Além da variável de ponteiro que aponta para o cabeçalho do buffer de atraso, o código cria um ponteiro móvel que percorre os dados no buffer em sincronização com o loop de processamento na função **DoProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="87381-116">In addition to the pointer variable that points to the head of the delay buffer, the code creates a movable pointer that steps through the data in the buffer in synchronization with the processing loop in the **DoProcessOutput** function.</span></span> <span data-ttu-id="87381-117">Quando o ponteiro móvel atinge o final do buffer de atraso, ele volta ao início do buffer.</span><span class="sxs-lookup"><span data-stu-id="87381-117">When the movable pointer reaches the end of the delay buffer, it moves back to the head of the buffer.</span></span> <span data-ttu-id="87381-118">Um buffer usado dessa maneira é chamado de buffer circular.</span><span class="sxs-lookup"><span data-stu-id="87381-118">A buffer used in this manner is called a circular buffer.</span></span>

<span data-ttu-id="87381-119">Depois que o buffer de atraso existir, e o Windows Media Player tiver alocado um buffer de entrada para fornecer dados de áudio e um buffer de saída para receber dados de áudio processados, o processamento de eco continuará da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="87381-119">Once the delay buffer exists, and Windows Media Player has allocated an input buffer to supply audio data and an output buffer to receive processed audio data, the echo processing proceeds like this:</span></span>

1.  <span data-ttu-id="87381-120">Insira um loop que permita o processamento de cada amostra de áudio no buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="87381-120">Enter a loop that allows processing of each audio sample in the input buffer.</span></span>
2.  <span data-ttu-id="87381-121">Recupere um exemplo do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="87381-121">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="87381-122">Em seguida, mova o ponteiro de buffer de entrada para a próxima amostra para se preparar para a próxima iteração do loop.</span><span class="sxs-lookup"><span data-stu-id="87381-122">Then, move the input buffer pointer forward to the next sample to prepare for the next loop iteration.</span></span>
3.  <span data-ttu-id="87381-123">Recupere um exemplo do buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="87381-123">Retrieve a sample from the delay buffer.</span></span>
4.  <span data-ttu-id="87381-124">Copie o exemplo do buffer de entrada para o mesmo local no buffer de atraso do qual a amostra do último atraso foi recuperada.</span><span class="sxs-lookup"><span data-stu-id="87381-124">Copy the sample from the input buffer to the same location in the delay buffer from which the last delay sample was retrieved.</span></span>
5.  <span data-ttu-id="87381-125">Mova o ponteiro de buffer de atraso para a próxima amostra.</span><span class="sxs-lookup"><span data-stu-id="87381-125">Move the delay buffer pointer forward to the next sample.</span></span> <span data-ttu-id="87381-126">Se o ponteiro mover após o final do buffer, mova-o para o cabeçalho do buffer.</span><span class="sxs-lookup"><span data-stu-id="87381-126">If the pointer moves past the end of the buffer, move it to the head of the buffer.</span></span>
6.  <span data-ttu-id="87381-127">Combine o exemplo do buffer de entrada com o exemplo do buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="87381-127">Combine the sample from the input buffer with the sample from the delay buffer.</span></span>
7.  <span data-ttu-id="87381-128">Copie o resultado para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="87381-128">Copy the result to the output buffer.</span></span> <span data-ttu-id="87381-129">Em seguida, mova o ponteiro de buffer de saída para a próxima unidade para se preparar para a próxima iteração do loop.</span><span class="sxs-lookup"><span data-stu-id="87381-129">Then, move the output buffer pointer forward to the next unit to prepare for the next loop iteration.</span></span>
8.  <span data-ttu-id="87381-130">Repita até que todos os exemplos sejam processados.</span><span class="sxs-lookup"><span data-stu-id="87381-130">Repeat until all the samples are processed.</span></span>

<span data-ttu-id="87381-131">Quando um exemplo de entrada recuperado na etapa 2 é copiado para o buffer de atraso na etapa 4, ele permanece lá até que o ponteiro móvel percorra cada exemplo no buffer de atraso e, finalmente, retorne à mesma posição.</span><span class="sxs-lookup"><span data-stu-id="87381-131">When an input sample retrieved in step 2 is copied to the delay buffer in step 4, it remains there until the movable pointer steps through each sample in the delay buffer and finally returns to the same position.</span></span> <span data-ttu-id="87381-132">Como o tamanho do buffer de atraso é projetado para corresponder ao tempo de atraso, o tempo decorrido entre o exemplo que está sendo copiado para o buffer de atraso e o exemplo que está sendo recuperado mais uma vez é igual ao atraso especificado (além de qualquer latência introduzida pelo processamento real).</span><span class="sxs-lookup"><span data-stu-id="87381-132">Because the size of the delay buffer is designed to correspond to the delay time, the elapsed time between the sample being copied to the delay buffer and the sample being retrieved once again equals the specified delay (plus any latency introduced by the actual processing).</span></span>

<span data-ttu-id="87381-133">Quando um fluxo é iniciado, nenhum dado de atraso é gerado até que o tempo de atraso tenha decorrido.</span><span class="sxs-lookup"><span data-stu-id="87381-133">When a stream starts, no delay data is generated until the delay time has elapsed.</span></span> <span data-ttu-id="87381-134">Portanto, é importante que o buffer de atraso inicialmente contenha silêncio.</span><span class="sxs-lookup"><span data-stu-id="87381-134">Therefore, it is important that the delay buffer initially contains silence.</span></span> <span data-ttu-id="87381-135">Se o buffer de atraso contiver dados aleatórios, o usuário ouvirá o ruído de branco até que o plug-in gere dados de atraso suficientes para substituir todo o buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="87381-135">If the delay buffer contains random data, the user will hear white noise until the plug-in generates enough delay data to overwrite the entire delay buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87381-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87381-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87381-137">**Visão geral do eco de exemplo**</span><span class="sxs-lookup"><span data-stu-id="87381-137">**Echo Sample Overview**</span></span>](echo-sample-overview.md)
</dt> </dl>

 

 




