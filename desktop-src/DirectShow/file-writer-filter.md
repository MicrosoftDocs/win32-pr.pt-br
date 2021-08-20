---
description: Filtro do File Writer
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro do File Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f21009d8135cb42ec93c4f5727398dcdf3094ed4e5da666c325c959dbffc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651366"
---
# <a name="file-writer-filter"></a>Filtro do File Writer

O filtro File Writer pode ser usado para gravar arquivos no disco, independentemente do formato. O filtro simplesmente grava no disco o que receber em seu pin de entrada, portanto, ele deve ser conectado upstream a um multiplexador que possa formatar o arquivo corretamente. Você pode criar um novo arquivo de saída com o File Writer ou especificar um arquivo existente; se o arquivo já existir, ele será completamente substituído com os novos dados.

O filtro de autor de arquivo usa os carimbos de data/hora do fluxo de entrada como deslocamentos de arquivo e fornece acesso aleatório ao arquivo. Ele dá **suporte a IStream** para permitir a leitura e a escrita do header do arquivo depois que o grafo é interrompido. Para melhorar o desempenho, ele também dá suporte a gravações sobrecodadas sem buffer e lida com a negociação de buffer correspondente.

> [!Note]  
> Para gravar arquivos ASF, use o filtro [Wm ASF Writer.](wm-asf-writer-filter.md)

 



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream** |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ Stream, MEDIASUBTYPE \_ NULL                                                                                                                                                              |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) **IStream**                                                                                |
| Tipos de mídia de pino de saída                   | Não se aplica                                                                                                                                                                                     |
| Interfaces de pino de saída                    | Não se aplica                                                                                                                                                                                     |
| Filtrar CLSID                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| CLSID da página de propriedades                      | Nenhuma página de propriedades                                                                                                                                                                                   |
| Executável                               | qcap.dll                                                                                                                                                                                           |
| [Mérito](merit.md)                       | NÃO USE O NÃO \_ \_ USO \_ DE LIMITED                                                                                                                                                                                |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



