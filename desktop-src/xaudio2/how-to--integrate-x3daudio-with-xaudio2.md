---
description: Este tópico mostra como integrar o X3DAudio ao XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Como: Integrar X3DAudio ao XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662552"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a><span data-ttu-id="ff318-103">Como: Integrar X3DAudio ao XAudio2</span><span class="sxs-lookup"><span data-stu-id="ff318-103">How to: Integrate X3DAudio with XAudio2</span></span>

<span data-ttu-id="ff318-104">Este tópico mostra como integrar o X3DAudio ao XAudio2.</span><span class="sxs-lookup"><span data-stu-id="ff318-104">This topic shows how to integrate X3DAudio with XAudio2.</span></span> <span data-ttu-id="ff318-105">Você pode usar X3DAudio para fornecer os valores de volume e de densidade para vozes XAudio2 e os parâmetros para o efeito de reverberação interno XAudio2.</span><span class="sxs-lookup"><span data-stu-id="ff318-105">You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect.</span></span> <span data-ttu-id="ff318-106">Este tópico pressupõe que você criou um grafo de áudio conforme descrito em [como compilar um grafo básico de processamento de áudio](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="ff318-106">This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="ff318-107">Se você ainda não criou um grafo de áudio, o [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) falhará.</span><span class="sxs-lookup"><span data-stu-id="ff318-107">If you have not already created an audio graph, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) will fail.</span></span>

<span data-ttu-id="ff318-108">**Para inicializar o X3DAudio**</span><span class="sxs-lookup"><span data-stu-id="ff318-108">**To initialize X3DAudio**</span></span>

1.  <span data-ttu-id="ff318-109">Inicialize o X3DAudio chamando [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span><span class="sxs-lookup"><span data-stu-id="ff318-109">Initialize X3DAudio by calling [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span></span>

    <span data-ttu-id="ff318-110">A função [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) recebe sinalizadores que indicam a configuração do alto-falante, a velocidade do som em unidades mundiais definidas pelo usuário por segundo e um identificador para retornar uma instância do mecanismo X3DAudio.</span><span class="sxs-lookup"><span data-stu-id="ff318-110">The [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine.</span></span> <span data-ttu-id="ff318-111">Chame [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para obter a máscara de canal do formato de saída.</span><span class="sxs-lookup"><span data-stu-id="ff318-111">Call [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) to get the output format's channel mask.</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  <span data-ttu-id="ff318-112">Crie instâncias das estruturas [**\_ ouvinte X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**\_ emissor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="ff318-112">Create instances of the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span>

    <span data-ttu-id="ff318-113">A estrutura do [**\_ ouvinte X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) representa a posição de tudo o que está ouvindo o som.</span><span class="sxs-lookup"><span data-stu-id="ff318-113">The [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) structure represents the position of whatever is hearing the sound.</span></span> <span data-ttu-id="ff318-114">Em geral, essa é a posição da câmera ou de uma posição perto dela.</span><span class="sxs-lookup"><span data-stu-id="ff318-114">Generally, this is the position of the camera or a position close to it.</span></span> <span data-ttu-id="ff318-115">A estrutura do [**\_ emissor do X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) representa a posição do item que faz o som.</span><span class="sxs-lookup"><span data-stu-id="ff318-115">The [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure represents the position of the thing making the sound.</span></span> <span data-ttu-id="ff318-116">Haverá uma estrutura do **\_ emissor do X3DAUDIO** para cada som que está sendo acompanhado.</span><span class="sxs-lookup"><span data-stu-id="ff318-116">There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.</span></span>

    <span data-ttu-id="ff318-117">Os membros das estruturas que não serão atualizadas em um loop de jogo devem ser inicializados aqui.</span><span class="sxs-lookup"><span data-stu-id="ff318-117">Members of the structures that will not be updated in a game loop should be initialized here.</span></span> <span data-ttu-id="ff318-118">A maioria dos membros das estruturas pode simplesmente ser inicializada para zero.</span><span class="sxs-lookup"><span data-stu-id="ff318-118">Most members of the structures can simply be initialized to zero.</span></span> <span data-ttu-id="ff318-119">No entanto, alguns membros do [**\_ emissor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) precisam ser definidos para serem inicializados com valores diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="ff318-119">However, some members of [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) need to be set to be initialized to non-zero values.</span></span> <span data-ttu-id="ff318-120">O membro ChannelCount do **\_ emissor de X3DAUDIO** precisa ser inicializado para o número de canais na voz que o emissor representa.</span><span class="sxs-lookup"><span data-stu-id="ff318-120">The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents.</span></span> <span data-ttu-id="ff318-121">Além disso, o membro CurveDistanceScaler **do \_ emissor X3DAUDIO** deve estar no intervalo de FLT \_ min a FLT \_ Max.</span><span class="sxs-lookup"><span data-stu-id="ff318-121">Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.</span></span>

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  <span data-ttu-id="ff318-122">Crie uma instância da estrutura [**de \_ \_ configurações do DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .</span><span class="sxs-lookup"><span data-stu-id="ff318-122">Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure.</span></span>

    <span data-ttu-id="ff318-123">A estrutura de [**\_ \_ configurações do DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) é usada para retornar resultados calculados por [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span><span class="sxs-lookup"><span data-stu-id="ff318-123">The [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure is used to return results calculated by [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span></span> <span data-ttu-id="ff318-124">A função **X3DAudioCalculate** não aloca memória para nenhum de seus parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ff318-124">The **X3DAudioCalculate** function does not allocate memory for any of its parameters.</span></span> <span data-ttu-id="ff318-125">Isso significa que você precisa alocar matrizes para os membros pMatrixCoefficients e pDelayTimes da estrutura de **\_ \_ configurações do DSP X3DAUDIO** se pretender usá-las.</span><span class="sxs-lookup"><span data-stu-id="ff318-125">This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them.</span></span> <span data-ttu-id="ff318-126">Além disso, você precisa definir os membros SrcChannelCount e DstChannelCount como o número de canais nas vozes de origem e de destino do emissor.</span><span class="sxs-lookup"><span data-stu-id="ff318-126">In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.</span></span>

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > <span data-ttu-id="ff318-127">Use [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) na voz de mestre para obter o número de InputChannels para **nChannels**.</span><span class="sxs-lookup"><span data-stu-id="ff318-127">Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) on the mastering voice to obtain the number of InputChannels for **nChannels**.</span></span> <span data-ttu-id="ff318-128">Para versões do SDK do DirectX do XAUDIO2 anteriores ao Windows 8, use IXAudio2:: GetDeviceDetails.</span><span class="sxs-lookup"><span data-stu-id="ff318-128">For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.</span></span>

     

<span data-ttu-id="ff318-129">Execute estas etapas uma vez a cada dois ou três quadros para calcular novas configurações e aplicá-las.</span><span class="sxs-lookup"><span data-stu-id="ff318-129">Perform these steps once every two to three frames to calculate new settings and apply them.</span></span> <span data-ttu-id="ff318-130">Neste exemplo, uma voz de origem está enviando diretamente para a voz de mestre e para uma voz submix com um efeito de reverberação aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="ff318-130">In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.</span></span>

<span data-ttu-id="ff318-131">**Para usar o X3DAudio para calcular e aplicar novas configurações de áudio 3D**</span><span class="sxs-lookup"><span data-stu-id="ff318-131">**To use X3DAudio to calculate and apply new 3D audio settings**</span></span>

1.  <span data-ttu-id="ff318-132">Atualize as estruturas do [**\_ emissor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) do X3DAUDIO e do [**\_ ouvinte**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) X3DAUDIO com sua posição, velocidade e orientação atuais.</span><span class="sxs-lookup"><span data-stu-id="ff318-132">Update the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures with their current position, velocity, and orientation.</span></span>

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  <span data-ttu-id="ff318-133">Chame [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) para calcular as novas configurações para as vozes.</span><span class="sxs-lookup"><span data-stu-id="ff318-133">Call [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) to calculate new settings for the voices.</span></span>

    <span data-ttu-id="ff318-134">Os parâmetros para [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) serão as estruturas [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ emissor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) atualizadas.</span><span class="sxs-lookup"><span data-stu-id="ff318-134">The parameters for [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) will be the updated [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span> <span data-ttu-id="ff318-135">Os sinalizadores indicarão quais valores **X3DAudioCalculate** deve calcular e qual estrutura [**de \_ \_ configurações do DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) manterá os resultados dos cálculos executados.</span><span class="sxs-lookup"><span data-stu-id="ff318-135">The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure will hold the results of the calculations performed.</span></span>

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  <span data-ttu-id="ff318-136">Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar os valores de volume e de densidade à voz de origem.</span><span class="sxs-lookup"><span data-stu-id="ff318-136">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) to apply the volume and pitch values to the source voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  <span data-ttu-id="ff318-137">Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para aplicar o nível de reverberação calculado à voz submix.</span><span class="sxs-lookup"><span data-stu-id="ff318-137">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) to apply the calculated reverb level to the submix voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  <span data-ttu-id="ff318-138">Use [**IXAudio2Voice:: Setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para aplicar o coeficiente de passagem baixa do filtro direto à voz de origem.</span><span class="sxs-lookup"><span data-stu-id="ff318-138">Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) to apply the calculated low pass filter direct coefficient to the source voice.</span></span>

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ff318-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff318-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff318-140">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="ff318-140">X3DAudio</span></span>](x3daudio.md)
</dt> <dt>

[<span data-ttu-id="ff318-141">Visão geral do X3DAudio</span><span class="sxs-lookup"><span data-stu-id="ff318-141">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="ff318-142">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="ff318-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ff318-143">Controle de volume e densidade XAudio2</span><span class="sxs-lookup"><span data-stu-id="ff318-143">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
