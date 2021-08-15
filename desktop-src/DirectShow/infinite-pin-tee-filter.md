---
description: Filtro de Pin Tee Infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro de Pin Tee Infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28edb67da9d6aae01786cece43b45dfcd33d571b82bdbab21ecf82a2473ff0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818781"
---
# <a name="infinite-pin-tee-filter"></a>Filtro de Pin Tee Infinito

Esse filtro fornece exemplos entregues ao pin de entrada para um número variável de pinos de saída. Quando uma instância do filtro é criada, ela tem um pino de saída. Sempre que um pino de saída é conectado, o filtro cria outro pino de saída. Todos os pinos de saída compartilham o mesmo tipo de mídia que o pino de entrada.

Uma versão desse filtro também é fornecida como um exemplo do SDK. Consulte [Exemplo de filtro infTee](inftee-filter-sample.md).



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de mídia de pino de entrada                    | Qualquer tipo de mídia                                                                                                                                     |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia de pino de saída                   | Qualquer tipo de mídia. O tipo de saída sempre corresponde ao tipo de entrada, para todos os pinos de saída                                                                 |
| Interfaces de pino de saída                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ InfTee                                                                                                                                      |
| CLSID da página de propriedades                      | Nenhuma página de propriedades                                                                                                                                   |
| Executável                               | qcap.dll                                                                                                                                           |
| [Mérito](merit.md)                       | NÃO USE O NÃO \_ \_ USO \_ DE LIMITED                                                                                                                                |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



