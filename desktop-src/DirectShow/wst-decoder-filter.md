---
description: Filtro de decodificador WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de decodificador WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61da0540c683e8c4646074715b0518717b4e1958beea5b8ca2ae41fb4629790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290766"
---
# <a name="wst-decoder-filter"></a>Filtro de decodificador WST

Esse componente foi removido do Windows Vista e sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Windows XP e Windows Server 2003.

> [!Note]  
> Começando no Windows Vista, DirectShow fornece um filtro para decodificar o WST (World Standard Teletext).

 

O Decodificador WST é um filtro de modo kernel que aceita dados Decodificados do World Standard Teletext do [](overlay-mixer-filter.md) [Codec do WST](wst-codec-filter.md) e fornece os bitmaps para Fixar 2 no Mixer sobreposição usando fontes fornecidas pela Microsoft. Somente idiomas da Europa Ocidental têm suporte no momento; Nenhuma fonte Unicode é fornecida no momento.

Esse filtro pode ser adicionado ao grafo automaticamente chamando [**ICaptureGraphBuilder2::RenderStream,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)usando o pino de saída do Codec do WST.



| Rótulo | Valor |
|------------------------------------------|---------------------------------------------------------------|
| Interfaces de filtro                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT                        |
| Interfaces de pino de entrada                     | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Tipos de mídia de pino de saída                   | Vídeo \_ MEDIATYPE                                              |
| Interfaces de pino de saída                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Filtrar CLSID                             | CLSID \_ WSTDecoder                                             |
| CLSID da página de propriedades                      | CLSID \_ WstDecoderPropertyPage                                 |
| Executável                               | Wstdecod.DLL                                                  |
| [Mérito](merit.md)                       | NORMAL DE SEMPRE \_                                                 |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Exibindo o World Standard Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



