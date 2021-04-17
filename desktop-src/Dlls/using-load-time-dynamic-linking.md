---
description: Depois de criar uma DLL, você pode usar as funções que ele define em um aplicativo. Veja a seguir um aplicativo de console simples que usa a função mycolocar exportada de Myputs.dll (consulte criando uma biblioteca de Dynamic-Link simples).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Usando Load-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783313"
---
# <a name="using-load-time-dynamic-linking"></a><span data-ttu-id="5d73c-104">Usando Load-Time vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="5d73c-104">Using Load-Time Dynamic Linking</span></span>

<span data-ttu-id="5d73c-105">Depois de criar uma DLL, você pode usar as funções que ele define em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5d73c-105">After you have created a DLL, you can use the functions it defines in an application.</span></span> <span data-ttu-id="5d73c-106">Veja a seguir um aplicativo de console simples que usa a função mycolocar exportada de Myputs.dll (consulte [criando uma biblioteca de Dynamic-Link simples](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="5d73c-106">The following is a simple console application that uses the myPuts function exported from Myputs.dll (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span>

<span data-ttu-id="5d73c-107">Como este exemplo chama a função DLL explicitamente, o módulo para o aplicativo deve ser vinculado à biblioteca de importação mycoloque. lib.</span><span class="sxs-lookup"><span data-stu-id="5d73c-107">Because this example calls the DLL function explicitly, the module for the application must be linked with the import library Myputs.lib.</span></span> <span data-ttu-id="5d73c-108">Para obter mais informações sobre como criar DLLs, consulte a documentação incluída com suas ferramentas de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="5d73c-108">For more information about building DLLs, see the documentation included with your development tools.</span></span>


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="5d73c-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d73c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d73c-110">Vinculação dinâmica em tempo de carregamento</span><span class="sxs-lookup"><span data-stu-id="5d73c-110">Load-Time Dynamic Linking</span></span>](load-time-dynamic-linking.md)
</dt> </dl>

 

 



