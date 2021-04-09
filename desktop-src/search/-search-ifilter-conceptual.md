---
description: O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desenvolvendo manipuladores de filtro para o Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010391"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Desenvolvendo manipuladores de filtro para o Windows Search

O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo. Você pode estender o Windows Search para indexar tipos de arquivo novos ou proprietários escrevendo filtros para extrair o conteúdo e os manipuladores de propriedade para extrair as propriedades dos arquivos.

Esta seção fornece a estrutura conceitual necessária para implementar um manipulador de filtro (uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

- [Noções básicas sobre manipuladores de filtro no Windows Search](-search-ifilter-about.md)
- [Práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)
- [Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)
- [Manipuladores de filtro que acompanham o Windows](-search-ifilter-implementations.md)
- [Implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md)
- [Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)
- [Testando manipuladores de filtro](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
