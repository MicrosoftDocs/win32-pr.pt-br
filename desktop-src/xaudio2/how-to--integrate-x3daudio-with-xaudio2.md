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
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Como: Integrar X3DAudio ao XAudio2

Este tópico mostra como integrar o X3DAudio ao XAudio2. Você pode usar X3DAudio para fornecer os valores de volume e de densidade para vozes XAudio2 e os parâmetros para o efeito de reverberação interno XAudio2. Este tópico pressupõe que você criou um grafo de áudio conforme descrito em [como compilar um grafo básico de processamento de áudio](how-to--build-a-basic-audio-processing-graph.md). Se você ainda não criou um grafo de áudio, o [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) falhará.

**Para inicializar o X3DAudio**

1.  Inicialize o X3DAudio chamando [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    A função [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) recebe sinalizadores que indicam a configuração do alto-falante, a velocidade do som em unidades mundiais definidas pelo usuário por segundo e um identificador para retornar uma instância do mecanismo X3DAudio. Chame [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para obter a máscara de canal do formato de saída.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Crie instâncias das estruturas [**\_ ouvinte X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**\_ emissor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

    A estrutura do [**\_ ouvinte X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) representa a posição de tudo o que está ouvindo o som. Em geral, essa é a posição da câmera ou de uma posição perto dela. A estrutura do [**\_ emissor do X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) representa a posição do item que faz o som. Haverá uma estrutura do **\_ emissor do X3DAUDIO** para cada som que está sendo acompanhado.

    Os membros das estruturas que não serão atualizadas em um loop de jogo devem ser inicializados aqui. A maioria dos membros das estruturas pode simplesmente ser inicializada para zero. No entanto, alguns membros do [**\_ emissor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) precisam ser definidos para serem inicializados com valores diferentes de zero. O membro ChannelCount do **\_ emissor de X3DAUDIO** precisa ser inicializado para o número de canais na voz que o emissor representa. Além disso, o membro CurveDistanceScaler **do \_ emissor X3DAUDIO** deve estar no intervalo de FLT \_ min a FLT \_ Max.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Crie uma instância da estrutura [**de \_ \_ configurações do DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .

    A estrutura de [**\_ \_ configurações do DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) é usada para retornar resultados calculados por [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate). A função **X3DAudioCalculate** não aloca memória para nenhum de seus parâmetros. Isso significa que você precisa alocar matrizes para os membros pMatrixCoefficients e pDelayTimes da estrutura de **\_ \_ configurações do DSP X3DAUDIO** se pretender usá-las. Além disso, você precisa definir os membros SrcChannelCount e DstChannelCount como o número de canais nas vozes de origem e de destino do emissor.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Use [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) na voz de mestre para obter o número de InputChannels para **nChannels**. Para versões do SDK do DirectX do XAUDIO2 anteriores ao Windows 8, use IXAudio2:: GetDeviceDetails.

     

Execute estas etapas uma vez a cada dois ou três quadros para calcular novas configurações e aplicá-las. Neste exemplo, uma voz de origem está enviando diretamente para a voz de mestre e para uma voz submix com um efeito de reverberação aplicado a ela.

**Para usar o X3DAudio para calcular e aplicar novas configurações de áudio 3D**

1.  Atualize as estruturas do [**\_ emissor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) do X3DAUDIO e do [**\_ ouvinte**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) X3DAUDIO com sua posição, velocidade e orientação atuais.

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

    

2.  Chame [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) para calcular as novas configurações para as vozes.

    Os parâmetros para [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) serão as estruturas [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ emissor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) atualizadas. Os sinalizadores indicarão quais valores **X3DAudioCalculate** deve calcular e qual estrutura [**de \_ \_ configurações do DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) manterá os resultados dos cálculos executados.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar os valores de volume e de densidade à voz de origem.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para aplicar o nível de reverberação calculado à voz submix.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Use [**IXAudio2Voice:: Setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para aplicar o coeficiente de passagem baixa do filtro direto à voz de origem.

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

[Controle de volume e densidade XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
