---
title: Tipos de Wide-Character
description: O Microsoft RPC dá suporte ao tipo de caractere largo WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eff57cf22e4836032acb59e1585da15285f55718b6c5b91733b1955ea85072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010394"
---
# <a name="wide-character-types"></a>Tipos de Wide-Character

O Microsoft RPC dá suporte ao tipo de caractere largo [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). O tipo de caractere largo usa 2 bytes para cada caractere. A definição ANSI C-Language permite que você inicialize caracteres longos e cadeias longas como:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 