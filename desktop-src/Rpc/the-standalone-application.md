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
# <a name="the-standalone-application"></a><span data-ttu-id="349ff-103">O aplicativo autônomo</span><span class="sxs-lookup"><span data-stu-id="349ff-103">The Standalone Application</span></span>

<span data-ttu-id="349ff-104">Esse aplicativo autônomo, que consiste em uma chamada para uma única função, constitui a base de nosso aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="349ff-104">This standalone application, which consists of a call to a single function, forms the basis of our distributed application.</span></span> <span data-ttu-id="349ff-105">A função, **HelloProc**, é definida em seu próprio arquivo de origem para que possa ser compilada e vinculada a um aplicativo autônomo ou a um aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="349ff-105">The function, **HelloProc**, is defined in its own source file so that it can be compiled and linked with either a standalone application or a distributed application.</span></span>


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



 

 




