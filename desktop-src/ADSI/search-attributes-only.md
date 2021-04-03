---
title: Pesquisar somente atributos
description: Às vezes, você executa uma pesquisa para determinar que tipo de dados está disponível para um objeto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Somente ADSI de atributos de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915887"
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
-   [Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




