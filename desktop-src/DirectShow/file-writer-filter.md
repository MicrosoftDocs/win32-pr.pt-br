---
description: Filtro de gravador de arquivo
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro de gravador de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163848"
---
# <a name="file-writer-filter"></a>Filtro de gravador de arquivo

O filtro de gravador de arquivo pode ser usado para gravar arquivos no disco, independentemente do formato. O filtro simplesmente grava em disco o que receber em seu pino de entrada, portanto, ele deve ser conectado ao upstream para um multiplexador que pode formatar o arquivo corretamente. Você pode criar um novo arquivo de saída com o gravador de arquivo ou especificar um arquivo existente; Se o arquivo já existir, ele será completamente substituído pelos novos dados.

O filtro de gravador de arquivo usa os carimbos de data/hora do fluxo de entrada como deslocamentos de arquivo e fornece acesso aleatório ao arquivo. Ele dá suporte a **IStream** para permitir a leitura e gravação do cabeçalho do arquivo depois que o grafo é interrompido. Para melhorar o desempenho, ele também dá suporte a gravações sobrepostas sem buffer e manipula a negociação de buffer correspondente.

> [!Note]  
> Para gravar arquivos ASF, use o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) .

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream** |
| Tipos de mídia de pino de entrada                    | \_Fluxo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                                                                              |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**                                                                                |
| Tipos de mídia do pino de saída                   | Não aplicável                                                                                                                                                                                     |
| Interfaces de pino de saída                    | Não aplicável                                                                                                                                                                                     |
| CLSID do filtro                             | FileWriter do CLSID \_                                                                                                                                                                                  |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                                                                                   |
| Executável                               | qcap.dll                                                                                                                                                                                           |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



