---
description: Este tópico descreve como usar o Leitor de Origem no modo assíncrono.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Usando o leitor de origem no modo assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 514331f9d1635cbe83222ccf413b1dbb5a7d350b4656e23ed27ccede5c0be6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237501"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a>Usando o leitor de origem no modo assíncrono

Este tópico descreve como usar o Leitor de [Origem](source-reader.md) no modo assíncrono. No modo assíncrono, o aplicativo fornece uma interface de retorno de chamada, que é usada para notificar o aplicativo de que os dados estão disponíveis.

Este tópico pressu que você já tenha lido o tópico Usando o Leitor de [Origem para processar dados de mídia.](processing-media-data-with-the-source-reader.md)

## <a name="using-asynchronous-mode"></a>Usando o modo assíncrono

O Leitor de Origem opera no modo síncrono ou no modo assíncrono. O exemplo de código mostrado na seção anterior presume que o Leitor de Origem está usando o modo síncrono, que é o padrão. No modo síncrono, o método [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) bloqueia enquanto a fonte de mídia produz o próximo exemplo. Uma fonte de mídia normalmente adquire dados de alguma fonte externa (como um arquivo local ou uma conexão de rede), para que o método possa bloquear o thread de chamada por um período perceptível.

No modo assíncrono, [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retorna imediatamente e o trabalho é executado em outro thread. Depois que a operação for concluída, o Leitor de Origem chamará o aplicativo por meio da interface de retorno de chamada [**IMFSourceReaderCallback.**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) Para usar o modo assíncrono, você deve fornecer um ponteiro de retorno de chamada ao criar pela primeira vez o Leitor de Origem, da seguinte forma:

1.  Crie um armazenamento de atributos chamando a [**função MFCreateAttributes.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)
2.  De definir o atributo DE RETORNO DE [ \_ CHAMADA \_ \_ ASSÍNCRONO DO \_ LEITOR](mf-source-reader-async-callback.md) DE ORIGEM do MF no armazenamento de atributos. O valor do atributo é um ponteiro para o objeto de retorno de chamada.
3.  Ao criar o Leitor de Origem, passe o armazenamento de atributos para a função de criação no *parâmetro pAttributes.* Todas as funções para criar o Leitor de Origem têm esse parâmetro.

O exemplo a seguir mostra estas etapas.


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



Depois de criar o Leitor de Origem, não é possível alternar os modos entre síncronos e assíncronos.

Para obter dados no modo assíncrono, chame o método [**ReadSample,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) mas de definir os últimos quatro parâmetros como **NULL,** conforme mostrado no exemplo a seguir.


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



Quando o [**método ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) for concluído de forma assíncrona, o Leitor de Origem chamará o método [**IMFSourceReaderCallback::OnReadSample.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) Esse método tem cinco parâmetros:

-   *hrStatus*: contém um **valor HRESULT.** Esse é o mesmo valor que [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retornaria no modo síncrono. Se *hrStatus contiver* um código de erro, você poderá ignorar os parâmetros restantes.
-   *dwStreamIndex*, *dwStreamFlags,* llTimestamp e *pSample:* esses três parâmetros são equivalentes aos três últimos parâmetros [**em ReadSample.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) Eles contêm o número de fluxo, os sinalizadores de status [**e o ponteiro IMFSample,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) respectivamente.


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



Além disso, a interface de retorno de chamada define dois outros métodos:

-   [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent). Notifica o aplicativo quando determinados eventos ocorrem na fonte de mídia, como eventos de conexão de rede ou buffer.
-   [**OnFlush.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) Chamado quando o [**método Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) é concluído.

## <a name="implementing-the-callback-interface"></a>Implementando a interface de retorno de chamada

A interface de retorno de chamada deve ser thread-safe, porque [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) e os outros métodos de retorno de chamada são chamados de threads de trabalho.

Há várias abordagens diferentes que você pode usar ao implementar o retorno de chamada. Por exemplo, você pode fazer todo o trabalho dentro do retorno de chamada ou pode usar o retorno de chamada para notificar o aplicativo (por exemplo, sinalizando um handle de evento) e, em seguida, fazer o trabalho do thread do aplicativo.

O [**método OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) será chamado uma vez para cada chamada que você fizer ao método [**IMFSourceReader::ReadSample.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) Para obter o próximo exemplo, chame **ReadSample** novamente. Se ocorrer um erro, **OnReadSample** será chamado com um código de erro para o *parâmetro hrStatus.*

O exemplo a seguir mostra uma implementação mínima da interface de retorno de chamada. Primeiro, aqui está a declaração de uma classe que implementa a interface .


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



Neste exemplo, não estamos interessados nos métodos [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) e [**OnFlush,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) portanto, eles simplesmente retornam **S \_ OK.** A classe usa um alça de evento para sinalizar o aplicativo; esse handle é fornecido por meio do construtor.

Neste exemplo mínimo, o método [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) apenas imprime o carimbo de data/hora na janela do console. Em seguida, ele armazena o código de status e o sinalizador de fim de fluxo e sinaliza o alça de evento:


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



O código a seguir mostra que o aplicativo usaria essa classe de retorno de chamada para ler todos os quadros de vídeo de um arquivo de mídia:


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Leitor de Origem](source-reader.md)
</dt> </dl>

 

 



