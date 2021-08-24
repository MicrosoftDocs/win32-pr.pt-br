---
description: 'Este exemplo cria um grafo de visualização de vídeo usando o método ICaptureGraphBuilder2:: RenderStream no DirectShow.'
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Visualizando vídeo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92a6fd3f34a6b2678f41f95a80caca64e47adcc62cbeb6c37f2ed7b71f8d947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748277"
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

-   o *pBuild* foi inicializado, conforme descrito em [sobre o construtor de Graph de captura](about-the-capture-graph-builder.md).
-   o *pcap* foi inicializado, criando uma instância do filtro de captura e adicionando-a ao grafo de filtro, conforme descrito em [selecionando um dispositivo de captura](selecting-a-capture-device.md).

O primeiro parâmetro para o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica uma categoria de PIN; para um grafo de visualização, use a **\_ \_ Visualização da categoria de PIN**. O segundo parâmetro especifica um tipo de mídia, como um GUID de tipo principal. Para vídeo, use **o \_ vídeo de MediaType**. Os dispositivos DV entregam áudio e vídeo intercalados, para os quais o tipo de mídia é a **\_ dicalada de MediaType**. (Para obter mais informações sobre o DV Capture, consulte [vídeo digital no DirectShow](digital-video-in-directshow.md).)

O terceiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de captura. Os próximos dois parâmetros não são necessários neste exemplo. Eles são usados para especificar filtros adicionais que podem ser necessários para renderizar o fluxo. definir o último parâmetro como **NULL** faz com que o construtor de Graph de captura selecione um renderizador padrão para o fluxo, com base no tipo de mídia. para vídeo, o construtor de Graph de captura sempre usa o filtro de [processador de vídeo](video-renderer-filter.md) como o renderizador padrão.

> [!Note]  
> no Windows XP e posterior, embora o VMR (video mixagem renderer) seja o processador de vídeo padrão para os métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , ele não é o renderizador padrão para o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . em qualquer plataforma, o construtor de Graph de captura sempre usa o filtro de processamento de vídeo antigo, a menos que você especifique o contrário.

 

Embora a categoria de PIN seja fornecida **como \_ \_ visualização de categoria de PIN**, não importa se o filtro realmente tem um pino de visualização; ele pode ter um PIN de porta de vídeo ou apenas um PIN de captura. em ambos os casos, o construtor de Graph de captura cria automaticamente o grafo correto.

O diagrama a seguir mostra o grafo mais simples possível para visualização de vídeo.

![Grafo de visualização de vídeo](images/vidcap01.png)

Neste diagrama, o filtro de captura tem um pino de visualização, que se conecta diretamente ao processador de vídeo.

se o filtro de captura tiver apenas um pin de captura, o construtor de Graph de captura inserirá um filtro de " [t" inteligente](smart-tee-filter.md) , que dividirá o fluxo em um fluxo de captura e um fluxo de visualização. Isso é descrito mais detalhadamente na [combinação de captura de vídeo e visualização](combining-video-capture-and-preview.md).

em alguns casos, o fluxo de vídeo deve passar pela sobreposição Mixer filtro. Nesse caso, o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) o adiciona automaticamente ao grafo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Combinando captura de vídeo e visualização](combining-video-capture-and-preview.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



