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
# <a name="canceling-a-network-connection"></a><span data-ttu-id="caba6-103">Cancelando uma conexão de rede</span><span class="sxs-lookup"><span data-stu-id="caba6-103">Canceling a Network Connection</span></span>

<span data-ttu-id="caba6-104">Para cancelar uma conexão a um recurso de rede, um aplicativo pode chamar a função [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="caba6-104">To cancel a connection to a network resource, an application can call the [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) function, as shown in the following example.</span></span>

<span data-ttu-id="caba6-105">A chamada para **WNetCancelConnection2** especifica que uma conexão de rede não deve mais ser persistente.</span><span class="sxs-lookup"><span data-stu-id="caba6-105">The call to **WNetCancelConnection2** specifies that a network connection should no longer be persistent.</span></span> <span data-ttu-id="caba6-106">O exemplo chama um manipulador de erro definido pelo aplicativo para processar erros e a função [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.</span><span class="sxs-lookup"><span data-stu-id="caba6-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


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



<span data-ttu-id="caba6-107">A função [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) tem suporte para compatibilidade com versões anteriores do Windows para Workgroups.</span><span class="sxs-lookup"><span data-stu-id="caba6-107">The [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="caba6-108">Para novos aplicativos, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span><span class="sxs-lookup"><span data-stu-id="caba6-108">For new applications, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span></span>

<span data-ttu-id="caba6-109">Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="caba6-109">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 