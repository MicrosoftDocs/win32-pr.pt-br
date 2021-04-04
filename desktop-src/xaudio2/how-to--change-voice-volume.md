---
description: Este tópico mostra como você pode alterar o volume de uma voz em um nível geral, em cada canal de saída ou entre cada canal de uma voz e outra voz em sua caixa de envio.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Como: alterar o volume de voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662553"
---
# <a name="how-to-change-voice-volume"></a><span data-ttu-id="ff2d7-103">Como: alterar o volume de voz</span><span class="sxs-lookup"><span data-stu-id="ff2d7-103">How to: Change Voice Volume</span></span>

<span data-ttu-id="ff2d7-104">Este tópico mostra como você pode alterar o volume de uma voz em um nível geral, em cada canal de saída ou entre cada canal de uma voz e outra voz em sua caixa de [**envio**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="ff2d7-104">This topic shows you how you can change the volume of a voice at an overall level, at each output channel, or between each channel of a voice and another voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a><span data-ttu-id="ff2d7-105">Para definir um nível de volume geral para a entrada da voz</span><span class="sxs-lookup"><span data-stu-id="ff2d7-105">To set an overall volume level for the voice's input</span></span>

-   <span data-ttu-id="ff2d7-106">Use a função [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .</span><span class="sxs-lookup"><span data-stu-id="ff2d7-106">Use the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function.</span></span>

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a><span data-ttu-id="ff2d7-107">Para definir o volume dos canais de saída da voz</span><span class="sxs-lookup"><span data-stu-id="ff2d7-107">To set the volume of the voice's output channels</span></span>

1.  <span data-ttu-id="ff2d7-108">Crie uma matriz de números de ponto flutuante que contenham os volumes desejados de todos os canais de saída na voz.</span><span class="sxs-lookup"><span data-stu-id="ff2d7-108">Create an array of floating point numbers that contain the desired volumes of all the output channels in the voice.</span></span>

    <span data-ttu-id="ff2d7-109">A matriz terá uma entrada para cada canal na voz.</span><span class="sxs-lookup"><span data-stu-id="ff2d7-109">The array will have one entry for each channel in the voice.</span></span>

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  <span data-ttu-id="ff2d7-110">Use a função [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) para definir o volume dos canais de saída.</span><span class="sxs-lookup"><span data-stu-id="ff2d7-110">Use the [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) function to set the volume of the output channels.</span></span>

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a><span data-ttu-id="ff2d7-111">Para definir o volume de conexões</span><span class="sxs-lookup"><span data-stu-id="ff2d7-111">To set the volume of connections</span></span>

<span data-ttu-id="ff2d7-112">Defina o volume de conexão entre a voz e uma voz em sua caixa de [**envio**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="ff2d7-112">Set the connection volume between the voice and a voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

1.  <span data-ttu-id="ff2d7-113">Crie uma matriz de números de ponto flutuante que define uma matriz de saída se a voz enviar para outra voz.</span><span class="sxs-lookup"><span data-stu-id="ff2d7-113">Create an array of floating point numbers that defines an output matrix if the voice sends to another voice.</span></span>

    > [!Note]  
    > <span data-ttu-id="ff2d7-114">A matriz deve ter um número de entradas iguais a canais de voz de origem × canais de voz de destino.</span><span class="sxs-lookup"><span data-stu-id="ff2d7-114">The array must have a number of entries equal to source voice channels × destination voice channels.</span></span> <span data-ttu-id="ff2d7-115">Neste exemplo, o mapeamento é de uma voz com um canal para uma voz com dois canais.</span><span class="sxs-lookup"><span data-stu-id="ff2d7-115">In this example, the mapping is from a voice with one channel to a voice with two channels.</span></span>

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  <span data-ttu-id="ff2d7-116">Use a função [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para definir a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="ff2d7-116">Use the [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) function to set the output matrix.</span></span>

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ff2d7-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff2d7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff2d7-118">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="ff2d7-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ff2d7-119">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="ff2d7-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="ff2d7-120">Controle de volume e densidade XAudio2</span><span class="sxs-lookup"><span data-stu-id="ff2d7-120">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
