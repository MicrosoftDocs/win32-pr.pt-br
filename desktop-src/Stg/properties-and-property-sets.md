---
title: Propriedades e conjuntos de propriedade
description: Embora os tipos de propriedades de tempo de execução oferecidos pela automação e pelos controles ActiveX da Microsoft sejam importantes, eles não atendem diretamente à necessidade de armazenar informações com objetos armazenados de forma persistente no sistema de arquivos.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Armazenamento estruturado Strctd STG, conceitos básicos, propriedades e conjuntos de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdafcbef0e92479aa628ab119b6d961abb74d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364492"
---
# <a name="properties-and-property-sets"></a>Propriedades e conjuntos de propriedade

Embora os tipos de propriedades de tempo de execução oferecidos pela automação e pelos controles ActiveX da Microsoft sejam importantes, eles não atendem diretamente à necessidade de armazenar informações com objetos armazenados de forma persistente no sistema de arquivos. Essas entidades podem incluir arquivos (estruturados, compostos e assim por diante), diretórios e catálogos de resumo. O COM fornece um formato serializado padrão para essas propriedades persistentes e um conjunto de interfaces e funções que permitem criar e manipular os conjuntos de propriedades e suas propriedades.

As propriedades persistentes são armazenadas como conjuntos e um ou mais conjuntos podem ser associados a uma entidade do sistema de arquivos. Esses conjuntos de propriedades persistentes devem ser usados para armazenar dados que são adequados para serem representados como uma coleção de valores refinados. Eles não devem ser usados como um grande banco de dados. Eles podem ser usados para armazenar informações resumidas sobre um objeto no sistema, que pode ser acessado por qualquer outro objeto que entenda como interpretar esse conjunto de propriedades.

As versões anteriores do COM especificavam muito pouco em relação às propriedades e ao seu uso, mas definimos um formato serializado que permitia que os desenvolvedores armazenassem Propriedades e conjuntos de propriedade em uma instância [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Os identificadores de propriedade e a semântica de um único conjunto de propriedades, usados para informações resumidas sobre um documento, também foram definidos. Nesse momento, era necessário criar e manipular essa estrutura diretamente como um fluxo de dados. Consulte [formato do conjunto de propriedades serializadas de armazenamento estruturado](structured-storage-serialized-property-set-format.md).

Agora, no entanto, COM define duas interfaces primárias para gerenciar conjuntos de propriedades:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Não é mais necessário lidar com o formato serializado diretamente quando essas interfaces são implementadas em um objeto que dá suporte à interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (como arquivos compostos). A gravação de propriedades por meio de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) cria dados que são exatamente em conformidade com o formato de conjunto de propriedades com, conforme exibido por meio de métodos **IStorage** . O inverso também é verdadeiro — as propriedades gravadas no formato de conjunto de propriedades COM usando **IStorage** são visíveis por meio de **IPropertySetStorage** e **IPropertyStorage** (embora você não possa esperar gravar em [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e ter as propriedades por meio de **IPropertyStorage** imediatamente disponíveis, ou vice-versa).

A interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) define métodos que criam e gerenciam conjuntos de propriedades. A interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manipula diretamente as propriedades dentro de um conjunto de propriedades. Ao chamar os métodos dessas interfaces, um desenvolvedor de aplicativos pode gerenciar quaisquer conjuntos de propriedades apropriados para uma determinada entidade do sistema de arquivos. O uso dessas interfaces fornece uma implementação de leitura e gravação ajustada para propriedades, em vez de ter uma implementação em cada aplicativo, onde pode haver gargalos de desempenho, como busca de Incessant. Você pode implementar as interfaces para aprimorar o desempenho, de modo que as propriedades possam ser lidas e gravadas mais rapidamente pelo, por exemplo, cache mais eficiente. Além disso, **IPropertyStorage** e **IPropertySetStorage** tornam possível manipular propriedades em entidades que não dão suporte a [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), embora em geral, a maioria dos aplicativos não fará isso.

Esta seção contém os seguintes tópicos:

-   [O conjunto de propriedades de informações de resumo](the-summary-information-property-set.md)
-   [Identificadores de formato do conjunto de propriedades predefinido](predefined-property-set-format-identifiers.md)
-   [Os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementações de conjunto de propriedades em COM](property-set-implementations-in-com.md)
</dt> <dt>

[Considerações sobre o conjunto de propriedades](property-set-considerations.md)
</dt> <dt>

[Gerenciando Propriedades](managing-properties.md)
</dt> <dt>

[Gerenciando conjuntos de propriedades](managing-property-sets.md)
</dt> <dt>

[Armazenando conjuntos de propriedades](storing-property-sets.md)
</dt> <dt>

[Características de desempenho](performance-characteristics.md)
</dt> </dl>

 

 




