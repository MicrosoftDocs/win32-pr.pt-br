---
description: As propriedades são extraídas de itens usando manipuladores de propriedade registrados ou usando filtros registrados para tipos de arquivo específicos. Um manipulador de filtro (uma implementação da interface IFilter) pode interpretar o conteúdo de um tipo de arquivo de várias maneiras.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Retornando Propriedades de um manipulador de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df0bfc811176e9b0672dbcbe4ef4f04f3c3a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812397"
---
# <a name="returning-properties-from-a-filter-handler"></a>Retornando Propriedades de um manipulador de filtro

As propriedades são extraídas de itens usando manipuladores de propriedade registrados ou usando filtros registrados para tipos de arquivo específicos. Um manipulador de filtro (uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) pode interpretar o conteúdo de um tipo de arquivo de várias maneiras.

Este tópico é organizado da seguinte maneira:

- [Filtragem de propriedades](#returning-properties-from-a-filter-handler)
  - [Limitações de tamanho de propriedade](#property-size-limitations)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

## <a name="property-filtering"></a>Filtragem de propriedades

As práticas recomendadas para a filtragem de propriedades são listadas na tabela a seguir.

| Método                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Retorna a enumeração de [**\_ sinalizadores IFILTER**](/windows/win32/api/filter/ne-filter-ifilter_flags) . Se o membro de *\_ \_ \_ Propriedades OLE de sinalizadores de IFILTER* dessa enumeração for definido como um, o Windows Search usará as interfaces de interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) para enumerar e acessar propriedades de tipo de valor externo. |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Retorna informações de um documento em "partes" com tipo de bloco (texto ou valor), nome e localidade. Uma parte contém uma propriedade de documento.                                                                                                                                                                                                                                                                                                      |
| [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Obtém uma propriedade de tipo de texto de uma parte.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Obtém uma propriedade de tipo de valor de uma parte.                                                                                                                                                                                                                                                                                                                                                                                                        |

A ilustração a seguir mostra um exemplo de documento. A propriedade de tipo de valor externo `DocTitle` (obtida usando métodos das interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) e [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) ) e a propriedade de tipo de valor interno `Book` (obtida como resultado de uma implementação de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) personalizada) descrevem o documento como um todo. As propriedades do tipo de texto `Contents` e `Chapter` descrevem o conteúdo do documento. Ao processar este documento, o manipulador de filtro (uma implementação da interface **IFilter** ) identifica e extrai essas propriedades.

![diagrama mostrando os elementos de um documento típico](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitações de tamanho de propriedade

Há duas possíveis limitações no tamanho da propriedade:

- O tamanho máximo de dados que o Windows Search aceita por arquivo.
- O tamanho máximo por propriedade, conforme definido no arquivo de descrição da propriedade.

Atualmente, o Windows Search não usa o tamanho de propriedade definido ao calcular a quantidade de dados que ele aceita de um item. Em vez disso, o limite que o Windows Search usa é o produto do tamanho do arquivo e o `MaxGrowFactor` (tamanho do arquivo N \* MaxGrowFactor) lido do registro. O padrão `MaxGrowFactor` é quatro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Consequentemente, se o tipo de arquivo tende a ser pequeno no tamanho total, mas tiver Propriedades maiores, o Windows Search poderá não aceitar todos os dados de propriedade que você deseja emitir. No entanto, você pode aumentar o `MaxGrowFactor` para atender às suas necessidades.

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
- Para obter uma visão geral das propriedades e dos manipuladores de propriedade e uma lista de propriedades do sistema que você pode usar para os formatos de arquivo, consulte [desenvolvendo manipuladores de propriedade para o Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[Sobre manipuladores de filtro no Windows Search](-search-ifilter-about.md)

[Práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)

[Manipuladores de filtro que acompanham o Windows](-search-ifilter-implementations.md)

[Implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md)

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)
