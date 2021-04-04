---
title: Cancelando uma conexão de rede
description: Para cancelar uma conexão a um recurso de rede, um aplicativo pode chamar a função WNetCancelConnection2, conforme mostrado no exemplo a seguir.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823910"
---
# <a name="canceling-a-network-connection"></a>Cancelando uma conexão de rede

Para cancelar uma conexão a um recurso de rede, um aplicativo pode chamar a função [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , conforme mostrado no exemplo a seguir.

A chamada para **WNetCancelConnection2** especifica que uma conexão de rede não deve mais ser persistente. O exemplo chama um manipulador de erro definido pelo aplicativo para processar erros e a função [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.


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



A função [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) tem suporte para compatibilidade com versões anteriores do Windows para Workgroups. Para novos aplicativos, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).

 

 