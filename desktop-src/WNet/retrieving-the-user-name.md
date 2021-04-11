---
title: Recuperando o nome de usuário
description: Para recuperar o nome do usuário associado a um dispositivo local conectado a um recurso de rede ou com o nome de uma rede, um aplicativo pode chamar a função WNetGetUser.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162352"
---
# <a name="retrieving-the-user-name"></a><span data-ttu-id="f0c79-103">Recuperando o nome de usuário</span><span class="sxs-lookup"><span data-stu-id="f0c79-103">Retrieving the User Name</span></span>

<span data-ttu-id="f0c79-104">Para recuperar o nome do usuário associado a um dispositivo local conectado a um recurso de rede ou com o nome de uma rede, um aplicativo pode chamar a função [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="f0c79-104">To retrieve the name of the user associated either with a local device connected to a network resource or with the name of a network, an application can call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="f0c79-105">O exemplo a seguir usa o nome do dispositivo para recuperar o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="f0c79-105">The following example uses the device name to retrieve the name of the user.</span></span> <span data-ttu-id="f0c79-106">O exemplo chama um manipulador de erro definido pelo aplicativo para processar erros e a função [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.</span><span class="sxs-lookup"><span data-stu-id="f0c79-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



<span data-ttu-id="f0c79-107">Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f0c79-107">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 