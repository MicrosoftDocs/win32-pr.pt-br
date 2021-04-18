---
description: Todos os usuários têm acesso de leitura à lista de processos no sistema e há várias funções diferentes que enumeram os processos ativos. A função que você deve usar dependerá de fatores como o suporte à plataforma desejada.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Enumeração de processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758730"
---
# <a name="process-enumeration"></a><span data-ttu-id="f78c9-104">Enumeração de processo</span><span class="sxs-lookup"><span data-stu-id="f78c9-104">Process Enumeration</span></span>

<span data-ttu-id="f78c9-105">Todos os usuários têm acesso de leitura à lista de processos no sistema e há várias funções diferentes que enumeram os processos ativos.</span><span class="sxs-lookup"><span data-stu-id="f78c9-105">All users have read access to the list of processes in the system and there are a number of different functions that enumerate the active processes.</span></span> <span data-ttu-id="f78c9-106">A função que você deve usar dependerá de fatores como o suporte à plataforma desejada.</span><span class="sxs-lookup"><span data-stu-id="f78c9-106">The function you should use will depend on factors such as desired platform support.</span></span>

<span data-ttu-id="f78c9-107">As funções a seguir são usadas para enumerar processos.</span><span class="sxs-lookup"><span data-stu-id="f78c9-107">The following functions are used to enumerate processes.</span></span>



| <span data-ttu-id="f78c9-108">Função</span><span class="sxs-lookup"><span data-stu-id="f78c9-108">Function</span></span>                                                    | <span data-ttu-id="f78c9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f78c9-109">Description</span></span>                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f78c9-110">**EnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="f78c9-110">**EnumProcesses**</span></span>](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | <span data-ttu-id="f78c9-111">Recupera o identificador de processo para cada objeto de processo no sistema.</span><span class="sxs-lookup"><span data-stu-id="f78c9-111">Retrieves the process identifier for each process object in the system.</span></span>            |
| [<span data-ttu-id="f78c9-112">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="f78c9-112">**Process32First**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | <span data-ttu-id="f78c9-113">Recupera informações sobre o primeiro processo encontrado em um instantâneo do sistema.</span><span class="sxs-lookup"><span data-stu-id="f78c9-113">Retrieves information about the first process encountered in a system snapshot.</span></span>    |
| [<span data-ttu-id="f78c9-114">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="f78c9-114">**Process32Next**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | <span data-ttu-id="f78c9-115">Recupera informações sobre o próximo processo registrado em um instantâneo do sistema.</span><span class="sxs-lookup"><span data-stu-id="f78c9-115">Retrieves information about the next process recorded in a system snapshot.</span></span>        |
| [<span data-ttu-id="f78c9-116">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="f78c9-116">**WTSEnumerateProcesses**</span></span>](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | <span data-ttu-id="f78c9-117">Recupera informações sobre os processos ativos no servidor de terminal especificado.</span><span class="sxs-lookup"><span data-stu-id="f78c9-117">Retrieves information about the active processes on the specified terminal server.</span></span> |



 

<span data-ttu-id="f78c9-118">O ToolHelp funções e [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumeram todos os processos.</span><span class="sxs-lookup"><span data-stu-id="f78c9-118">The toolhelp functions and [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerate all process.</span></span> <span data-ttu-id="f78c9-119">Para listar os processos que estão sendo executados em uma conta de usuário específica, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) e filtre no SID do usuário.</span><span class="sxs-lookup"><span data-stu-id="f78c9-119">To list the processes that are running in a specific user account, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) and filter on the user SID.</span></span> <span data-ttu-id="f78c9-120">Você pode filtrar a ID da sessão para ocultar os processos em execução em outras sessões do Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="f78c9-120">You can filter on the session ID to hide processes running in other terminal server sessions.</span></span>

<span data-ttu-id="f78c9-121">Você também pode filtrar processos por conta de usuário, independentemente da função de enumeração, chamando [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)e [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) com **TokenUser**.</span><span class="sxs-lookup"><span data-stu-id="f78c9-121">You can also filter processes by user account, regardless of the enumeration function, by calling [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) with **TokenUser**.</span></span> <span data-ttu-id="f78c9-122">No entanto, você não pode abrir um processo protegido por um descritor de segurança, a menos que tenha recebido acesso.</span><span class="sxs-lookup"><span data-stu-id="f78c9-122">However, you cannot open a process that is protected by a security descriptor unless you have been granted access.</span></span>

 

 
