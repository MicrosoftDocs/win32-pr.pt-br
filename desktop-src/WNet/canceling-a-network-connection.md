---
title: Cancelando uma conexão de rede
description: Para cancelar uma conexão com um recurso de rede, um aplicativo pode chamar a função WNetCancelConnection2, conforme mostrado no exemplo a seguir.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb5c74faa1e1f8b75d0e3b604d89615c6ad1481384a661253ee204dd3ee6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566916"
---
# <a name="canceling-a-network-connection"></a>Cancelando uma conexão de rede

Para cancelar uma conexão com um recurso de rede, um aplicativo pode chamar a [**função WNetCancelConnection2,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) conforme mostrado no exemplo a seguir.

A chamada para **WNetCancelConnection2** especifica que uma conexão de rede não deve mais ser persistente. O exemplo chama um manipulador de erros definido pelo aplicativo para processar erros e a [**função TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



A [**função WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) tem suporte para compatibilidade com versões anteriores do Windows for Workgroups. Para novos aplicativos, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Para obter mais informações sobre como usar um manipulador de erros definido pelo aplicativo, consulte [Recuperando erros de rede](retrieving-network-errors.md).

 

 