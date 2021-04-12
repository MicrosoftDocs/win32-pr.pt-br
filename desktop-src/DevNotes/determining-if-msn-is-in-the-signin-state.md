---
description: O exemplo de código a seguir mostra o uso de um objeto mutex para determinar se o MSN Explorer está conectado.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Determinando se o MSN está no estado de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501027"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a><span data-ttu-id="082eb-103">Determinando se o MSN está no estado de entrada</span><span class="sxs-lookup"><span data-stu-id="082eb-103">Determining if MSN Is in the Sign-in State</span></span>

<span data-ttu-id="082eb-104">O exemplo de código a seguir mostra o uso de um objeto mutex para determinar se o MSN Explorer está conectado.</span><span class="sxs-lookup"><span data-stu-id="082eb-104">The following code example shows the usage of a mutex object to determine if MSN Explorer is signed in.</span></span> <span data-ttu-id="082eb-105">Quando terminar de usar o identificador, certifique-se de chamar a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="082eb-105">When you have finished using the handle, be sure to call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

> [!Note]  
> <span data-ttu-id="082eb-106">Este objeto mutex está disponível para uso na verificação do MSN Explorer 7. *x* status de entrada.</span><span class="sxs-lookup"><span data-stu-id="082eb-106">This mutex object is available for use in checking MSN Explorer 7.*x* sign-in status.</span></span> <span data-ttu-id="082eb-107">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="082eb-107">It may be unavailable in subsequent versions.</span></span>

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
