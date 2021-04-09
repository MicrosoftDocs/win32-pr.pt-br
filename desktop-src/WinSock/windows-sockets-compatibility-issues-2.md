---
description: O Windows Sockets 2 continua a dar suporte a todas as semânticas e chamadas de função do Windows Sockets 1,1, exceto aquelas que lidam com o pseudo-bloqueio.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Problemas de compatibilidade do Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164866"
---
# <a name="windows-sockets-compatibility-issues"></a><span data-ttu-id="e518e-103">Problemas de compatibilidade do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="e518e-103">Windows Sockets Compatibility Issues</span></span>

<span data-ttu-id="e518e-104">O Windows Sockets 2 continua a dar suporte a todas as semânticas e chamadas de função do Windows Sockets 1,1, exceto aquelas que lidam com o pseudo-bloqueio.</span><span class="sxs-lookup"><span data-stu-id="e518e-104">Windows Sockets 2 continues to support all of the Windows Sockets 1.1 semantics and function calls except for those dealing with pseudo-blocking.</span></span> <span data-ttu-id="e518e-105">Como o Windows Sockets 2 é executado somente em ambientes de 32 bits e programados de vez em diante, não é necessário implementar o pseudo-bloqueio encontrado no Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="e518e-105">Since Windows Sockets 2 runs only in 32-bit, preemptively scheduled environments, there is no need to implement the pseudo-blocking found in Windows Sockets 1.1.</span></span> <span data-ttu-id="e518e-106">Isso significa que o código de erro WSAEINPROGRESS nunca será indicado e que as seguintes funções do Windows Sockets 1,1 não estão disponíveis para aplicativos do Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="e518e-106">This means that the WSAEINPROGRESS error code will never be indicated and that the following Windows Sockets 1.1 functions are not available to Windows Sockets 2 applications:</span></span>

-   <span data-ttu-id="e518e-107">WSACancelBlockingCall</span><span class="sxs-lookup"><span data-stu-id="e518e-107">WSACancelBlockingCall</span></span>
-   <span data-ttu-id="e518e-108">WSAIsBlocking</span><span class="sxs-lookup"><span data-stu-id="e518e-108">WSAIsBlocking</span></span>
-   <span data-ttu-id="e518e-109">WSASetBlockingHook</span><span class="sxs-lookup"><span data-stu-id="e518e-109">WSASetBlockingHook</span></span>
-   <span data-ttu-id="e518e-110">WSAUnhookBlockingHook</span><span class="sxs-lookup"><span data-stu-id="e518e-110">WSAUnhookBlockingHook</span></span>

<span data-ttu-id="e518e-111">Os programas do Windows Sockets 1,1 que são gravados para utilizar o pseudo-bloqueio continuarão a operar corretamente, pois eles se vinculam a Winsock.dll ou Wsock32.dll.</span><span class="sxs-lookup"><span data-stu-id="e518e-111">Windows Sockets 1.1 programs that are written to utilize pseudo-blocking will continue to operate correctly since they link to either Winsock.dll or Wsock32.dll.</span></span> <span data-ttu-id="e518e-112">Ambos continuam a dar suporte ao conjunto completo de funções do Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="e518e-112">Both continue to support the complete set of Windows Sockets 1.1 functions.</span></span> <span data-ttu-id="e518e-113">Para que os programas se tornem aplicativos do Windows Sockets 2, deve ocorrer alguma modificação de código.</span><span class="sxs-lookup"><span data-stu-id="e518e-113">In order for programs to become Windows Sockets 2 applications, some code modification must occur.</span></span> <span data-ttu-id="e518e-114">Na maioria dos casos, o uso criterioso de threads pode ser substituído para acomodar o processamento que estava sendo realizado com uma função de gancho de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="e518e-114">In most cases, the judicious use of threads can be substituted to accommodate processing that was being accomplished with a blocking hook function.</span></span>

 

 



