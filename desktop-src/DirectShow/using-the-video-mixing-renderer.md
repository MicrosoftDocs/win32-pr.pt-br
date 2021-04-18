---
description: Usando o processador de mixagem de vídeo
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Usando o processador de mixagem de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778780"
---
# <a name="using-the-video-mixing-renderer"></a>Usando o processador de mixagem de vídeo

Em termos de desempenho e amplitude de recursos, o filtro de processador de mixagem de vídeo (VMR) representa a próxima geração na renderização de vídeo na plataforma Windows. O VMR substitui o [mixer de sobreposição](overlay-mixer-filter.md) e o [processador de vídeo](video-renderer-filter.md), além de adicionar muitos novos recursos de mixagem.

Há duas versões do VMR:

-   O VMR-7, que usa o DirectDraw 7 para renderização.
-   O VMR-9, que usa o Direct3D 9.

O VMR-7 está disponível no Windows XP e posterior, mas não está disponível para redistribuição. O VMR-9 está disponível para redistribuição em todas as plataformas com suporte no DirectX 9. Os dois filtros do VMR são muito semelhantes em sua implementação e nas interfaces que eles expõem.

O VMR-9 tem seu próprio CLSID e seu próprio conjunto de interfaces, estruturas e tipos de enumeração que nem sempre são idênticos aos tipos de dados correspondentes para o VMR-7, devido às diferenças subjacentes entre o DirectDraw 7 e o Direct3D 9. Todas as interfaces do VMR-9 terminam com "9", por exemplo, **IVMRStreamConfig9**, e as estruturas e os tipos de enumeração têm "VMR9" em seu nome para diferenciá-las dos tipos de dados usados com o VMR-7.

Para garantir a compatibilidade com versões anteriores, o VMR-9 não é o renderizador padrão em nenhum sistema. Para usar o VMR-9, você deve adicioná-lo explicitamente ao grafo de filtro usando o método [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) e configurá-lo antes de conectá-lo a qualquer filtro upstream.

Este artigo inclui as seções a seguir. Exceto quando indicado, as informações nessas seções se aplicam aos filtros VMR-7 e VMR-9.

-   [Sobre o processamento de mixagem de vídeo](about-the-video-mixing-render.md)
-   [Modos de operação do VMR](vmr-modes-of-operation.md)
-   [Criando um grafo de filtro do VMR-9](building-a-vmr-9-filter-graph.md)
-   [Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
-   [Definindo preferências de desentrelaçamento](setting-deinterlace-preferences.md)
-   [Usando o VMR para desenvolvedores de filtro do DirectShow](using-the-vmr-for-directshow-filter-developers.md)
-   [Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md)
</dt> <dt>

[Filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



