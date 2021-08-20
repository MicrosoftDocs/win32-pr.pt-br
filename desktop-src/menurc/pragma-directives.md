---
title: Diretivas pragma
description: O RC não oferece suporte às diretivas pragma com suporte pelo compilador C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35559aaadeaa6c3b769cd6ffe7a3848f44a5e165c6a25bca17f0239cafbd8f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870135"
---
# <a name="pragma-directives"></a>Diretivas pragma

O RC não oferece suporte às diretivas pragma com suporte pelo compilador C/C++. No entanto, o RC oferece suporte à seguinte diretiva pragma para alterar a página de código:

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

Não há suporte para esse pragma em um arquivo de recurso incluído (. rc). Portanto, se você tiver um arquivo pai. rc e ele incluir arquivos. rc para vários idiomas, use esse pragma antes de incluir outro arquivo. RC em vez de usá-lo no próprio arquivo. rc incluído. Isso é demonstrado no exemplo a seguir.

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

Para obter uma lista de valores para CodePageNum, consulte [identificadores de página de código](../intl/code-page-identifiers.md).

 

 