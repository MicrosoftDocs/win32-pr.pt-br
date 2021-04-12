---
description: Renderizando um fluxo
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Renderizando um fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96e720bab43c75b0a3958bb3b6137d3a3d9ef6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457064"
---
# <a name="rendering-a-stream"></a>Renderizando um fluxo

O cliente chama os métodos na interface [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) para gravar dados de renderização em um buffer de ponto de extremidade. Para um fluxo de modo compartilhado, o cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio. Para um fluxo de modo exclusivo, o cliente compartilha o buffer de ponto de extremidade com o dispositivo de áudio. Para solicitar um buffer de ponto de extremidade de um tamanho específico, o cliente chama o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Para obter o tamanho do buffer alocado, que pode ser diferente do tamanho solicitado, o cliente chama o método [**IAudioClient:: getbuffersize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Para mover um fluxo de dados de renderização por meio do buffer de ponto de extremidade, o cliente chama o método [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e o método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) de forma alternativa. O cliente acessa os dados no buffer de ponto de extremidade como uma série de pacotes de dados. A chamada **GetBuffer** recupera o próximo pacote para que o cliente possa preenchê-lo com dados de renderização. Depois de gravar os dados no pacote, o cliente chama **ReleaseBuffer** para adicionar o pacote concluído à fila de renderização.

Para um buffer de renderização, o valor de preenchimento que é relatado pelo método [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) representa a quantidade de dados de renderização que são enfileirados para reprodução no buffer. Um aplicativo de renderização pode usar o valor de preenchimento para determinar o quanto novos dados podem ser gravados com segurança no buffer sem o risco de substituir os dados gravados anteriormente que o mecanismo de áudio ainda não leu do buffer. O espaço disponível é simplesmente o tamanho do buffer menos o tamanho do preenchimento. O cliente pode solicitar um tamanho de pacote que represente um ou todo esse espaço disponível em sua próxima chamada [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) .

O tamanho de um pacote é expresso em *quadros de áudio*. Um quadro de áudio em um fluxo PCM é um conjunto de amostras (o conjunto contém uma amostra para cada canal no fluxo) que é reproduzida ou registrada ao mesmo tempo (tique-relógio). Assim, o tamanho de um quadro de áudio é o tamanho da amostra multiplicado pelo número de canais no fluxo. Por exemplo, o tamanho do quadro para um fluxo estéreo (2 canais) com amostras de 16 bits é de quatro bytes.

O exemplo de código a seguir mostra como reproduzir um fluxo de áudio no dispositivo de renderização padrão:


```C++
//-----------------------------------------------------------
// Play an audio stream on the default audio rendering
// device. The PlayAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data to the
// rendering device. The inner loop runs every 1/2 second.
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

HRESULT PlayAudioStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    UINT32 numFramesPadding;
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

    hr = pAudioClient->GetMixFormat(&pwfx);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_SHARED,
                         0,
                         hnsRequestedDuration,
                         0,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Get the actual size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // Grab the entire buffer for the initial fill operation.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    // Load the initial data into the shared buffer.
    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                        bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Sleep for half the buffer duration.
        Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

        // See how much buffer space is available.
        hr = pAudioClient->GetCurrentPadding(&numFramesPadding);
        EXIT_ON_ERROR(hr)

        numFramesAvailable = bufferFrameCount - numFramesPadding;

        // Grab all the available space in the shared buffer.
        hr = pRenderClient->GetBuffer(numFramesAvailable, &pData);
        EXIT_ON_ERROR(hr)

        // Get next 1/2-second of data from the audio source.
        hr = pMySource->LoadData(numFramesAvailable, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(numFramesAvailable, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for last data in buffer to play before stopping.
    Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



No exemplo anterior, a função PlayAudioStream usa um único parâmetro, `pMySource` , que é um ponteiro para um objeto que pertence a uma classe definida pelo cliente, Myaudioname, com duas funções de membro, LoadData e SetFormat. O código de exemplo não inclui a implementação de myaudioname porque:

-   Nenhum dos membros da classe se comunica diretamente com qualquer um dos métodos nas interfaces no WASAPI.
-   A classe pode ser implementada de várias maneiras, dependendo dos requisitos do cliente. (Por exemplo, ele pode ler os dados de renderização de um arquivo WAV e executar a conversão imediata no formato de fluxo.)

No entanto, algumas informações sobre a operação das duas funções são úteis para entender o exemplo.

A função LoadData grava um número especificado de quadros de áudio (primeiro parâmetro) em um local de buffer especificado (segundo parâmetro). (O tamanho de um quadro de áudio é o número de canais no fluxo multiplicado pelo tamanho da amostra.) A função PlayAudioStream usa LoadData para preencher partes do buffer compartilhado com dados de áudio. A função SetFormat especifica o formato da função LoadData a ser usada para os dados. Se a função LoadData for capaz de gravar pelo menos um quadro no local do buffer especificado, mas ficar sem dados antes de gravar o número especificado de quadros, ele gravará silêncio nos quadros restantes.

Desde que LoadData tenha sido realizado com sucesso ao gravar pelo menos um quadro de dados reais (não silenciar) para o local de buffer especificado, ele gera 0 por meio de seu terceiro parâmetro, que, no exemplo de código anterior, é um ponteiro de saída para a `flags` variável. Quando LoadData estiver sem dados e não puder gravar até mesmo um único quadro no local de buffer especificado, ele não gravará nada no buffer (nem mesmo em silêncio) e gravará o valor AUDCLNT \_ BUFFERFLAGS \_ Silent na `flags` variável. A `flags` variável transmite esse valor para o método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , que responde preenchendo o número especificado de quadros no buffer com silêncio.

Em sua chamada ao método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , a função PlayAudioStream no exemplo anterior solicita um buffer compartilhado que tem uma duração de um segundo. (O buffer alocado pode ter uma duração um pouco maior.) Em suas chamadas iniciais para os métodos [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , a função preenche o buffer inteiro antes de chamar o método [**IAudioClient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) para começar a reproduzir o buffer.

No loop principal, a função preenche com iteração a metade do buffer em intervalos de meio segundo. Logo antes de cada chamada para a função de [**suspensão**](/windows/win32/api/synchapi/nf-synchapi-sleep) do Windows no loop principal, o buffer está cheio ou quase cheio. Quando a chamada de **suspensão** retorna, o buffer está cerca de metade cheia. O loop termina depois que a chamada final para a função LoadData define a `flags` variável como o valor AUDCLNT \_ BUFFERFLAGS \_ Silent. Nesse ponto, o buffer contém pelo menos um quadro de dados reais, e ele pode conter até um meio segundo de dados reais. O restante do buffer contém silêncio. A chamada de **suspensão** que segue o loop fornece tempo suficiente (um meio segundo) para reproduzir todos os dados restantes. O silêncio que segue os dados impede sons indesejados antes que a chamada para o método [**IAudioClient:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) pare o fluxo de áudio. Para obter mais informações sobre **suspensão**, consulte a documentação do SDK do Windows.

Seguindo a chamada para o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , o fluxo permanece aberto até que o cliente libere todas as suas referências para a interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e todas as referências a interfaces de serviço que o cliente obteve por meio do método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . A chamada de [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) final fecha o fluxo.

A função PlayAudioStream no exemplo de código anterior chama a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um enumerador para os dispositivos de ponto de extremidade de áudio no sistema. A menos que o programa de chamada chamou anteriormente a função **CoCreateInstance** ou [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com, a chamada **CoCreateInstance** falhará. Para obter mais informações sobre **CoCreateInstance**, **CoCreateInstance** e **CoInitializeEx**, consulte a documentação do SDK do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de fluxo](stream-management.md)
</dt> </dl>

 

 
