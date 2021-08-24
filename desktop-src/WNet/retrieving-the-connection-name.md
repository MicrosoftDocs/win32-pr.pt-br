---
title: Recuperando o nome da conexão
description: Para recuperar o nome do recurso de rede associado a um dispositivo local, um aplicativo pode chamar a função WNetGetConnection, conforme mostrado no exemplo a seguir.
ms.assetid: 7c02cf9a-cca3-47d8-8a4b-f2245f1db92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264a7352fb10139df538d5803fc94966b276fa334f2e4ef5f2c0799e1c32c4cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566823"
---
# <a name="retrieving-the-connection-name"></a>Recuperando o nome da conexão

Para recuperar o nome do recurso de rede associado a um dispositivo local, um aplicativo pode chamar a [**função WNetGetConnection,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) conforme mostrado no exemplo a seguir.

O exemplo a seguir chama um manipulador de erros definido pelo aplicativo para processar erros e a [**função TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.


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



Para obter mais informações sobre como usar um manipulador de erros definido pelo aplicativo, consulte [Recuperando erros de rede](retrieving-network-errors.md).

 

 