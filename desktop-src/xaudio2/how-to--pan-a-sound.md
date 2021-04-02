---
description: Este tópico mostra como você pode definir a matriz de saída de uma voz de origem mono que gera uma voz de mestre de estéreo para obter movimento panorâmico entre os alto-falantes esquerdo e direito.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Como: deslocar um som'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829071"
---
# <a name="how-to-pan-a-sound"></a><span data-ttu-id="28da9-103">Como: deslocar um som</span><span class="sxs-lookup"><span data-stu-id="28da9-103">How to: Pan a Sound</span></span>

<span data-ttu-id="28da9-104">Este tópico mostra como você pode definir a matriz de saída de uma voz de origem mono que gera uma voz de mestre de estéreo para obter movimento panorâmico entre os alto-falantes esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="28da9-104">This topic shows you how you can set the output matrix of a mono source voice that outputs to a stereo mastering voice in order to achieve panning between the left and right speakers.</span></span>

## <a name="to-setup-panning"></a><span data-ttu-id="28da9-105">Para configurar o movimento panorâmico</span><span class="sxs-lookup"><span data-stu-id="28da9-105">To setup panning</span></span>

1.  <span data-ttu-id="28da9-106">Recupere a configuração do alto-falante usando [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="28da9-106">Retrieve the speaker configuration using [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  <span data-ttu-id="28da9-107">Crie uma matriz para manter a matriz de saída.</span><span class="sxs-lookup"><span data-stu-id="28da9-107">Create an array to hold the output matrix.</span></span> <span data-ttu-id="28da9-108">O tamanho mínimo da matriz de saída é o número de canais na voz de origem, o número de canais na voz de saída.</span><span class="sxs-lookup"><span data-stu-id="28da9-108">The minimum size of the output matrix is the number of channels in the source voice times the number of channels in the output voice.</span></span> <span data-ttu-id="28da9-109">Nesse caso, uma matriz de oito elementos tratará uma saída de voz mono para qualquer formato de saída de até 7,1 surround sound.</span><span class="sxs-lookup"><span data-stu-id="28da9-109">In this case an eight element array will handle a mono voice outputting to any output format up to 7.1 surround sound.</span></span>

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  <span data-ttu-id="28da9-110">Calcule os níveis de envio com base no movimento panorâmico desejado entre os alto-falantes esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="28da9-110">Calculate the send levels based on the desired panning between the left and right speakers.</span></span> <span data-ttu-id="28da9-111">Neste exemplo, os valores de Pan vão de-1 a 1 com-1, indicando todo o som para o palestrante esquerdo e 1 indicando todo o som ao alto-falante direito.</span><span class="sxs-lookup"><span data-stu-id="28da9-111">In this example, pan values will range from -1 to 1 with -1 indicating all sound to the left speaker and 1 indicating all sound to the right speaker.</span></span>

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  <span data-ttu-id="28da9-112">Defina os índices de matriz de saída correspondentes aos alto-falantes esquerdo e direito com os valores calculados na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="28da9-112">Set the output matrix indices corresponding to the left and right speakers with the values calculated in the previous step.</span></span> <span data-ttu-id="28da9-113">Os alto-falantes esquerdo e direito são determinados examinando a máscara de canal retornada por [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="28da9-113">The left and right speakers are determined by looking at the channel mask returned by [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span> <span data-ttu-id="28da9-114">Como os canais sempre devem ser codificados na ordem especificada na página de referência do [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , é possível determinar o índice de matriz correspondente a um orador individual.</span><span class="sxs-lookup"><span data-stu-id="28da9-114">Since the channels must always be encoded in the order specified on the [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) reference page, it is possible to determine the array index corresponding to an individual speaker.</span></span>

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  <span data-ttu-id="28da9-115">Aplique a matriz de saída à voz de origem usando [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span><span class="sxs-lookup"><span data-stu-id="28da9-115">Apply the output matrix to the originating voice by using [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span></span> <span data-ttu-id="28da9-116">A voz de origem será uma voz de origem ou uma voz submix enviando para uma voz submix ou uma voz de mestre.</span><span class="sxs-lookup"><span data-stu-id="28da9-116">The originating voice will be either a source voice or a submix voice sending to either a submix voice or a mastering voice.</span></span> <span data-ttu-id="28da9-117">Você pode obter informações sobre as vozes de origem e de destino, como o número de canais, usando [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span><span class="sxs-lookup"><span data-stu-id="28da9-117">You can get info about the originating and destination voices, like their number of channels, by using [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span></span>

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="28da9-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28da9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28da9-119">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="28da9-119">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="28da9-120">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="28da9-120">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="28da9-121">Controle de volume e densidade XAudio2</span><span class="sxs-lookup"><span data-stu-id="28da9-121">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
