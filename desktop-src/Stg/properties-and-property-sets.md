---
title: Propriedades e conjuntos de propriedades
description: Embora os tipos de propriedades em tempo de run time que a Automação e os Controles do Microsoft ActiveX oferecem sejam importantes, eles não abordam diretamente a necessidade de armazenar informações com objetos armazenados persistentemente no sistema de arquivos.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Estruturadas Armazenamento Stg Strctd , conceitos básicos, propriedades e conjuntos de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df2ef4b3e4d91cc908d82b58a0ec0156a60de23208cfd8dde2718fa62eaab60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662256"
---
# <a name="properties-and-property-sets"></a>Propriedades e conjuntos de propriedades

Embora os tipos de propriedades em tempo de run time que a Automação e os Controles do Microsoft ActiveX oferecem sejam importantes, eles não abordam diretamente a necessidade de armazenar informações com objetos armazenados persistentemente no sistema de arquivos. Essas entidades podem incluir arquivos (estruturados, compostos e assim por diante), diretórios e catálogos de resumo. O COM fornece um formato serializado padrão para essas propriedades persistentes e um conjunto de interfaces e funções que permitem criar e manipular os conjuntos de propriedades e suas propriedades.

As propriedades persistentes são armazenadas como conjuntos e um ou mais conjuntos podem ser associados a uma entidade do sistema de arquivos. Esses conjuntos de propriedades persistentes devem ser usados para armazenar dados adequados para serem representados como uma coleção de valores finos. Elas não se destinam a serem usadas como uma grande base de dados. Eles podem ser usados para armazenar informações resumidas sobre um objeto no sistema, que pode ser acessado por qualquer outro objeto que entenda como interpretar esse conjunto de propriedades.

As versões anteriores do COM especificam muito pouco em relação às propriedades e seu uso, mas definiram um formato serializado que permitia aos desenvolvedores armazenar propriedades e conjuntos de propriedades em uma [**instância do IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Os identificadores de propriedade e a semântica de um único conjunto de propriedades, usados para informações resumidas sobre um documento, também foram definidos. Nesse momento, era necessário criar e manipular essa estrutura diretamente como um fluxo de dados. Consulte [Formato Armazenamento conjunto de propriedades serializado estruturado.](structured-storage-serialized-property-set-format.md)

Agora, no entanto, o COM define duas interfaces primárias para gerenciar conjuntos de propriedades:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Não é mais necessário lidar com o formato serializado diretamente quando essas interfaces são implementadas em um objeto que dá suporte à interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (como arquivos compostos). A escrita de propriedades por meio [**de IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) cria dados que estão exatamente em conformidade com o formato do conjunto de propriedades COM, conforme exibido por meio dos métodos **IStorage.** O inverso também é verdadeiro – as propriedades escritas no formato de conjunto de propriedades COM usando **IStorage** são visíveis por meio de **IPropertySetStorage** e **IPropertyStorage** (embora você não possa esperar gravar em [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e ter as propriedades por meio de **IPropertyStorage** imediatamente disponíveis ou vice-versa).

A interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) define métodos que criam e gerenciam conjuntos de propriedades. A interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manipula diretamente as propriedades dentro de um conjunto de propriedades. Ao chamar os métodos dessas interfaces, um desenvolvedor de aplicativos pode gerenciar quaisquer conjuntos de propriedades apropriados para uma determinada entidade do sistema de arquivos. O uso dessas interfaces fornece uma implementação de leitura e escrita ajustada para propriedades, em vez de ter uma implementação em cada aplicativo, em que pode haver gargalos de desempenho, como busca direta. Você pode implementar as interfaces para melhorar o desempenho, para que as propriedades possam ser lidas e escritas mais rapidamente por, por exemplo, cache mais eficiente. Além disso, **IPropertyStorage** e **IPropertySetStorage** possibilitam manipular propriedades em entidades que não são suportadas pelo [**IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage)embora, em geral, a maioria dos aplicativos não faça isso.

Esta seção contém os seguintes tópicos:

-   [O conjunto de propriedades de informações de resumo](the-summary-information-property-set.md)
-   [Identificadores de formato de conjunto de propriedades predefinidos](predefined-property-set-format-identifiers.md)
-   [Os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implementações de conjunto de propriedades em COM](property-set-implementations-in-com.md)
</dt> <dt>

[Considerações sobre o conjunto de propriedades](property-set-considerations.md)
</dt> <dt>

[Gerenciando propriedades](managing-properties.md)
</dt> <dt>

[Gerenciando conjuntos de propriedades](managing-property-sets.md)
</dt> <dt>

[Armazenar conjuntos de propriedades](storing-property-sets.md)
</dt> <dt>

[Características de desempenho](performance-characteristics.md)
</dt> </dl>

 

 




