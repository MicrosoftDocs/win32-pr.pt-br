---
description: Filtro de decodificador de WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de decodificador de WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908474"
---
# <a name="wst-decoder-filter"></a>Filtro de decodificador de WST

Este componente foi removido do Windows Vista e de sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Windows XP e Windows Server 2003.

> [!Note]  
> A partir do Windows Vista, o DirectShow não fornece um filtro para decodificar o teletexto padrão do mundo (WST).

 

O decodificador de WST é um filtro de modo kernel que aceita dados de teletextos padrão do mundo decodificados do [codec de WST](wst-codec-filter.md) e entrega os bitmaps para o pino 2 no [mixer de sobreposição](overlay-mixer-filter.md) usando fontes fornecidas pela Microsoft. Somente os idiomas da Europa Ocidental têm suporte no momento; no momento, não há fontes Unicode fornecidas.

Esse filtro pode ser adicionado ao grafo automaticamente chamando [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), usando o pino de saída do codec de WST.



| Label | Valor |
|------------------------------------------|---------------------------------------------------------------|
| Filtrar interfaces                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ VBI, \_ TELEtext MEDIASUBTYPE                        |
| Interfaces de pino de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Tipos de mídia do pino de saída                   | Vídeo de MEDIATYPE \_                                              |
| Interfaces de pino de saída                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| CLSID do filtro                             | \_WSTDECODER CLSID                                             |
| CLSID de página de propriedades                      | \_WSTDECODERPROPERTYPAGE CLSID                                 |
| Executável                               | Wstdecod.DLL                                                  |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                 |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Exibindo teletexto do mundo Standard](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



