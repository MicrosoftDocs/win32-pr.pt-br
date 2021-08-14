---
title: O aplicativo autônomo
description: Esse aplicativo autônomo, que consiste em uma chamada para uma única função, forma a base de nosso aplicativo distribuído.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946d76d0259fd3db971da345a10108cb3dbe11c23184b4ea9a88254e4ecb5e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923860"
---
# <a name="the-standalone-application"></a>O aplicativo autônomo

Esse aplicativo autônomo, que consiste em uma chamada para uma única função, forma a base de nosso aplicativo distribuído. A função, **HelloProc,** é definida em seu próprio arquivo de origem para que possa ser compilada e vinculada a um aplicativo autônomo ou a um aplicativo distribuído.


```C++
/* file hellop.c */
#include <stdio.h>
#include <windows.h>

void HelloProc(char * pszString)
{
    printf("%s\n", pszString);
}
 
/* file: hello.c, a stand-alone application */
#include "hellop.c"

void main(void)
{
    char * pszString = "Hello, World";
    HelloProc(pszString);
}
```



 

 




