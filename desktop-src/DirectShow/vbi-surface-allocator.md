---
description: Alocador de superfície VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Alocador de superfície VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909004"
---
# <a name="vbi-surface-allocator"></a>Alocador de superfície VBI

O alocador de superfície VBI controla a alocação de buffers VBI em gráficos de televisão analógicas com cenários de captura de porta de vídeo de hardware. Com dispositivos como o decodificador Bt829, o buffer de quadro pode conter vários buffers de captura VBI que são acessados por meio de um mecanismo de hardware proprietário conhecido genericamente como uma porta de vídeo. O filtro de alocador de superfície VBI conecta downstream do filtro de captura e não tem nenhum pino de saída. O filtro funciona junto com o [mixer de sobreposição](overlay-mixer-filter.md) (via DirectDraw) para executar operações coordenadas na porta de vídeo de hardware, utilizando a mesma memória de buffer de quadro SVGA limitada.



| Label | Valor |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ VPVBI                                               |
| Interfaces de pino de entrada                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Tipos de mídia do pino de saída                   | MEDIATYPE \_ nulo, MEDIASUBTYPE \_ nulo. (Nada está sempre conectado ao pino de saída.) |
| Interfaces de pino de saída                    | Não aplicável.                                                                     |
| CLSID do filtro                             | \_VBISURFACES CLSID                                                                  |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                   |
| Executável                               | vbisurf.ax                                                                          |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                                       |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



