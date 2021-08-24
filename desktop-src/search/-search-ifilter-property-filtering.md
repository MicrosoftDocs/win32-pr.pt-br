---
description: As propriedades são extraídas de itens usando manipuladores de propriedades registrados ou usando filtros registrados para tipos de arquivo específicos. Um manipulador de filtro (uma implementação da interface IFilter) pode interpretar o conteúdo de um tipo de arquivo de várias maneiras.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Retornando propriedades de um manipulador de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1842710af65e22f5a730891ea6e7f32053b92212f8c3ad4c5f0f68f23578d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594846"
---
# <a name="returning-properties-from-a-filter-handler"></a>Retornando propriedades de um manipulador de filtro

As propriedades são extraídas de itens usando manipuladores de propriedades registrados ou usando filtros registrados para tipos de arquivo específicos. Um manipulador de filtro (uma implementação da interface [**IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) pode interpretar o conteúdo de um tipo de arquivo de várias maneiras.

Este tópico é organizado da seguinte forma:

- [Filtragem de propriedade](#returning-properties-from-a-filter-handler)
  - [Limitações de tamanho da propriedade](#property-size-limitations)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

## <a name="property-filtering"></a>Filtragem de propriedade

As práticas recomendadas para filtragem de propriedade são listadas na tabela a seguir.

| Método                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Retorna a [**enumeração \_ FLAGS de IFILTER.**](/windows/win32/api/filter/ne-filter-ifilter_flags) Se o membro *\_ IFILTER FLAGS \_ OLE \_ PROPERTIES* dessa enumeração estiver definido como um, o Windows Search usará as interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) para enumerar e acessar propriedades externas do tipo de valor. |
| [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Retorna informações de um documento em "partes" com tipo de parte (texto ou valor), nome e localidade. Uma parte contém uma propriedade de documento.                                                                                                                                                                                                                                                                                                      |
| [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Obtém uma propriedade de tipo de texto de uma parte.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Obtém uma propriedade de tipo de valor de uma parte.                                                                                                                                                                                                                                                                                                                                                                                                        |

A ilustração a seguir mostra um documento de exemplo. A propriedade de tipo de valor externo (obtida usando métodos das `DocTitle` interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage)](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e a propriedade de tipo de valor interno (obtida como resultado de uma implementação `Book` de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) personalizada) descrevem o documento como um todo. As propriedades de tipo de `Contents` texto e descrevem o conteúdo do `Chapter` documento. Ao processar este documento, o manipulador de filtros (uma implementação da interface **IFilter)** identifica e extrai essas propriedades.

![diagrama mostrando os elementos de um documento típico](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitações de tamanho da propriedade

Há duas limitações potenciais para o tamanho da propriedade:

- O tamanho máximo dos dados que Windows Search aceita por arquivo.
- O tamanho máximo por propriedade, conforme definido no arquivo de descrição da propriedade.

Atualmente, Windows Search não usa o tamanho da propriedade definido ao calcular a quantidade de dados que ele aceita de um item. Em vez disso, o limite Windows Search usa é o produto do tamanho do arquivo e o (tamanho do arquivo `MaxGrowFactor` N \* MaxGrowFactor) lido do Registro. O padrão `MaxGrowFactor` é quatro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Consequentemente, se o tipo de arquivo tende a ser pequeno em tamanho total, mas tem propriedades maiores, Windows Search pode não aceitar todos os dados de propriedade que você deseja emitir. No entanto, você pode aumentar o `MaxGrowFactor` para atender às suas necessidades.

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample,](-search-sample-ifiltersample.md) disponível [no GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
- Para uma visão geral do processo de indexação, consulte [O processo de indexação](-search-indexing-process-overview.md).
- Para uma visão geral dos tipos de arquivo, consulte [Tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e Registro de Aplicativo.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))
- Para uma visão geral das propriedades e manipuladores de propriedades e uma lista de propriedades do sistema que você pode usar para seus formatos de arquivo, consulte Desenvolvendo manipuladores de propriedades para [Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[Sobre manipuladores de filtro na Windows Search](-search-ifilter-about.md)

[Práticas recomendadas para criar manipuladores de filtro na Windows Search](-search-3x-wds-extidx-filters.md)

[Manipuladores de filtros que são Windows](-search-ifilter-implementations.md)

[Implementando manipuladores de filtro na Windows Search](-search-ifilter-constructing-filters.md)

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)
