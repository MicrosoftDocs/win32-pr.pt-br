---
description: Saiba como desenvolver manipuladores de filtro em Windows Search. A pesquisa usa filtros para extrair itens para inclusão em um índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desenvolvendo manipuladores de filtro para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988855"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Desenvolvendo manipuladores de filtro para Windows Search

O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo. Você pode estender Windows Search para indexar tipos de arquivo novos ou proprietários escrevendo filtros para extrair o conteúdo e manipuladores de propriedades para extrair as propriedades dos arquivos.

Esta seção fornece a estrutura conceitual necessária para implementar um manipulador de filtro (uma implementação da interface [**IFilter).**](/windows/win32/api/filter/nn-filter-ifilter)

- [Noções básicas sobre manipuladores de filtro Windows Search](-search-ifilter-about.md)
- [Práticas recomendadas para criar manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)
- [Retornando propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)
- [Manipuladores de filtros que são enviar com o Windows](-search-ifilter-implementations.md)
- [Implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md)
- [Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)
- [Testando manipuladores de filtro](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample,](-search-sample-ifiltersample.md) disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para uma visão geral do processo de indexação, consulte [O processo de indexação](-search-indexing-process-overview.md).
- Para uma visão geral dos tipos de arquivo, consulte [Tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e Registro de Aplicativo.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))
