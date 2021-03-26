---
title: Informações do processo
description: O sistema mantém uma lista de processos em execução. Você pode recuperar os identificadores para esses processos chamando a função EnumProcesses. Essa função preenche uma matriz de valores DWORD com os identificadores de todos os processos no sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294199"
---
# <a name="process-information"></a><span data-ttu-id="eb0b8-105">Informações do processo</span><span class="sxs-lookup"><span data-stu-id="eb0b8-105">Process Information</span></span>

<span data-ttu-id="eb0b8-106">O sistema mantém uma lista de processos em execução.</span><span class="sxs-lookup"><span data-stu-id="eb0b8-106">The system maintains a list of running processes.</span></span> <span data-ttu-id="eb0b8-107">Você pode recuperar os identificadores para esses processos chamando a função [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="eb0b8-107">You can retrieve the identifiers for these processes by calling the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="eb0b8-108">Essa função preenche uma matriz de valores **DWORD** com os identificadores de todos os processos no sistema.</span><span class="sxs-lookup"><span data-stu-id="eb0b8-108">This function fills an array of **DWORD** values with the identifiers of all processes in the system.</span></span>

<span data-ttu-id="eb0b8-109">Muitas funções no PSAPI exigem um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="eb0b8-109">Many functions in PSAPI require a process handle.</span></span> <span data-ttu-id="eb0b8-110">Para obter um identificador de processo para um processo em execução, passe seu identificador de processo (obtido de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) para a função [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) .</span><span class="sxs-lookup"><span data-stu-id="eb0b8-110">To obtain a process handle for a running process, pass its process identifier (obtained from [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) to the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="eb0b8-111">Lembre-se de chamar a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) quando terminar com o identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="eb0b8-111">Remember to call the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function when you are finished with the process handle.</span></span>

 

 