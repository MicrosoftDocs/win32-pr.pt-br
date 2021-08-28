---
description: Gerenciador de portas de vídeo
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: Gerenciador de portas de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb7a31d21592bd94579ad608fb453e2a2ec0a264d674f807b404a43f2a0bc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903506"
---
# <a name="video-port-manager"></a>Gerenciador de portas de vídeo

O filtro do Gerenciador de portas de vídeo (VPM) permite que o filtro de processador de mixagem de vídeo 7 (VMR-7) funcione com dispositivos de captura de vídeo ou decodificadores de hardware que usam uma porta de vídeo. Uma porta de vídeo é uma conexão de hardware direta com o chip de gráficos. Ele permite que o vídeo seja transferido diretamente para o chip de gráficos sem passar pelo barramento do sistema.

> [!Note]  
> O Gerenciador de portas de vídeo não é compatível com o VMR-9, pois o VMR-9 não oferece suporte a portas de vídeo.

 



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IKsPropertySet**](ikspropertyset.md), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ VPVIDEO ou MEDIASUBTYPE \_ VPVBI, Format \_ None                                                                                                                                         |
| Interfaces de pino de entrada                     | [**IKsPin**](ikspin.md), [**IKsPropertySet**](ikspropertyset.md), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, formato \_ VideoInfo2                                                                                                                                                                                 |
| Interfaces de pino de saída                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| CLSID do filtro                             | \_VIDEOPORTMANAGER CLSID                                                                                                                                                                                              |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                                                                                                                                                                        |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentários

o gerenciador de portas de vídeo combina a funcionalidade de porta de vídeo da [sobreposição Mixer filtro](overlay-mixer-filter.md) e a funcionalidade do [alocador de superfície VBI](vbi-surface-allocator.md). O VPM aloca portas de vídeo e superfícies e sincroniza a captura de dados da porta de vídeo. Ele permite a captura baseada em porta de vídeo que é independente da renderização. Se a visualização for desejada, o VPM coordenará com o VMR-7 para exibir dados de porta de vídeo capturados. Quando uma porta de vídeo está presente no sistema, o filtro de captura requer buffers adicionais para extrair dados de VBI do fluxo de vídeo. Esses buffers são fornecidos pelo VPM. Depois que o filtro de captura extrair os dados VBI, ele o entregará em um PIN separado para filtros como o decodificador CC. A ilustração a seguir mostra o VPM e suas conexões em um grafo de filtro.

![segmento do grafo de filtro do Gerenciador de portas de vídeo](images/vpm.png)

o construtor de Graph de DVD adiciona o VPM ao grafo de filtro automaticamente quando uma porta de vídeo é detectada no sistema. Depois de adicionado ao grafo, o VPM usa um objeto do DirectDraw fornecido pelo processador de mixagem de vídeo para alocar duas ou três superfícies. Essas superfícies recebem os quadros digitalizados do filtro de captura upstream. Em resposta às notificações de eventos do modo de usuário enviadas quando os dados estão presentes na superfície, o VPM executa um blit automático para uma superfície fora da tela fornecida pelo VMR.

o fato de que o VPM usa várias superfícies para seus buffers de entrada significa que ele requer mais VRAM do que a implementação da porta de vídeo DirectShow anterior. O blit extra do VPM para o VMR-7 requer largura de banda de memória de vídeo adicional. E como a inversão automática de hardware não é mais usada, há um potencial teórico para quadros descartados, mas a evidência empírica sugere que isso não ocorre.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> <dt>

[**Interface IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



