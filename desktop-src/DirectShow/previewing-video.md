---
description: Visualizando vídeo
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Visualizando vídeo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550652"
---
# <a name="previewing-video-directshow"></a>Visualizando vídeo (DirectShow)

Para criar um grafo de visualização de vídeo, chame o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) da seguinte maneira:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



Este exemplo pressupõe o seguinte:

-   o *pBuild* foi inicializado, conforme descrito em [sobre o construtor do grafo de captura](about-the-capture-graph-builder.md).
-   o *pcap* foi inicializado, criando uma instância do filtro de captura e adicionando-a ao grafo de filtro, conforme descrito em [selecionando um dispositivo de captura](selecting-a-capture-device.md).

O primeiro parâmetro para o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica uma categoria de PIN; para um grafo de visualização, use a **\_ \_ Visualização da categoria de PIN**. O segundo parâmetro especifica um tipo de mídia, como um GUID de tipo principal. Para vídeo, use **o \_ vídeo de MediaType**. Os dispositivos DV entregam áudio e vídeo intercalados, para os quais o tipo de mídia é a **\_ dicalada de MediaType**. (Para obter mais informações sobre o DV Capture, consulte [vídeo digital no DirectShow](digital-video-in-directshow.md).)

O terceiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de captura. Os próximos dois parâmetros não são necessários neste exemplo. Eles são usados para especificar filtros adicionais que podem ser necessários para renderizar o fluxo. Definir o último parâmetro como **NULL** faz com que o construtor do grafo de captura selecione um renderizador padrão para o fluxo, com base no tipo de mídia. Para vídeo, o construtor de gráficos de captura sempre usa o filtro de [processador de vídeo](video-renderer-filter.md) como o renderizador padrão.

> [!Note]  
> No Windows XP e posterior, embora o VMR (Video mixagem Renderer) seja o processador de vídeo padrão para os métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , ele não é o renderizador padrão para o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . Em qualquer plataforma, o construtor de grafo de captura sempre usa o filtro de processamento de vídeo antigo, a menos que você especifique o contrário.

 

Embora a categoria de PIN seja fornecida **como \_ \_ visualização de categoria de PIN**, não importa se o filtro realmente tem um pino de visualização; ele pode ter um PIN de porta de vídeo ou apenas um PIN de captura. Em ambos os casos, o construtor do grafo de captura cria automaticamente o grafo correto.

O diagrama a seguir mostra o grafo mais simples possível para visualização de vídeo.

![Grafo de visualização de vídeo](images/vidcap01.png)

Neste diagrama, o filtro de captura tem um pino de visualização, que se conecta diretamente ao processador de vídeo.

Se o filtro de captura tiver apenas um PIN de captura, o construtor do grafo de captura inserirá um filtro de " [t" inteligente](smart-tee-filter.md) , que dividirá o fluxo em um fluxo de captura e um fluxo de visualização. Isso é descrito mais detalhadamente na [combinação de captura de vídeo e visualização](combining-video-capture-and-preview.md).

Em alguns casos, o fluxo de vídeo deve passar pelo filtro de mixer de sobreposição. Nesse caso, o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) o adiciona automaticamente ao grafo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Combinando captura de vídeo e visualização](combining-video-capture-and-preview.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



