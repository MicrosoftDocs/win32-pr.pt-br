---
title: Recuperando o nome da conexão
description: Para recuperar o nome do recurso de rede associado a um dispositivo local, um aplicativo pode chamar a função WNetGetConnection, conforme mostrado no exemplo a seguir.
ms.assetid: 7c02cf9a-cca3-47d8-8a4b-f2245f1db92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac84aec3c6aafb8a5113ea29251247a1de35aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084706"
---
# <a name="retrieving-the-connection-name"></a><span data-ttu-id="d61bc-103">Recuperando o nome da conexão</span><span class="sxs-lookup"><span data-stu-id="d61bc-103">Retrieving the Connection Name</span></span>

<span data-ttu-id="d61bc-104">Para recuperar o nome do recurso de rede associado a um dispositivo local, um aplicativo pode chamar a função [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d61bc-104">To retrieve the name of the network resource associated with a local device, an application can call the [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) function, as shown in the following sample.</span></span>

<span data-ttu-id="d61bc-105">O exemplo a seguir chama um manipulador de erro definido pelo aplicativo para processar erros e a função [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.</span><span class="sxs-lookup"><span data-stu-id="d61bc-105">The following sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
TCHAR szDeviceName[80]; 
DWORD dwResult, cchBuff = sizeof(szDeviceName); 
 
// Call the WNetGetConnection function.
//
dwResult = WNetGetConnection(_T("z:"), 
    szDeviceName, 
    &cchBuff); 
 
switch (dwResult) 
{ 
    //
    // Print the connection name or process errors.
    //
    case NO_ERROR: 
        printf("Connection name: %s\n", szDeviceName); 
        break; 
    //
    // The device is not a redirected device.
    //
    case ERROR_NOT_CONNECTED: 
        printf("Device z: not connected.\n"); 
        break;
    //
    // The device is not currently connected, but it is a persistent connection.
    //
    case ERROR_CONNECTION_UNAVAIL: 
        printf("Connection unavailable.\n"); 
        break;
    //
    // Handle the error.
    //
    default: 
        printf("WNetGetConnection failed.\n"); 
}
```



<span data-ttu-id="d61bc-106">Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d61bc-106">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 