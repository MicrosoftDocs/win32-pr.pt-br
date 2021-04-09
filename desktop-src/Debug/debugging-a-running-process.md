---
description: Para depurar um processo que já está em execução, o depurador deve usar DebugActiveProcess com o identificador de processo. Para recuperar uma lista de identificadores de processo, use a função EnumProcesses ou Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Depurando um processo em execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088850"
---
# <a name="debugging-a-running-process"></a><span data-ttu-id="446b2-104">Depurando um processo em execução</span><span class="sxs-lookup"><span data-stu-id="446b2-104">Debugging a Running Process</span></span>

<span data-ttu-id="446b2-105">Para depurar um processo que já está em execução, o depurador deve usar [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) com o identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="446b2-105">To debug a process that is already running, the debugger should use [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) with the process identifier.</span></span> <span data-ttu-id="446b2-106">Para recuperar uma lista de identificadores de processo, use a função [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) ou [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="446b2-106">To retrieve a list of process identifiers, use either the [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) or [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function.</span></span>

<span data-ttu-id="446b2-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) anexa o depurador ao processo ativo.</span><span class="sxs-lookup"><span data-stu-id="446b2-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attaches the debugger to the active process.</span></span> <span data-ttu-id="446b2-108">Nesse caso, somente o processo ativo pode ser depurado; seus processos filho não podem.</span><span class="sxs-lookup"><span data-stu-id="446b2-108">In this case, only the active process can be debugged; its child processes cannot.</span></span> <span data-ttu-id="446b2-109">O depurador deve ter acesso apropriado ao processo em execução para usar o **DebugActiveProcess**.</span><span class="sxs-lookup"><span data-stu-id="446b2-109">The debugger must have appropriate access to the executing process to use **DebugActiveProcess**.</span></span> <span data-ttu-id="446b2-110">Para obter mais informações sobre direitos de acesso, consulte [controle de acesso](../secauthz/access-control.md).</span><span class="sxs-lookup"><span data-stu-id="446b2-110">For more information about access rights, see [Access Control](../secauthz/access-control.md).</span></span>

<span data-ttu-id="446b2-111">Depois que o depurador tiver sido criado ou anexado ao processo que pretende depurar, o sistema notificará o depurador de todos os eventos de depuração que ocorrem no processo e, se especificado, em qualquer processo filho.</span><span class="sxs-lookup"><span data-stu-id="446b2-111">After the debugger has either created or attached itself to the process it intends to debug, the system notifies the debugger of all debugging events that occur in the process, and, if specified, in any child processes.</span></span> <span data-ttu-id="446b2-112">Para obter mais informações sobre eventos de depuração, consulte [Debugging Events](debugging-events.md).</span><span class="sxs-lookup"><span data-stu-id="446b2-112">For more information about debugging events, see [Debugging Events](debugging-events.md).</span></span>

<span data-ttu-id="446b2-113">Para desanexar do processo que está sendo depurado, o depurador deve usar a função [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .</span><span class="sxs-lookup"><span data-stu-id="446b2-113">To detach from the process being debugged, the debugger should use the [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) function.</span></span>

 

 
