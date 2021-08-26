---
description: Capturando um fluxo
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Capturando um fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dda6fd8527acbfff4072a2b79854eca4c32541f57d462b6073f9f6f39854ddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059026"
---
# <a name="capturing-a-stream"></a>Capturando um fluxo

O cliente chama os métodos na interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) para ler dados capturados de um buffer de ponto de extremidade. O cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio no modo compartilhado e com o dispositivo de áudio no modo exclusivo. Para solicitar um buffer de ponto de extremidade de um tamanho específico, o cliente chama o [**método IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Para obter o tamanho do buffer alocado, que pode ser diferente do tamanho solicitado, o cliente chama o método [**IAudioClient::GetBufferSize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)

Para mover um fluxo de dados capturados pelo buffer do ponto de extremidade, o cliente chama como alternativa o método [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e o [**método IAudioCaptureClient::ReleaseBuffer.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) O cliente acessa os dados no buffer de ponto de extremidade como uma série de pacotes de dados. A **chamada GetBuffer** recupera o próximo pacote de dados capturados do buffer. Depois de ler os dados do pacote, o cliente chama **ReleaseBuffer** para liberar o pacote e torná-lo disponível para mais dados capturados.

O tamanho do pacote pode variar de uma [**chamada GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) para a próxima. Antes de chamar **GetBuffer**, o cliente tem a opção de chamar o método [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) para obter o tamanho do próximo pacote com antecedência. Além disso, o cliente pode chamar o método [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) para obter a quantidade total de dados capturados disponíveis no buffer. A qualquer momento, o tamanho do pacote é sempre menor ou igual à quantidade total de dados capturados no buffer.

Durante cada passagem de processamento, o cliente tem a opção de processar os dados capturados de uma das seguintes maneiras:

-   Como alternativa, o cliente chama [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), lendo um pacote com cada par de chamadas, até **que GetBuffer** retorne \_ BUFFEREMPTY do AUDCNT S, indicando que o \_ buffer está vazio.
-   O cliente chama [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) antes de cada par de chamadas para [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) até **que GetNextPacketSize** reporte um tamanho de pacote de 0, indicando que o buffer está vazio.

As duas técnicas produzem resultados equivalentes.

O exemplo de código a seguir mostra como registrar um fluxo de áudio do dispositivo de captura padrão:


```C++
//-----------------------------------------------------------
// Record an audio stream from the default audio capture
// device. The RecordAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data from the
// capture device. The main loop runs every 1/2 second.
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
const IID IID_IAudioCaptureClient = __uuidof(IAudioCaptureClient);

HRESULT RecordAudioStream(MyAudioSink *pMySink)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioCaptureClient *pCaptureClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 packetLength = 0;
    BOOL bDone = FALSE;
    BYTE *pData;
    DWORD flags;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eCapture, eConsole, &pDevice);
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

    // Get the size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioCaptureClient,
                         (void**)&pCaptureClient);
    EXIT_ON_ERROR(hr)

    // Notify the audio sink which format to use.
    hr = pMySink->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                     bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start recording.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (bDone == FALSE)
    {
        // Sleep for half the buffer duration.
        Sleep(hnsActualDuration/REFTIMES_PER_MILLISEC/2);

        hr = pCaptureClient->GetNextPacketSize(&packetLength);
        EXIT_ON_ERROR(hr)

        while (packetLength != 0)
        {
            // Get the available data in the shared buffer.
            hr = pCaptureClient->GetBuffer(
                                   &pData,
                                   &numFramesAvailable,
                                   &flags, NULL, NULL);
            EXIT_ON_ERROR(hr)

            if (flags & AUDCLNT_BUFFERFLAGS_SILENT)
            {
                pData = NULL;  // Tell CopyData to write silence.
            }

            // Copy the available capture data to the audio sink.
            hr = pMySink->CopyData(
                              pData, numFramesAvailable, &bDone);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->ReleaseBuffer(numFramesAvailable);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->GetNextPacketSize(&packetLength);
            EXIT_ON_ERROR(hr)
        }
    }

    hr = pAudioClient->Stop();  // Stop recording.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pCaptureClient)

    return hr;
}
```



No exemplo anterior, a função RecordAudioStream recebe um único parâmetro, , que é um ponteiro para um objeto que pertence a uma classe definida pelo `pMySink` cliente, MyAudioSink, com duas funções, CopyData e SetFormat. O código de exemplo não inclui a implementação de MyAudioSink porque:

-   Nenhum dos membros da classe se comunica diretamente com qualquer um dos métodos nas interfaces no WASAPI.
-   A classe pode ser implementada de várias maneiras, dependendo dos requisitos do cliente. (Por exemplo, ele pode gravar os dados de captura em um arquivo WAV.)

No entanto, as informações sobre a operação dos dois métodos são úteis para entender o exemplo.

A função CopyData copia um número especificado de quadros de áudio de um local de buffer especificado. A função RecordAudioStream usa a função CopyData para ler e salvar os dados de áudio do buffer compartilhado. A função SetFormat especifica o formato para a função CopyData a ser usada para os dados.

Desde que o objeto MyAudioSink exija dados adicionais, a função CopyData saída o valor **FALSE** por meio de seu terceiro parâmetro, que, no exemplo de código anterior, é um ponteiro para a variável `bDone` . Quando o objeto MyAudioSink tem todos os dados necessários, a função CopyData define como TRUE, o que faz com que o programa saia do loop na `bDone` função RecordAudioStream. 

A função RecordAudioStream aloca um buffer compartilhado que tem uma duração de um segundo. (O buffer alocado pode ter uma duração um pouco mais longa.) Dentro do loop principal, a chamada para a função Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) faz com que o programa aguarde um segundo. No início de cada **chamada de Sleep,** o buffer compartilhado está vazio ou quase vazio. No momento em que a **chamada** Sleep é retornada, o buffer compartilhado é aproximadamente metade preenchido com os dados de captura.

Após a chamada para o método [**IAudioClient::Initialize,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) o fluxo permanece aberto até que o cliente libere todas as suas referências à interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e a todas as referências às interfaces de serviço obtidas pelo cliente por meio do método [**IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) A chamada [**de versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) final fecha o fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Fluxo](stream-management.md)
</dt> </dl>

 

 
