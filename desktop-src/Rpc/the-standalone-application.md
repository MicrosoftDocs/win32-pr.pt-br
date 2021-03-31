---
title: O aplicativo autônomo
description: Esse aplicativo autônomo, que consiste em uma chamada para uma única função, constitui a base de nosso aplicativo distribuído.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf1b11df2372a1db5c74659d1800b62e53b7309
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005514"
---
# <a name="the-standalone-application"></a>O aplicativo autônomo

Esse aplicativo autônomo, que consiste em uma chamada para uma única função, constitui a base de nosso aplicativo distribuído. A função, **HelloProc**, é definida em seu próprio arquivo de origem para que possa ser compilada e vinculada a um aplicativo autônomo ou a um aplicativo distribuído.


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



 

 




