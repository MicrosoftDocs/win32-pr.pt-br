---
title: Usando níveis de tempo
description: Usando níveis de tempo
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- visualizações, eventos cronometrados
- visualizações personalizadas, eventos cronometrados
- visualizações, matriz de frequência
- visualizações personalizadas, matriz de frequência
- visualizações, matriz de formato de onda
- visualizações personalizadas, matriz de formato de onda
- visualizações, variável de estado
- visualizações personalizadas, variável de estado
- visualizações, variável timeStamp
- visualizações personalizadas, variável timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005543"
---
# <a name="using-timed-levels"></a><span data-ttu-id="fc1ea-113">Usando níveis de tempo</span><span class="sxs-lookup"><span data-stu-id="fc1ea-113">Using Timed Levels</span></span>

<span data-ttu-id="fc1ea-114">A estrutura **TimedLevel** é composta de matrizes 2 2-dimensional, um valor de estado e um valor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-114">The **TimedLevel** structure is composed of two two-dimensional arrays, a state value, and a time stamp value.</span></span>

## <a name="frequency-array"></a><span data-ttu-id="fc1ea-115">Matriz de frequência</span><span class="sxs-lookup"><span data-stu-id="fc1ea-115">Frequency Array</span></span>

<span data-ttu-id="fc1ea-116">A matriz Frequency é uma matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-116">The frequency array is a two-dimensional array.</span></span> <span data-ttu-id="fc1ea-117">A primeira dimensão de cada matriz corresponde ao canal de áudio estéreo (esquerda ou direita) e a segunda corresponde aos níveis de frequência (em bytes) do instantâneo, onde o espectro de áudio é dividido em regiões de 1024.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-117">The first dimension of each array corresponds to the stereo audio channel (left or right), and the second corresponds to the frequency levels (in bytes) of the snapshot, where the audio spectrum is divided up into 1024 regions.</span></span>

<span data-ttu-id="fc1ea-118">Você pode obter os dados da matriz de frequência fornecidos pelo Windows Media Player da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fc1ea-118">You can get the frequency array data supplied from the Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



<span data-ttu-id="fc1ea-119">O valor de instantâneo é para o canal esquerdo e contém o valor da parte mais baixa do espectro de frequência.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-119">The value of snapshot is for the left channel and contains the value of the lowest part of the frequency spectrum.</span></span> <span data-ttu-id="fc1ea-120">Por exemplo, se o instantâneo tiver um valor grande, ele indica que a parte mais baixa da 1024th do espectro de frequência é avançada em frequência.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-120">For example, if snapshot has a large value, it indicates that the lowest 1024th part of the frequency spectrum is rich in frequency.</span></span> <span data-ttu-id="fc1ea-121">Um valor de zero indica que não há valores de frequência baixa nessa parte do espectro para o canal esquerdo.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-121">A value of zero indicates no low frequency values in that part of the spectrum for the left channel.</span></span> <span data-ttu-id="fc1ea-122">Se você tiver um sinal de monotelephony, somente a primeira dimensão terá valores válidos.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-122">If you have a monophonic signal, only the first dimension has valid values.</span></span>

<span data-ttu-id="fc1ea-123">Se o sinal for não estéreo, a segunda matriz conterá uma cópia do sinal mono.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-123">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="fc1ea-124">Ou seja, \[ a frequência 0 \] \[ *n* \] e \[ a frequência 1 \] \[ *n* \] conterão os mesmos dados, em que *n* é o índice em uma determinada célula.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-124">That is, frequency\[0\]\[*n*\] and frequency\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="waveform-array"></a><span data-ttu-id="fc1ea-125">Matriz de formato de onda</span><span class="sxs-lookup"><span data-stu-id="fc1ea-125">Waveform Array</span></span>

<span data-ttu-id="fc1ea-126">A matriz de formato de onda também é uma matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-126">The waveform array is also a two-dimensional array.</span></span> <span data-ttu-id="fc1ea-127">A primeira dimensão da matriz corresponde ao canal (esquerda ou direita) e a segunda corresponde aos níveis de energia (em bytes) do instantâneo, onde a energia de áudio é dividida em 1024 segmentos de tempo contíguos.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-127">The first dimension of the array corresponds to the channel (left or right), and the second corresponds to the power levels (in bytes) of the snapshot, where the audio power is broken up into 1024 contiguous time segments.</span></span>

<span data-ttu-id="fc1ea-128">Você pode obter os dados da matriz de forma de onda do Windows Media Player da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fc1ea-128">You can get the waveform array data from Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



<span data-ttu-id="fc1ea-129">O valor de instantâneo é para o canal esquerdo e contém o primeiro valor do instantâneo quantificado dos valores de energia.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-129">The value of snapshot is for the left channel and contains the first value of the quantized snapshot of the power values.</span></span> <span data-ttu-id="fc1ea-130">Quando um instantâneo é obtido, ele consiste em 1024 pequenas medidas incrementais da potência de áudio.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-130">When a snapshot is taken, it consists of 1024 tiny incremental measurements of the audio power.</span></span> <span data-ttu-id="fc1ea-131">O valor mais baixo da matriz é gerado pela primeira medida incremental de energia de áudio.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-131">The lowest value of the array is generated by the first incremental measurement of audio power.</span></span> <span data-ttu-id="fc1ea-132">Observe que os valores da potência são medidos de-128 a + 127, mas os valores na matriz variam de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-132">Note that the values of the power are measured from -128 to +127 but the values in the array range from 0 to 255.</span></span> <span data-ttu-id="fc1ea-133">Se você tiver uma onda de telefonia, somente a primeira dimensão terá valores válidos.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-133">If you have a monophonic wave, only the first dimension will have valid values.</span></span>

<span data-ttu-id="fc1ea-134">Se o sinal for não estéreo, a segunda matriz conterá uma cópia do sinal mono.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-134">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="fc1ea-135">Ou seja, Wave \[ 0 \] \[ *n* \] e forma de onda \[ 1 \] \[ *n* \] conterão os mesmos dados, em que *n* é o índice em uma determinada célula.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-135">That is, waveform\[0\]\[*n*\] and waveform\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="state"></a><span data-ttu-id="fc1ea-136">Estado</span><span class="sxs-lookup"><span data-stu-id="fc1ea-136">State</span></span>

<span data-ttu-id="fc1ea-137">A variável de estado reflete o estado de reprodução de áudio do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-137">The state variable reflects the audio playback state of Windows Media Player.</span></span> <span data-ttu-id="fc1ea-138">Os valores de enumeração do Playerstate são</span><span class="sxs-lookup"><span data-stu-id="fc1ea-138">The PlayerState enumeration values are</span></span>


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



<span data-ttu-id="fc1ea-139">Você pode usar essa variável para executar ações diferentes dependendo do estado de reprodução de áudio.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-139">You can use this variable to take different actions depending on the audio playback state.</span></span> <span data-ttu-id="fc1ea-140">Por exemplo, você pode reproduzir um tipo de visualização quando o áudio estiver sendo reproduzido e outro quando for interrompido.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-140">For example, you can play one kind of visualization when the audio is playing and another when it is stopped.</span></span>

## <a name="time-stamp"></a><span data-ttu-id="fc1ea-141">Carimbo de Data/Hora</span><span class="sxs-lookup"><span data-stu-id="fc1ea-141">Time Stamp</span></span>

<span data-ttu-id="fc1ea-142">A variável timeStamp reflete a hora atual em que o instantâneo é tirado.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-142">The timeStamp variable reflects the current time when the snapshot is taken.</span></span> <span data-ttu-id="fc1ea-143">Isso pode ser usado para medir a frequência com que os instantâneos são obtidos.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-143">This can be used to measure how frequently the snapshots are taken.</span></span>

<span data-ttu-id="fc1ea-144">Você pode usar essa variável para cronometrar suas animações.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-144">You can use this variable to time your animations.</span></span> <span data-ttu-id="fc1ea-145">Se os instantâneos forem muito frequentes, você poderá degradar a imagem de forma elegante para exibição da maneira que escolher.</span><span class="sxs-lookup"><span data-stu-id="fc1ea-145">If the snapshots are too frequent, you can gracefully degrade your image to display in the manner you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc1ea-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc1ea-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc1ea-147">**Implementando renderização**</span><span class="sxs-lookup"><span data-stu-id="fc1ea-147">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




