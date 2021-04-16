---
description: O filtro de apoio de exemplo é um filtro de transformação que pode ser usado para obter amostras de mídia de um fluxo à medida que eles passam pelo gráfico de filtro.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Usando o exemplo de apoio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758505"
---
# <a name="using-the-sample-grabber"></a>Usando o exemplo de apoio

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

O filtro de [**apoio de exemplo**](sample-grabber-filter.md) é um filtro de transformação que pode ser usado para obter amostras de mídia de um fluxo à medida que eles passam pelo gráfico de filtro.

Se você simplesmente deseja pegar um bitmap de um arquivo de vídeo, é mais fácil usar o objeto [detector de mídia (MediaDet)](media-detector--mediadet.md) . Consulte [captando um quadro de cartaz](grabbing-a-poster-frame.md) para obter detalhes. No entanto, o exemplo de apoio é mais flexível porque funciona com quase qualquer tipo de mídia (consulte [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) para as poucas exceções) e oferece mais controle ao aplicativo.

-   [Criar o Gerenciador de gráfico de filtro](#create-the-filter-graph-manager)
-   [Adicionar o exemplo de apoio ao grafo de filtro](#add-the-sample-grabber-to-the-filter-graph)
-   [Definir o tipo de mídia](#set-the-media-type)
-   [Criar o grafo de filtro](#build-the-filter-graph)
-   [Executar o grafo](#run-the-graph)
-   [Obter o exemplo](#grab-the-sample)
-   [Código de exemplo](#example-code)
-   [Tópicos relacionados](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Criar o Gerenciador de gráfico de filtro

Para começar, crie o [Gerenciador do grafo de filtro](filter-graph-manager.md) e consulte as interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Adicionar o exemplo de apoio ao grafo de filtro

Crie uma instância do filtro de apoio de exemplo e addit para o grafo de filtro. Consulte o filtro de apoio de exemplo para a interface [**ISampleGrabber**](isamplegrabber.md) .


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a>Definir o tipo de mídia

Quando você cria o exemplo de apoio pela primeira vez, ele não tem nenhum tipo de mídia preferencial. Isso significa que você pode se conectar a praticamente qualquer filtro no grafo, mas não teria nenhum controle sobre o tipo de dados que ele recebeu. Antes de compilar o restante do grafo, portanto, você deve definir um tipo de mídia para o exemplo de apoio, chamando o método [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) .

Quando o elemento de exemplo se conecta, ele compara esse tipo de mídia com o tipo de mídia oferecido pelo outro filtro. Os únicos campos que ele verifica são o tipo principal, subtipo e tipo de formato. Para qualquer um deles, o valor GUID \_ null significa "aceitar qualquer valor". Na maioria das vezes, você desejará definir o tipo e subtipo principais. Por exemplo, o código a seguir especifica um vídeo RGB não compactado de 24 bits:


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a>Criar o grafo de filtro

Agora você pode criar o restante do gráfico de filtro. Como o exemplo de apoio se conectará apenas usando o tipo de mídia que você especificou, isso permite que você aproveite os mecanismos de [conexão inteligente](intelligent-connect.md) do Gerenciador de grafo de filtro ao criar o grafo.

Por exemplo, se você tiver especificado vídeo descompactado, poderá conectar um filtro de origem ao complemento de exemplo e o Gerenciador de gráfico de filtro adicionará automaticamente o analisador de arquivo e o decodificador. O exemplo a seguir usa a função auxiliar ConnectFilters, que está listada em [conectar dois filtros](connect-two-filters.md):


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





O exemplo de apoio é um filtro de transformação, portanto, o pino de saída deve estar conectado a outro filtro. Muitas vezes, talvez você queira simplesmente descartar os exemplos depois de concluí-los. Nesse caso, conecte o exemplo de apoio ao [**filtro de renderizador nulo**](null-renderer-filter.md), que descarta os dados que recebe.

O exemplo a seguir conecta o exemplo de apoio ao filtro de renderizador nulo:


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





Lembre-se de que colocar o exemplo de apoio entre um decodificador de vídeo e o renderizador de vídeo pode prejudicar significativamente o desempenho da renderização. O exemplo de amostra é um filtro de trans-in-Place, o que significa que o buffer de saída é o mesmo que o buffer de entrada. Para a renderização de vídeo, é provável que o buffer de saída esteja localizado na placa gráfica, em que as operações de leitura são muito mais lentas, comparadas com as operações de leitura na memória principal.

## <a name="run-the-graph"></a>Executar o grafo

O exemplo de apoio Opera em um dos dois modos:

-   O modo de buffer faz uma cópia de cada amostra antes de entregar o downstream de exemplo.
-   O modo de retorno de chamada invoca uma função de retorno de chamada definida pelo aplicativo em cada exemplo.

Este artigo descreve o modo de buffer. (Antes de usar o modo de retorno de chamada, lembre-se de que a função de retorno de chamada deve ser bastante limitada. Caso contrário, ele pode reduzir drasticamente o desempenho ou até mesmo causar deadlocks. Para obter mais informações, consulte [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).) Para ativar o modo de buffer, chame o método [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) com o valor **true**.

Opcionalmente, chame o método [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md) com o valor **true**. Isso faz com que o exemplo de apoio Pare depois de receber o primeiro exemplo de mídia, o que é útil se você quiser pegar um único quadro a partir do fluxo. Procure o tempo desejado, execute o grafo e aguarde o evento de [**\_ conclusão do EC**](ec-complete.md) . Observe que o nível de precisão do quadro depende da origem. Por exemplo, procurar um arquivo MPEG geralmente não é preciso de quadros.

Para executar o grafo o mais rápido possível, ative o relógio do grafo, conforme descrito em [definindo o relógio do grafo](setting-the-graph-clock.md).

O exemplo a seguir habilita o modo único e o modo de buffer, executa o gráfico de filtro e aguarda a conclusão.


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a>Obter o exemplo

No modo de buffer, o exemplo de apoio armazena uma cópia de cada amostra. O método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia o buffer em uma matriz alocada pelo chamador. Para determinar o tamanho da matriz que é necessária, primeiro chame **GetCurrentBuffer** com um ponteiro **nulo** para o endereço da matriz. Em seguida, aloque a matriz e chame o método uma segunda vez para copiar o buffer. O exemplo a seguir mostra estas etapas.


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



Você precisará saber o formato exato dos dados no buffer. Para obter essas informações, chame o método [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) . Esse método preenche uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) com o formato.

Para um fluxo de vídeo descompactado, as informações de formato estão contidas em uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . O exemplo a seguir mostra como obter as informações de formato de um fluxo de vídeo descompactado.


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> O exemplo de apoio não oferece suporte a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

 

## <a name="example-code"></a>Código de exemplo

Aqui está o código completo para os exemplos anteriores.

> [!Note]  
> Este exemplo usa a função [SafeRelease](../medfound/saferelease.md) para liberar ponteiros de interface.

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os serviços de edição do DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
