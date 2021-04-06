---
description: Capturando um fluxo
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Capturando um fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826436"
---
# <a name="capturing-a-stream"></a><span data-ttu-id="f4b63-103">Capturando um fluxo</span><span class="sxs-lookup"><span data-stu-id="f4b63-103">Capturing a Stream</span></span>

<span data-ttu-id="f4b63-104">O cliente chama os métodos na interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) para ler dados capturados de um buffer de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f4b63-104">The client calls the methods in the [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface to read captured data from an endpoint buffer.</span></span> <span data-ttu-id="f4b63-105">O cliente compartilha o buffer de ponto de extremidade com o mecanismo de áudio no modo compartilhado e com o dispositivo de áudio em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f4b63-105">The client shares the endpoint buffer with the audio engine in shared mode and with the audio device in exclusive mode.</span></span> <span data-ttu-id="f4b63-106">Para solicitar um buffer de ponto de extremidade de um tamanho específico, o cliente chama o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="f4b63-106">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="f4b63-107">Para obter o tamanho do buffer alocado, que pode ser diferente do tamanho solicitado, o cliente chama o método [**IAudioClient:: getbuffersize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="f4b63-107">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="f4b63-108">Para mover um fluxo de dados capturados por meio do buffer de ponto de extremidade, o cliente chama o método [**IAudioCaptureClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e o método [**IAudioCaptureClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) de forma alternativa.</span><span class="sxs-lookup"><span data-stu-id="f4b63-108">To move a stream of captured data through the endpoint buffer, the client alternately calls the [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) method and the [**IAudioCaptureClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) method.</span></span> <span data-ttu-id="f4b63-109">O cliente acessa os dados no buffer de ponto de extremidade como uma série de pacotes de dados.</span><span class="sxs-lookup"><span data-stu-id="f4b63-109">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="f4b63-110">A chamada **GetBuffer** recupera o próximo pacote de dados capturados do buffer.</span><span class="sxs-lookup"><span data-stu-id="f4b63-110">The **GetBuffer** call retrieves the next packet of captured data from the buffer.</span></span> <span data-ttu-id="f4b63-111">Depois de ler os dados do pacote, o cliente chama **ReleaseBuffer** para liberar o pacote e disponibilizá-lo para dados mais capturados.</span><span class="sxs-lookup"><span data-stu-id="f4b63-111">After reading the data from the packet, the client calls **ReleaseBuffer** to release the packet and make it available for more captured data.</span></span>

<span data-ttu-id="f4b63-112">O tamanho do pacote pode variar de uma chamada [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) para a próxima.</span><span class="sxs-lookup"><span data-stu-id="f4b63-112">The packet size can vary from one [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) call to the next.</span></span> <span data-ttu-id="f4b63-113">Antes de chamar **GetBuffer**, o cliente tem a opção de chamar o método [**IAudioCaptureClient:: GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) para obter o tamanho do próximo pacote com antecedência.</span><span class="sxs-lookup"><span data-stu-id="f4b63-113">Before calling **GetBuffer**, the client has the option of calling the [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) method to get the size of the next packet in advance.</span></span> <span data-ttu-id="f4b63-114">Além disso, o cliente pode chamar o método [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) para obter a quantidade total de dados capturados que estão disponíveis no buffer.</span><span class="sxs-lookup"><span data-stu-id="f4b63-114">In addition, the client can call the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method to get the total amount of captured data that is available in the buffer.</span></span> <span data-ttu-id="f4b63-115">A qualquer instante, o tamanho do pacote é sempre menor ou igual à quantidade total de dados capturados no buffer.</span><span class="sxs-lookup"><span data-stu-id="f4b63-115">At any instant, the packet size is always less than or equal to the total amount of captured data in the buffer.</span></span>

<span data-ttu-id="f4b63-116">Durante cada passagem de processamento, o cliente tem a opção de processar os dados capturados de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="f4b63-116">During each processing pass, the client has the option of processing the captured data in one of the following ways:</span></span>

-   <span data-ttu-id="f4b63-117">O cliente chama, de forma alternativa, [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), lendo um pacote com cada par de chamadas, até que **GetBuffer** retorne AUDCNT \_ S \_ BUFFEREMPTY, indicando que o buffer está vazio.</span><span class="sxs-lookup"><span data-stu-id="f4b63-117">The client alternately calls [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), reading one packet with each pair of calls, until **GetBuffer** returns AUDCNT\_S\_BUFFEREMPTY, indicating that the buffer is empty.</span></span>
-   <span data-ttu-id="f4b63-118">O cliente chama [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) antes de cada par de chamadas para [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) até que **GetNextPacketSize** relate um tamanho de pacote de 0, indicando que o buffer está vazio.</span><span class="sxs-lookup"><span data-stu-id="f4b63-118">The client calls [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) before each pair of calls to [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) until **GetNextPacketSize** reports a packet size of 0, indicating that the buffer is empty.</span></span>

<span data-ttu-id="f4b63-119">As duas técnicas produzem resultados equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f4b63-119">The two techniques yield equivalent results.</span></span>

<span data-ttu-id="f4b63-120">O exemplo de código a seguir mostra como registrar um fluxo de áudio do dispositivo de captura padrão:</span><span class="sxs-lookup"><span data-stu-id="f4b63-120">The following code example shows how to record an audio stream from the default capture device:</span></span>


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



<span data-ttu-id="f4b63-121">No exemplo anterior, a função RecordAudioStream usa um único parâmetro, `pMySink` , que é um ponteiro para um objeto que pertence a uma classe definida pelo cliente, MyAudioSink, com duas funções, CopyData e SetFormat.</span><span class="sxs-lookup"><span data-stu-id="f4b63-121">In the preceding example, the RecordAudioStream function takes a single parameter, `pMySink`, which is a pointer to an object that belongs to a client-defined class, MyAudioSink, with two functions, CopyData and SetFormat.</span></span> <span data-ttu-id="f4b63-122">O código de exemplo não inclui a implementação de MyAudioSink porque:</span><span class="sxs-lookup"><span data-stu-id="f4b63-122">The example code does not include the implementation of MyAudioSink because:</span></span>

-   <span data-ttu-id="f4b63-123">Nenhum dos membros da classe se comunica diretamente com qualquer um dos métodos nas interfaces no WASAPI.</span><span class="sxs-lookup"><span data-stu-id="f4b63-123">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="f4b63-124">A classe pode ser implementada de várias maneiras, dependendo dos requisitos do cliente.</span><span class="sxs-lookup"><span data-stu-id="f4b63-124">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="f4b63-125">(Por exemplo, ele pode gravar os dados de captura em um arquivo WAV.)</span><span class="sxs-lookup"><span data-stu-id="f4b63-125">(For example, it might write the capture data to a WAV file.)</span></span>

<span data-ttu-id="f4b63-126">No entanto, as informações sobre a operação dos dois métodos são úteis para entender o exemplo.</span><span class="sxs-lookup"><span data-stu-id="f4b63-126">However, information about the operation of the two methods is useful for understanding the example.</span></span>

<span data-ttu-id="f4b63-127">A função CopyData copia um número especificado de quadros de áudio de um local de buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="f4b63-127">The CopyData function copies a specified number of audio frames from a specified buffer location.</span></span> <span data-ttu-id="f4b63-128">A função RecordAudioStream usa a função CopyData para ler e salvar os dados de áudio do buffer compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f4b63-128">The RecordAudioStream function uses the CopyData function to read and save the audio data from the shared buffer.</span></span> <span data-ttu-id="f4b63-129">A função SetFormat especifica o formato da função CopyData a ser usada para os dados.</span><span class="sxs-lookup"><span data-stu-id="f4b63-129">The SetFormat function specifies the format for the CopyData function to use for the data.</span></span>

<span data-ttu-id="f4b63-130">Desde que o objeto MyAudioSink exija dados adicionais, a função CopyData gera o valor **false** por meio de seu terceiro parâmetro, que, no exemplo de código anterior, é um ponteiro para a variável `bDone` .</span><span class="sxs-lookup"><span data-stu-id="f4b63-130">As long as the MyAudioSink object requires additional data, the CopyData function outputs the value **FALSE** through its third parameter, which, in the preceding code example, is a pointer to the variable `bDone`.</span></span> <span data-ttu-id="f4b63-131">Quando o objeto MyAudioSink tem todos os dados necessários, a função CopyData define `bDone` como **true**, o que faz com que o programa saia do loop na função RecordAudioStream.</span><span class="sxs-lookup"><span data-stu-id="f4b63-131">When the MyAudioSink object has all the data that it requires, the CopyData function sets `bDone` to **TRUE**, which causes the program to exit the loop in the RecordAudioStream function.</span></span>

<span data-ttu-id="f4b63-132">A função RecordAudioStream aloca um buffer compartilhado que tem uma duração de um segundo.</span><span class="sxs-lookup"><span data-stu-id="f4b63-132">The RecordAudioStream function allocates a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="f4b63-133">(O buffer alocado pode ter uma duração um pouco maior.) Dentro do loop principal, a chamada para a função de [**suspensão**](/windows/desktop/api/synchapi/nf-synchapi-sleep) do Windows faz com que o programa Aguarde por meio de um segundo.</span><span class="sxs-lookup"><span data-stu-id="f4b63-133">(The allocated buffer might have a slightly longer duration.) Within the main loop, the call to the Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) function causes the program to wait for a half second.</span></span> <span data-ttu-id="f4b63-134">No início de cada chamada de **suspensão** , o buffer compartilhado está vazio ou quase vazio.</span><span class="sxs-lookup"><span data-stu-id="f4b63-134">At the start of each **Sleep** call, the shared buffer is empty or nearly empty.</span></span> <span data-ttu-id="f4b63-135">No momento em que a chamada de **suspensão** retorna, o buffer compartilhado é cerca de metade preenchida com dados de captura.</span><span class="sxs-lookup"><span data-stu-id="f4b63-135">By the time the **Sleep** call returns, the shared buffer is about half filled with capture data.</span></span>

<span data-ttu-id="f4b63-136">Seguindo a chamada para o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , o fluxo permanece aberto até que o cliente libere todas as suas referências para a interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e todas as referências a interfaces de serviço que o cliente obteve por meio do método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="f4b63-136">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="f4b63-137">A chamada de [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) final fecha o fluxo.</span><span class="sxs-lookup"><span data-stu-id="f4b63-137">The final [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4b63-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4b63-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4b63-139">Gerenciamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="f4b63-139">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
