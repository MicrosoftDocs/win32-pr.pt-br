---
description: Os diretórios na tabela de diretórios especificam o layout de uma instalação.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Usando uma propriedade de diretório em um caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa00bf3953be46484d74d3a432135763d1b06d4e7daf72bbc36f284e039613f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141464"
---
# <a name="using-a-directory-property-in-a-path"></a>Usando uma propriedade de diretório em um caminho

Os diretórios na [tabela de diretórios](directory-table.md) especificam o layout de uma instalação. quando o Windows Installer resolve esses diretórios durante a [ação CostFinalize](costfinalize-action.md), as chaves na tabela de diretório tornam-se [propriedades](properties.md) definidas como caminhos de diretório. O instalador também define um número de propriedades de [pasta do sistema](property-reference.md) padrão para caminhos de pasta do sistema.

Os valores das [Propriedades da pasta do sistema](property-reference.md) são garantidos para terminar em um separador de diretório. Os valores de todas as outras propriedades inseridas na [tabela de diretórios](directory-table.md) só são garantidos para terminar em um separador de diretório depois que o instalador tiver executado a [ação CostFinalize](costfinalize-action.md). Antes que o custo seja concluído, os valores das propriedades inseridas na tabela de diretório que não são [Propriedades da pasta do sistema](property-reference.md) podem não terminar em um separador de diretório. Portanto, se a instalação definir propriedades de diretório usando [ações personalizadas](custom-actions.md) no pacote, os valores na referência poderão não terminar com um separador de diretório.

Propriedades de diretório terminando com um separador de diretório podem, portanto, ser usadas em uma cadeia de caracteres de caminho sem incluir explicitamente o separador de diretório Por exemplo, se o valor de DirectoryProperty terminar com um separador de diretório, a cadeia de caracteres a seguir especificará corretamente o caminho para o *arquivo* no *subdiretório*

``` syntax
[DirectoryProperty]subdirectory\file
```

e a cadeia de caracteres de caminho a seguir está incorreta.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



