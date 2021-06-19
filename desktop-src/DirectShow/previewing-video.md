---
description: Este exemplo cria um grafo de visualização de vídeo usando o método ICaptureGraphBuilder2::RenderStream no DirectShow.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Vídeo de visualização (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406889"
---
# <a name="previewing-video-directshow"></a>Vídeo de visualização (DirectShow)

Para criar um grafo de visualização de vídeo, chame o [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) da seguinte forma:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



Este exemplo pressupo o seguinte:

-   *pBuild* foi inicializado, conforme descrito em [Sobre o Construtor do Graph de Captura.](about-the-capture-graph-builder.md)
-   *o pCap* foi inicializado criando uma instância do filtro de captura e adicionando-a ao grafo de filtro, conforme descrito em [Selecionando um dispositivo de captura](selecting-a-capture-device.md).

O primeiro parâmetro para o [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica uma categoria de pin; para um grafo de visualização, use **PIN \_ CATEGORY \_ PREVIEW.** O segundo parâmetro especifica um tipo de mídia, como um GUID de tipo principal. Para vídeo, use **MEDIATYPE \_ Video**. Os dispositivos DV entregam áudio e vídeo intercalados, para os quais o tipo de mídia **é MEDIATYPE \_ intercalado.** (Para obter mais informações sobre a captura de DV, consulte [Vídeo digital no DirectShow](digital-video-in-directshow.md).)

O terceiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de captura. Os próximos dois parâmetros não são necessários neste exemplo. Eles são usados para especificar filtros adicionais que podem ser necessários para renderizar o fluxo. Definir o último parâmetro como **NULL** faz com que o Construtor do Graph de Captura selecione um renderdor padrão para o fluxo, com base no tipo de mídia. Para o vídeo, o Construtor do Graph de Captura sempre usa o filtro [Renderização de](video-renderer-filter.md) Vídeo como o renderdor padrão.

> [!Note]  
> No Windows XP e posteriores, embora o VMR (Video Mixing Renderer) seja o renderador de vídeo padrão para métodos [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) ele não é o renderador padrão para o [**método RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Em qualquer plataforma, o Construtor do Graph de Captura sempre usa o filtro antigo do Renderização de Vídeo, a menos que você especifique o contrário.

 

Embora a categoria de pino seja dada como **PIN \_ CATEGORY \_ PREVIEW**, não importa se o filtro realmente tem um pin de visualização; ele pode ter um pino de porta de vídeo ou apenas um pino de captura. Em ambos os casos, o Construtor do Graph de Captura cria automaticamente o grafo correto.

O diagrama a seguir mostra o grafo mais simples possível para visualizar o vídeo.

![grafo de visualização de vídeo](images/vidcap01.png)

Neste diagrama, o filtro de captura tem um pin de visualização, que se conecta diretamente ao renderdor de vídeo.

Se o filtro de captura tiver apenas um pino de captura, o Construtor do Graph de Captura insere um filtro [Smart Tee,](smart-tee-filter.md) que divide o fluxo em um fluxo de captura e em um fluxo de visualização. Isso é descrito em mais detalhes em [Combinando Captura de Vídeo e Visualização.](combining-video-capture-and-preview.md)

Em alguns casos, o fluxo de vídeo deve passar pelo filtro Mixer de Sobreposição. Se sim, o [**método RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) o adiciona ao grafo automaticamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Combinando captura e visualização de vídeo](combining-video-capture-and-preview.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



