---
description: A noção de bloqueio em um ambiente do Windows tem sido historicamente muito importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operações de bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763520"
---
# <a name="blocking-operations"></a><span data-ttu-id="7782d-103">Operações de bloqueio</span><span class="sxs-lookup"><span data-stu-id="7782d-103">Blocking Operations</span></span>

<span data-ttu-id="7782d-104">A noção de bloqueio em um ambiente do Windows tem sido historicamente muito importante.</span><span class="sxs-lookup"><span data-stu-id="7782d-104">The notion of blocking in a Windows environment has historically been a very important one.</span></span> <span data-ttu-id="7782d-105">Nos ambientes do Windows Sockets 1,1, as chamadas de bloqueio foram desencorajadas, pois elas tendiamm para desabilitar a interação contínua com o sistema.</span><span class="sxs-lookup"><span data-stu-id="7782d-105">In Windows Sockets 1.1 environments, blocking calls were discouraged since they tended to disable ongoing interaction with the system.</span></span> <span data-ttu-id="7782d-106">Além disso, eles empregam uma técnica pseudoblocking, que, por vários motivos, nem sempre funciona conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="7782d-106">Additionally, they employ a pseudoblocking technique which, for a variety of reasons, does not always work as intended.</span></span> <span data-ttu-id="7782d-107">No entanto, em ambientes Windows programados de forma preventiva, as chamadas de bloqueio fazem muito mais sentido, podem ser implementadas por serviços do sistema operacional nativo e, na verdade, são um mecanismo preferencial.</span><span class="sxs-lookup"><span data-stu-id="7782d-107">However, in preemptively scheduled Windows environments, blocking calls make much more sense, can be implemented by native operating system services, and are in fact a generally preferred mechanism.</span></span> <span data-ttu-id="7782d-108">A API do Winsock 2 não dá mais suporte a psuedoblocking, mas como os shims de compatibilidade do Windows Sockets 1,1 devem continuar emulando esse comportamento, os provedores de serviços devem dar suporte a isso, conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="7782d-108">The Winsock 2 API no longer supports psuedoblocking, but because the Windows Sockets 1.1 compatibility shims must continue to emulate this behavior, service providers must support this as described in the following.</span></span>

 

 



