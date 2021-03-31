---
title: Comentários (menus e outros recursos)
description: O RC dá suporte à sintaxe em estilo C para comentários de linha única e para bloquear comentários. Os comentários de linha única começam com duas barras (//) e são executados até o final da linha. Veja a seguir um exemplo de uma instrução de recurso seguida por um comentário de linha única.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644181"
---
# <a name="comments-menus-and-other-resources"></a>Comentários (menus e outros recursos)

O RC dá suporte à sintaxe em estilo C para comentários de linha única e para bloquear comentários. Os comentários de linha única começam com duas barras (//) e são executados até o final da linha. Veja a seguir um exemplo de uma instrução de recurso seguida por um comentário de linha única.

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

Os comentários de bloco começam com um delimitador de abertura (/ \* ) e são executados para um delimitador de fechamento ( \* /). Os comentários não podem ser aninhados. Veja a seguir um exemplo de um comentário de bloco no início de um arquivo. rc.

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




