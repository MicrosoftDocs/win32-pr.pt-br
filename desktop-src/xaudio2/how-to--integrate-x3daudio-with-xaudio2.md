---
description: Este tópico mostra como integrar o X3DAudio ao XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Como: Integrar X3DAudio ao XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c940acbe78e8d4ca4247f77500adeeca7c9619057a3008dea50fc8b55a9f364e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962685"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Como: Integrar X3DAudio ao XAudio2

Este tópico mostra como integrar o X3DAudio ao XAudio2. Você pode usar X3DAudio para fornecer os valores de volume e tom para vozes XAudio2 e os parâmetros para o efeito de reverb criado no XAudio2. Este tópico pressupo que você criou um grafo de áudio conforme descrito em Como [criar um](how-to--build-a-basic-audio-processing-graph.md)processamento de áudio básico Graph . Se você ainda não tiver criado um grafo de áudio, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) falhará.

**Para inicializar o X3DAudio**

1.  Inicialize X3DAudio chamando [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    A [**função X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) recebe sinalizadores que indicam a configuração do locutor, a velocidade do som em unidades do mundo definidas pelo usuário por segundo e um handle para retornar uma instância do mecanismo X3DAudio. Chame [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para obter a máscara de canal do formato de saída.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Crie instâncias das estruturas [**X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ EMITTER.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

    A [**estrutura LISTENER \_ X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) representa a posição de tudo o que está escutando o som. Geralmente, essa é a posição da câmera ou uma posição próxima a ela. A [**estrutura \_ EMITTER X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) representa a posição da coisa que está fazendo o som. Haverá uma estrutura **\_ EMITTER X3DAUDIO** para cada som que está sendo rastreado.

    Os membros das estruturas que não serão atualizadas em um loop de jogo devem ser inicializados aqui. A maioria dos membros das estruturas pode simplesmente ser inicializada como zero. No entanto, alguns membros do [**\_ EMITTER X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) precisam ser definidos para serem inicializados com valores diferentes de zero. O membro ChannelCount do **\_ EMITTER X3DAUDIO** precisa ser inicializado para o número de canais na voz que o emissor representa. Além disso, o membro CurveDistanceScaler do **X3DAUDIO \_ EMITTER** deve estar no intervalo FLT \_ MIN a FLT \_ MAX.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Crie uma instância da estrutura [**X3DAUDIO \_ DSP \_ SETTINGS.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)

    A [**estrutura X3DAUDIO DSP SETTINGS é usada para retornar resultados \_ \_ calculados**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) por [**X3DAudioCalculate.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) A **função X3DAudioCalculate** não aloca memória para nenhum de seus parâmetros. Isso significa que você precisa alocar matrizes para os membros pMatrixCoefficients e pDelayTimes da estrutura **\_ DSP X3DAUDIO se \_** você pretende usá-las. Além disso, você precisa definir os membros SrcChannelCount e DstChannelCount para o número de canais nas vozes de origem e destino do emissor.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) na voz mestra para obter o número de InputChannels para **nChannels**. Para versões do SDK do DirectX do XAUDIO2 antes Windows 8, use IXAudio2::GetDeviceDetails.

     

Execute essas etapas uma vez a cada dois a três quadros para calcular novas configurações e aplicá-las. Neste exemplo, uma voz de origem está enviando diretamente para a voz mestra e para uma voz submix com um efeito reverb aplicado a ela.

**Para usar x3DAudio para calcular e aplicar novas configurações de áudio 3D**

1.  Atualize [**as estruturas X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) com sua posição atual, velocidade e orientação.

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

    

2.  Chame [**X3DAudioCalculate para**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) calcular novas configurações para as vozes.

    Os parâmetros para [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) serão as estruturas [**X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ EMITTER atualizadas.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) Os sinalizadores indicarão quais valores **X3DAudioCalculate** devem calcular e quais configurações de DSP X3DAUDIO conterão os resultados dos [**\_ \_ cálculos executados.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar os valores de volume e tom à voz de origem.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para aplicar o nível de reverb calculado à voz da submix.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para aplicar o coeficiente direto do filtro de passagem baixo calculado à voz de origem.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[Visão geral do X3DAudio](x3daudio-overview.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Controle de volume e tom XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
