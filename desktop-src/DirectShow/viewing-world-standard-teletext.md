---
description: Exibindo o World Standard Teletext
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Exibindo o World Standard Teletext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2129538d91a7ac48fea26fd5f1987473896760c164fb3e2b1d4a2b1d142a1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078537"
---
# <a name="viewing-world-standard-teletext"></a>Exibindo o World Standard Teletext

> [!Note]  
> Essa funcionalidade foi removida do Windows Vista e sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

O WST (World Standard Teletext) é codificado no VBI (intervalo de espaço em branco vertical) do sinal de tv análogo. O grafo de filtro para visualizar o teletexto é semelhante ao grafo usado para exibir legendas fechadas. O diagrama a seguir ilustra esse grafo.

![gráfico de visualização do wst](images/vidcap10.png)

Este grafo usa os seguintes filtros para exibição WST:

-   [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md). Aceita as informações da VBI do filtro de captura e as divide em fluxos separados para cada um dos serviços de dados presentes no sinal.
-   [Codec do WST.](wst-codec-filter.md) Decodifica os dados Teletext dos exemplos de VBI.
-   [Decodificador WST](wst-decoder-filter.md). Converte dados de teletexto e desenha o texto em bitmaps. O filtro downstream (nesse caso, o Mixer sobreposição) sobrepõe os bitmaps no vídeo.

O método **RenderStream** do Capture Graph Builder não dá suporte diretamente aos filtros WST, portanto, seu aplicativo deve fazer algum trabalho extra.

1.  Adicione o filtro sobreposição Mixer ao grafo de filtro. O código a seguir usa a função AddFilterByCLSID descrita em [Adicionar um filtro por CLSID.](add-a-filter-by-clsid.md) (AddFilterByCLSID não é uma API DirectShow.)
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Conexão o pin de visualização para o filtro do Renderador de Vídeo por meio do filtro Sobreposição Mixer. Você pode usar o **método RenderStream,** da seguinte forma:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Adicione o filtro Tee/Sink-to-Sink Converter ao grafo de filtro. O código a seguir usa a função CreateKernelFilter descrita em [Criando Kernel-Mode Filtros](creating-kernel-mode-filters.md). (CreateKernelFilter não é uma API DirectShow.)
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Adicione o filtro codec do WST ao grafo de filtro:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Chame **RenderStream** para conectar o pino de VBI do filtro de captura ao Conversor Tee/Sink-to-Sink e o Conversor Tee/Sink-to-Sink ao filtro codec do WST:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Chame **RenderStream novamente** para conectar o filtro codec do WST ao filtro sobreposição Mixer. O filtro de decodificador WST é automaticamente trazido para o grafo.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  Lembre-se de liberar todas as interfaces de filtro.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Atualmente, o filtro de decodificador WST não dá suporte a conexões com o filtro VMR (Video Mixing Renderer). Portanto, você deve usar o filtro renderador de vídeo herdado para exibir o teletexto.

 

Se o filtro de captura tiver um pino de VBI de porta de vídeo (PIN \_ CATEGPORY VIDEOPORT VBI), conecte-o ao filtro alocador de superfície \_ \_ da [VBI.](vbi-surface-allocator.md) Caso contrário, o grafo não será executado corretamente. O exemplo de código a seguir usa a função AddFilterByCLSID, descrita em Adicionar um filtro por [CLSID](add-a-filter-by-clsid.md)e a função FindPinByCategory, descrita em Trabalhando com categorias de [pino](working-with-pin-categories.md). (Nenhuma função é uma API DirectShow.)


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Legendas fechadas e teletexto](closed-captions-and-teletext.md)
</dt> </dl>

 

 



