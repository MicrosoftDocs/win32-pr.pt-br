---
description: Fluxos de Exclusive-Mode
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Fluxos de Exclusive-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7722dd3463346e976f30a77949f56026a2425624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920367"
---
# <a name="exclusive-mode-streams"></a>Fluxos de Exclusive-Mode

Conforme explicado anteriormente, se um aplicativo abrir um fluxo em modo exclusivo, o aplicativo terá o uso exclusivo do dispositivo de ponto de extremidade de áudio que reproduz ou registra o fluxo. Por outro lado, vários aplicativos podem compartilhar um dispositivo de ponto de extremidade de áudio abrindo fluxos de modo compartilhado no dispositivo.

O acesso de modo exclusivo a um dispositivo de áudio pode bloquear sons de sistema cruciais, impedir a interoperabilidade com outros aplicativos e, de outra forma, degradar a experiência do usuário. Para atenuar esses problemas, um aplicativo com um fluxo de modo exclusivo normalmente abandona o controle do dispositivo de áudio quando o aplicativo não é o processo em primeiro plano ou não é transmitido ativamente.

A latência de fluxo é o atraso que é inerente ao caminho de dados que conecta o buffer de ponto de extremidade de um aplicativo a um dispositivo de ponto de extremidade de áudio. Para um fluxo de renderização, a latência é o atraso máximo desde o momento em que um aplicativo grava um exemplo em um buffer de ponto de extremidade no momento em que o exemplo é ouvido pelos alto-falantes. Para um fluxo de captura, a latência é o atraso máximo desde o momento em que um som entra no microfone até a hora em que um aplicativo pode ler o exemplo desse som do buffer de ponto de extremidade.

Os aplicativos que usam fluxos de modo exclusivo geralmente fazem isso porque exigem latências baixas nos caminhos de dados entre os dispositivos de ponto de extremidade de áudio e os threads de aplicativo que acessam os buffers de ponto de extremidade. Normalmente, esses threads são executados com prioridade relativamente alta e se agendam para serem executados em intervalos periódicos próximos ou iguais ao intervalo periódico que separa as passagens de processamento sucessivas pelo hardware de áudio. Durante cada passagem, o hardware de áudio processa os novos dados nos buffers de ponto de extremidade.

Para alcançar as menores latências de fluxo, um aplicativo pode exigir hardware de áudio especial e um sistema de computador que está levemente carregado. A condução do hardware de áudio além de seus limites de tempo ou o carregamento do sistema com tarefas de alta prioridade concorrentes pode causar uma falha em um fluxo de áudio de baixa latência. Por exemplo, para um fluxo de renderização, pode ocorrer uma falha se o aplicativo não conseguir gravar em um buffer de ponto de extremidade antes de o hardware de áudio ler o buffer ou se o hardware não conseguir ler o buffer antes da hora em que o buffer está agendado para reprodução. Normalmente, um aplicativo destinado a ser executado em uma ampla variedade de hardwares de áudio e em uma ampla gama de sistemas deve relaxar seus requisitos de tempo suficientes para evitar problemas em todos os ambientes de destino.

O Windows Vista tem vários recursos para dar suporte a aplicativos que exigem fluxos de áudio de baixa latência. Conforme discutido nos [componentes de áudio do modo de usuário](user-mode-audio-components.md), os aplicativos que executam operações de tempo crítico podem chamar as funções do serviço do Agendador de classes de multimídia (MMCSS) para aumentar a prioridade do thread sem negar recursos de CPU a aplicativos de prioridade mais baixa. Além disso, o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) dá suporte a um \_ sinalizador AUDCLNT STREAMFLAGS \_ EVENTCALLBACK que permite que o thread de serviço de buffer de um aplicativo agende sua execução para ocorrer quando um novo buffer se tornar disponível no dispositivo de áudio. Usando esses recursos, um thread de aplicativo pode reduzir as incertezas sobre quando ele será executado, diminuindo assim o risco de falhas em um fluxo de áudio de baixa latência.

Os drivers para adaptadores de áudio mais antigos provavelmente usarão a DDI (interface de driver de dispositivo) WaveCyclic ou WavePci, enquanto os drivers para adaptadores de áudio mais novos têm maior probabilidade de oferecer suporte à DDI WaveRT. Para aplicativos de modo exclusivo, os drivers WaveRT podem fornecer melhor desempenho que os drivers WaveCyclic ou WavePci, mas os drivers de WaveRT exigem recursos de hardware adicionais. Esses recursos incluem a capacidade de compartilhar buffers de hardware diretamente com aplicativos. Com o compartilhamento direto, nenhuma intervenção do sistema é necessária para transferir dados entre um aplicativo de modo exclusivo e o hardware de áudio. Por outro lado, os drivers WaveCyclic e WavePci são adequados para adaptadores de áudio mais antigos e com menos capacidade. Esses adaptadores dependem do software do sistema para transportar blocos de dados (anexados a pacotes de solicitação de e/s do sistema ou IRPs) entre buffers de aplicativo e buffers de hardware. Além disso, os dispositivos de áudio USB dependem do software do sistema para transportar dados entre buffers de aplicativo e buffers de hardware. Para melhorar o desempenho de aplicativos de modo exclusivo que se conectam a dispositivos de áudio que dependem do sistema para o transporte de dados, o WASAPI aumenta automaticamente a prioridade dos threads do sistema que transferem dados entre os aplicativos e o hardware. O WASAPI usa o MMCSS para aumentar a prioridade do thread. No Windows Vista, se um thread do sistema gerencia o transporte de dados para um fluxo de reprodução de áudio de modo exclusivo com um formato PCM e um período de dispositivo inferior a 10 milissegundos, o WASAPI atribui o nome da tarefa do MMCSS "áudio pro" ao thread. Se o período do dispositivo do fluxo for maior ou igual a 10 milissegundos, o WASAPI atribuirá o nome da tarefa do MMCSS "áudio" ao thread. Para obter mais informações sobre WaveCyclic, WavePci e WaveRT DDIs, consulte a documentação do Windows DDK. Para obter informações sobre como selecionar um período de dispositivo apropriado, consulte [**IAudioClient:: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).

Conforme descrito em [controles de volume de sessão](session-volume-controls.md), o [WASAPI](wasapi.md) fornece as interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para controlar os níveis de volume de fluxos de áudio de modo compartilhado. No entanto, os controles nessas interfaces não têm nenhum efeito em fluxos de modo exclusivo. Em vez disso, os aplicativos que gerenciam fluxos de modo exclusivo normalmente usam a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) na [API EndpointVolume](endpointvolume-api.md) para controlar os níveis de volume desses fluxos. Para obter informações sobre essa interface, consulte [controles de volume do ponto de extremidade](endpoint-volume-controls.md).

Para cada dispositivo de reprodução e dispositivo de captura no sistema, o usuário pode controlar se o dispositivo pode ser usado em modo exclusivo. Se o usuário desabilitar o uso de modo exclusivo do dispositivo, o dispositivo poderá ser usado para reproduzir ou gravar somente fluxos de modo compartilhado.

Se o usuário habilitar o uso de modo exclusivo do dispositivo, o usuário também poderá controlar se uma solicitação por um aplicativo para usar o dispositivo em modo exclusivo tomará a preempção do uso do dispositivo por aplicativos que podem estar atualmente em execução ou gravando fluxos de modo compartilhado por meio do dispositivo. Se a preempção estiver habilitada, uma solicitação por um aplicativo para assumir o controle exclusivo do dispositivo terá êxito se o dispositivo não estiver em uso no momento ou se o dispositivo estiver sendo usado no modo compartilhado, mas a solicitação falhará se outro aplicativo já tiver controle exclusivo do dispositivo. Se a preempção estiver desabilitada, uma solicitação por um aplicativo para assumir o controle exclusivo do dispositivo terá êxito se o dispositivo não estiver em uso no momento, mas a solicitação falhará se o dispositivo já estiver sendo usado no modo compartilhado ou em modo exclusivo.

No Windows Vista, as configurações padrão para um dispositivo de ponto de extremidade de áudio são as seguintes:

-   O dispositivo pode ser usado para reproduzir ou registrar fluxos de modo exclusivo.
-   Uma solicitação para usar um dispositivo para reproduzir ou gravar um fluxo de modo exclusivo preempção de qualquer fluxo de modo compartilhado que esteja sendo reproduzido ou registrado por meio do dispositivo.

**Para alterar as configurações de modo exclusivo de um dispositivo de reprodução ou de gravação**

1.  Clique com o botão direito do mouse no ícone do orador na área de notificação, que está localizada no lado direito da barra de tarefas e selecione **dispositivos de reprodução** ou **dispositivos de gravação**. (Como alternativa, execute o painel de controle multimídia do Windows Mmsys.cpl, em uma janela de prompt de comando. Para obter mais informações, consulte comentários [nas \_ constantes do estado do dispositivo \_ xxx](device-state-xxx-constants.md).)
2.  Depois que a janela de **som** for exibida, selecione **reprodução** ou **gravação**. Em seguida, selecione uma entrada na lista de nomes de dispositivo e clique em **Propriedades**.
3.  Depois que a janela **Propriedades** for exibida, clique em **avançado**.
4.  Para permitir que os aplicativos usem o dispositivo em modo exclusivo, marque a caixa rotulada **permitir que os aplicativos assumam o controle exclusivo desse dispositivo**. Para desabilitar o uso de modo exclusivo do dispositivo, desmarque a caixa de seleção.
5.  Se o uso de modo exclusivo do dispositivo estiver habilitado, você poderá especificar se uma solicitação de controle exclusivo do dispositivo terá sucesso se o dispositivo estiver atualmente em execução ou gravando fluxos de modo compartilhado. Para dar prioridade aos aplicativos de modo exclusivo sobre aplicativos de modo compartilhado, marque a caixa rotulada **fornecer prioridade de aplicativos em modo exclusivo**. Para negar a prioridade de aplicativos de modo exclusivo em aplicativos de modo compartilhado, desmarque a caixa de seleção.

O exemplo de código a seguir mostra como reproduzir um fluxo de áudio de baixa latência em um dispositivo de renderização de áudio configurado para uso no modo exclusivo:


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    DWORD taskIndex = 0;
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



No exemplo de código anterior, a função PlayExclusiveStream é executada no thread do aplicativo que Services armazena os buffers de ponto de extremidade enquanto um fluxo de renderização é reproduzido. A função usa um único parâmetro, pMySource, que é um ponteiro para um objeto que pertence a uma classe definida pelo cliente, myaudioname. Essa classe tem duas funções de membro, LoadData e SetFormat, que são chamadas no exemplo de código. Myaudioname é descrito na [renderização de um fluxo](rendering-a-stream.md).

A função PlayExclusiveStream chama uma função auxiliar, GetStreamFormat, que negocia com o dispositivo de processamento padrão para determinar se o dispositivo dá suporte a um formato de fluxo de modo exclusivo que é adequado para uso pelo aplicativo. O código para a função GetStreamFormat não aparece no exemplo de código; Isso ocorre porque os detalhes de sua implementação dependem inteiramente dos requisitos do aplicativo. No entanto, a operação da função GetStreamFormat pode ser descrita simplesmente — chama o método [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) uma ou mais vezes para determinar se o dispositivo dá suporte a um formato adequado. Os requisitos do aplicativo ditam quais formatos o GetStreamFormat apresenta ao método **IsFormatSupported** e a ordem em que ele os apresenta. Para obter mais informações sobre **IsFormatSupported**, consulte [formatos de dispositivo](device-formats.md).

Após a chamada GetStreamFormat, a função PlayExclusiveStream chama o método [**IAudioClient:: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) para obter o período mínimo de dispositivos com suporte pelo hardware de áudio. Em seguida, a função chama o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para solicitar uma duração de buffer igual ao período mínimo. Se a chamada for realizada com sucesso, o método **Initialize** alocará dois buffers de ponto de extremidade, cada um deles com duração igual ao período mínimo. Posteriormente, quando o fluxo de áudio começar a ser executado, o hardware de aplicativo e de áudio compartilhará os dois buffers na maneira "pingue-pongue", ou seja, enquanto o aplicativo grava em um buffer, o hardware lê do outro buffer.

Antes de iniciar o fluxo, a função PlayExclusiveStream faz o seguinte:

-   Cria e registra o identificador de evento por meio do qual ele receberá notificações quando os buffers estiverem prontos para preenchimento.
-   Preenche o primeiro buffer com dados da fonte de áudio para reduzir o atraso de quando o fluxo começa a ser executado quando o som inicial é ouvido.
-   Chama a função **AvSetMmThreadCharacteristics** para solicitar que o MMCSS aumente a prioridade do thread no qual o PlayExclusiveStream é executado. (Quando o fluxo para a execução, a chamada de função **AvRevertMmThreadCharacteristics** restaura a prioridade do thread original.)

Para obter mais informações sobre **AvSetMmThreadCharacteristics** e **AvRevertMmThreadCharacteristics**, consulte a documentação do SDK do Windows.

Enquanto o fluxo está em execução, cada iteração do loop **while** no exemplo de código anterior preenche um buffer de ponto de extremidade. Entre as iterações, a chamada de função **WaitForSingleObject** aguarda o identificador de evento ser sinalizado. Quando o identificador é sinalizado, o corpo do loop faz o seguinte:

1.  Chama o método [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) para obter o próximo buffer.
2.  Preenche o buffer.
3.  Chama o método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) para liberar o buffer.

Para obter mais informações sobre o **WaitForSingleObject**, consulte a documentação do SDK do Windows.

Se o adaptador de áudio for controlado por um driver WaveRT, a sinalização do identificador de evento será vinculada às notificações de transferência de DMA do hardware de áudio. Para um dispositivo de áudio USB, ou para um dispositivo de áudio que é controlado por um driver WaveCyclic ou WavePci, a sinalização do identificador de evento é vinculada a conclusões do IRPs que transferem dados do buffer de aplicativo para o buffer de hardware.

O exemplo de código anterior envia por push o hardware de áudio e o sistema de computador para seus limites de desempenho. Primeiro, para reduzir a latência do fluxo, o aplicativo agenda seu thread de serviço de buffer para usar o período mínimo do dispositivo ao qual o hardware de áudio dará suporte. Em segundo lugar, para garantir que o thread seja executado de forma confiável em cada período do dispositivo, a chamada de função **AvSetMmThreadCharacteristics** define o parâmetro TaskName como "Pro Audio", que é, no Windows Vista, o nome da tarefa padrão com a prioridade mais alta. Considere se os requisitos de tempo de seu aplicativo podem ser relaxados sem comprometer sua utilidade. Por exemplo, o aplicativo pode agendar seu thread de serviço de buffer para usar um período maior que o mínimo. Um período mais longo pode permitir com segurança o uso de uma prioridade de thread inferior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de fluxo](stream-management.md)
</dt> </dl>

 

 



