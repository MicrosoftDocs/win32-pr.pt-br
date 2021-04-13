---
description: O WMI usa caminhos de objeto nas propriedades de referência de classes de associação para identificar objetos relacionados, bem como usar caminhos de objeto em parâmetros de entrada ou saída para vários métodos.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisitos de caminho do objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370675"
---
# <a name="wmi-object-path-requirements"></a>Requisitos de caminho do objeto WMI

O WMI usa caminhos de objeto nas propriedades de referência de classes de associação para identificar objetos relacionados, bem como usar caminhos de objeto em parâmetros de entrada ou saída para vários métodos. Como os caminhos de objeto são tratados como cadeias de caracteres para fins de pesquisa e comparação, o valor de um caminho de objeto quando usado como uma propriedade de referência é sempre a própria cadeia de caracteres e não o objeto desreferenciado. Comparações de cadeias de caracteres que lidam com caminhos de objeto sempre diferenciam maiúsculas de minúsculas.

Um caminho de objeto pode usar a seguinte sintaxe:

-   Cadeias de caracteres contidas entre aspas simples.
-   Redirecionar barras como separadores.
-   Barras invertidas como separadores.
-   Constantes hexadecimais para inteiros.
-   Constantes booleanas para classes com chaves que usam valores Boolianos.
-   Notação de URL para representar caracteres não imprimíveis, como %20 para um espaço em branco.

Além disso, uma cadeia de caracteres de caminho de objeto deve obedecer às seguintes restrições:

-   Um servidor local assumido com um caminho de namespace parcial. Assim, especificar a raiz e o namespace padrão implica a raiz e o namespace padrão no servidor local.
-   Não há espaço em branco dentro de um elemento ou entre elementos.
-   Aspas inseridas em caminhos de objeto são permitidas, mas devem delimitar as aspas com caracteres de escape, como em um aplicativo C ou C++.
-   Somente valores decimais são reconhecidos como partes numéricas de chaves.

 

 



