---
title: Pesquisar somente atributos
description: Às vezes, você executa uma pesquisa para determinar que tipo de dados está disponível para um objeto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Somente ADSI de atributos de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b1775c759975a508f5382ef2a30f290ac4a96b3b92120d4face6b1d0556426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443926"
---
# <a name="search-attributes-only"></a>Pesquisar somente atributos

Às vezes, você executa uma pesquisa para determinar que tipo de dados está disponível para um objeto. Nesse caso, você está interessado apenas nos atributos, e não nos valores do objeto. Para fazer isso, defina a opção "Pesquisar somente atributos". A especificação dessa opção retorna os nomes de atributo sem seus valores. No entanto, o conjunto de resultados inclui apenas os atributos que têm valores atribuídos. Por exemplo, considere um objeto com os seguintes atributos:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Quando a opção Pesquisar somente atributos é definida, o conjunto de resultados inclui:

``` syntax
First Name
Last Name
Phone Number
```

Para obter mais informações sobre como usar a opção somente atributos de pesquisa com uma interface de pesquisa específica, consulte:

-   [Retornando somente nomes de atributo com IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




