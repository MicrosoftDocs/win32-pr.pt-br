---
description: Exibindo teletexto do mundo Standard
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Exibindo teletexto do mundo Standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296524"
---
# <a name="viewing-world-standard-teletext"></a>Exibindo teletexto do mundo Standard

> [!Note]  
> Essa funcionalidade foi removida do Windows Vista e de sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

O teletexto padrão mundial (WST) é codificado no intervalo vertical em branco (VBI) do sinal de televisão analógica. O grafo de filtro para visualização de teletexto é semelhante ao gráfico usado para exibir legendas ocultas. O diagrama a seguir ilustra esse grafo.

![Grafo de visualização de WST](images/vidcap10.png)

Este grafo usa os seguintes filtros para exibição de WST:

-   [Conversor de t/coletor de alto-para-coletor](tee-sink-to-sink-converter.md). Aceita as informações de VBI do filtro de captura e divide-as em fluxos separados para cada um dos serviços de dados presentes no sinal.
-   [Codec de WST](wst-codec-filter.md). Decodifica os dados do TELETEXT dos exemplos de VBI.
-   [Decodificador de WST](wst-decoder-filter.md). Traduz dados do TELETEXT e desenha o texto em bitmaps. O filtro downstream (nesse caso, o mixer de sobreposição) sobrepõe os bitmaps no vídeo.

O método **RenderStream** do construtor do grafo de captura não dá suporte a filtros de WST diretamente, portanto, seu aplicativo deve fazer algum trabalho extra.

1.  Adicione o filtro do mixer de sobreposição ao gráfico de filtro. O código a seguir usa a função AddFilterByCLSID descrita em [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md). (AddFilterByCLSID não é uma API do DirectShow.)
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Conecte o pino de visualização ao filtro de processador de vídeo por meio do mixer de sobreposição. Você pode usar o método **RenderStream** , da seguinte maneira:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Adicione o filtro de conversor de Altova/coletor para coletor ao grafo de filtro. O código a seguir usa a função CreateKernelFilter descrita em [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md). (CreateKernelFilter não é uma API do DirectShow.)
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Adicione o filtro de codec de WST ao gráfico de filtro:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Chame **RenderStream** para conectar o PIN do VBI do filtro de captura ao conversor de alto/coletor-para-coletor e o conversor de alto/coletor para coletor para o filtro de codec de WST:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Chame **RenderStream** novamente para conectar o filtro de codec de WST ao mixer de sobreposição. O filtro de decodificador de WST é automaticamente colocado no grafo.
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
> Atualmente, o filtro de decodificador de WST não oferece suporte a conexões com o filtro de processador de mixagem de vídeo (VMR). Portanto, você deve usar o filtro de renderização de vídeo herdado para exibir o teletexto.

 

Se o filtro de captura tiver uma porta de vídeo VBI PIN (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI), conecte-o ao filtro de [alocador de superfície de VBI](vbi-surface-allocator.md) . Caso contrário, o grafo não será executado corretamente. O exemplo de código a seguir usa a função AddFilterByCLSID, descrita em [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md), e a função FindPinByCategory, descrita em [trabalhando com categorias de PIN](working-with-pin-categories.md). (Nenhuma função é uma API do DirectShow.)


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

[Legendas e teletextos codificados](closed-captions-and-teletext.md)
</dt> </dl>

 

 



