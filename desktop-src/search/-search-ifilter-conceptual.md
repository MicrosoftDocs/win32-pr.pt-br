---
description: saiba como desenvolver manipuladores de filtro na pesquisa Windows. A pesquisa usa filtros para extrair itens para inclusão em um índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: desenvolvendo manipuladores de filtro para pesquisa de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cb8fe61ce85c86d0b8397d81303014ed1268bc0aef96b22e7b7bab335b7f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597816"
---
# <a name="developing-filter-handlers-for-windows-search"></a>desenvolvendo manipuladores de filtro para pesquisa de Windows

o Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo. você pode estender Windows pesquisa para indexar tipos de arquivo novos ou proprietários escrevendo filtros para extrair o conteúdo e os manipuladores de propriedade para extrair as propriedades dos arquivos.

Esta seção fornece a estrutura conceitual necessária para implementar um manipulador de filtro (uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

- [noções básicas sobre manipuladores de filtro na pesquisa Windows](-search-ifilter-about.md)
- [práticas recomendadas para a criação de manipuladores de filtro na pesquisa Windows](-search-3x-wds-extidx-filters.md)
- [Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)
- [Manipuladores de filtro que acompanham Windows](-search-ifilter-implementations.md)
- [implementando manipuladores de filtro na pesquisa Windows](-search-ifilter-constructing-filters.md)
- [Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)
- [Testando manipuladores de filtro](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Recursos adicionais

- o exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível em [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
