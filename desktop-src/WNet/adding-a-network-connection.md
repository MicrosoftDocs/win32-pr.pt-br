---
title: Adicionando uma conexão de rede
description: Para fazer uma conexão com um recurso de rede descrito por uma estrutura NETRESOURCE, um aplicativo pode chamar a função WNetAddConnection2, WNetAddConnection3 ou WNetUseConnection.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8298216ab277c5f0ec4a0db8c4d6d1b6c592a8b643e6c30de96731ae2a32632b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053384"
---
# <a name="adding-a-network-connection"></a>Adicionando uma conexão de rede

Para fazer uma conexão com um recurso de rede descrito por uma estrutura [**NETRESOURCE,**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) um aplicativo pode chamar a [**função WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)ou [**WNetUseConnection.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) O exemplo a seguir demonstra o uso da **função WNetAddConnection2.**

O exemplo de código chama a **função WNetAddConnection2,** especificando que o sistema deve atualizar o perfil do usuário com as informações, criando uma conexão "lembrada" ou persistente. O exemplo chama um manipulador de erros definido pelo aplicativo para processar erros e a [**função TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



A [**função WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) tem suporte para compatibilidade com versões anteriores do Windows for Workgroups. Novos aplicativos devem chamar a [**função WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou a [**função WNetAddConnection3.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)

Para obter mais informações sobre como usar um manipulador de erros definido pelo aplicativo, consulte [Recuperando erros de rede](retrieving-network-errors.md).

 

 