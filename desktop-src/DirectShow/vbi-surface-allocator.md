---
description: Alocador de Superfície de VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Alocador de Superfície de VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c586c3ef135722ac259813d918dc4054617b8ae6bfb987083f0a2ceaa986067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071980"
---
# <a name="vbi-surface-allocator"></a>Alocador de Superfície de VBI

O Alocador de Superfície de VBI controla a alocação de buffers de VBI em grafos de tv análogos com cenários de captura de porta de vídeo de hardware. Com dispositivos como o decodificador Bt829, o buffer de quadro pode conter vários buffers de captura de VBI acessados por meio de um mecanismo proprietário baseado em hardware conhecido genericamente como uma Porta de Vídeo. O filtro Alocador de Superfície da VBI conecta-se downstream do filtro de captura e não tem nenhum pino de saída. O filtro funciona em estreita proximidade com a Mixer [sobreposição](overlay-mixer-filter.md) (via DirectDraw) para executar operações coordenadas na porta de vídeo de hardware, utilizando a mesma memória de buffer de quadro SVGA limitada.



| Rótulo | Valor |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Tipos de mídia de pino de entrada                    | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ VPVBI                                               |
| Interfaces de pino de entrada                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Tipos de mídia de pino de saída                   | MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL. (Nada está conectado ao pino de saída.) |
| Interfaces de pino de saída                    | Não aplicável.                                                                     |
| Filtrar CLSID                             | CLSID \_ VBISurfaces                                                                  |
| CLSID da página de propriedades                      | Nenhuma página de propriedades.                                                                   |
| Executável                               | vbisurf.ax                                                                          |
| [Mérito](merit.md)                       | NORMAL DE SEMPRE \_                                                                       |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



