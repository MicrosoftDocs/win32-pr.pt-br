---
title: Adicionando uma conexão de rede
description: Para fazer uma conexão com um recurso de rede descrito por uma estrutura de NETRESOURCE, um aplicativo pode chamar o WNetAddConnection2, a WNetAddConnection3 ou a função WNetUseConnection.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105791631"
---
# <a name="adding-a-network-connection"></a><span data-ttu-id="48fab-103">Adicionando uma conexão de rede</span><span class="sxs-lookup"><span data-stu-id="48fab-103">Adding a Network Connection</span></span>

<span data-ttu-id="48fab-104">Para fazer uma conexão com um recurso de rede descrito por uma estrutura de [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , um aplicativo pode chamar o [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), a [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)ou a função [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) .</span><span class="sxs-lookup"><span data-stu-id="48fab-104">To make a connection to a network resource described by a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure, an application can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a), or the [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) function.</span></span> <span data-ttu-id="48fab-105">O exemplo a seguir demonstra o uso da função **WNetAddConnection2** .</span><span class="sxs-lookup"><span data-stu-id="48fab-105">The following example demonstrates use of the **WNetAddConnection2** function.</span></span>

<span data-ttu-id="48fab-106">O exemplo de código chama a função **WNetAddConnection2** , especificando que o sistema deve atualizar o perfil do usuário com as informações, criando uma conexão persistente ou "lembrada".</span><span class="sxs-lookup"><span data-stu-id="48fab-106">The code sample calls the **WNetAddConnection2** function, specifying that the system should update the user's profile with the information, creating a "remembered" or persistent connection.</span></span> <span data-ttu-id="48fab-107">O exemplo chama um manipulador de erro definido pelo aplicativo para processar erros e a função [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.</span><span class="sxs-lookup"><span data-stu-id="48fab-107">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


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



<span data-ttu-id="48fab-108">A função [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) tem suporte para compatibilidade com versões anteriores do Windows para Workgroups.</span><span class="sxs-lookup"><span data-stu-id="48fab-108">The [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="48fab-109">Novos aplicativos devem chamar a função [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou a função [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) .</span><span class="sxs-lookup"><span data-stu-id="48fab-109">New applications should call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function.</span></span>

<span data-ttu-id="48fab-110">Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="48fab-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 