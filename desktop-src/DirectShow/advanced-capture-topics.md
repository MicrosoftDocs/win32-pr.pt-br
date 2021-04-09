---
description: Tópicos de captura avançada
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Tópicos de captura avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087788"
---
# <a name="advanced-capture-topics"></a>Tópicos de captura avançada

Esta seção descreve alguns aspectos avançados da captura de vídeo no DirectShow. A maioria dos problemas descritos nesta seção é manipulada automaticamente pela interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . No entanto, as informações aqui podem ser úteis se você precisar solucionar problemas de um aplicativo de captura de vídeo. Você também deve ler esta seção se seu aplicativo criar um grafo de captura personalizado de algum tipo e você achar que o ICaptureGraphBuilder2 não atende às suas necessidades. Por fim, esta seção contém algumas informações sobre como usar o filtro de processador de mixagem de vídeo (VMR) em um aplicativo de captura de vídeo.

É possível criar um grafo de captura de vídeo totalmente usando métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . Você também pode combinar as duas interfaces, usando ICaptureGraphBuilder2 para algumas tarefas e IGraphBuilder para outras.

Esta seção contém os seguintes tópicos:

-   [Manipulando eventos redesenhados na captura de vídeo](handling-repaint-events-in-video-capture.md)
-   [Trabalhando com categorias de PIN](working-with-pin-categories.md)
-   [Usando o filtro de "t inteligente"](using-the-smart-tee-filter.md)
-   [Usando o mixer de sobreposição na captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
-   [Pins de porta de vídeo](video-port-pins.md)
-   [Tipo de formato VideoInfo2](videoinfo2-format-type.md)
-   [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md)
-   [Filtros de driver de classe WDM](wdm-class-driver-filters.md)
-   [Usando a captura do WDDM no DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



