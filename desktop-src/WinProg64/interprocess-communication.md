---
title: Comunicação entre processos
description: As técnicas a seguir podem ser usadas para comunicação entre aplicativos de 32 bits e de 64 bits.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- Programação entre processos de comunicação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366400"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a><span data-ttu-id="c0313-104">Comunicação entre processos entre aplicativos de 32 bits e de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c0313-104">Interprocess Communication Between 32-bit and 64-bit Applications</span></span>

<span data-ttu-id="c0313-105">As técnicas a seguir podem ser usadas para comunicação entre aplicativos de 32 bits e de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="c0313-105">The following techniques can be used for communication between 32-bit and 64-bit applications:</span></span>

-   <span data-ttu-id="c0313-106">as versões de 64 bits do Windows usam identificadores de 32 bits para interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="c0313-106">64-bit versions of Windows use 32-bit handles for interoperability.</span></span> <span data-ttu-id="c0313-107">Ao compartilhar um identificador entre os aplicativos de 32 bits e 64 bits, somente os menores bits 32 são significativos, portanto, é seguro truncar o identificador (ao passá-lo de 64 para 32 bits) ou estender a alça (ao passá-lo de 32 para 64 bits).</span><span class="sxs-lookup"><span data-stu-id="c0313-107">When sharing a handle between 32-bit and 64-bit applications, only the lower 32 bits are significant, so it is safe to truncate the handle (when passing it from 64-bit to 32-bit) or sign-extend the handle (when passing it from 32-bit to 64-bit).</span></span> <span data-ttu-id="c0313-108">Identificadores que podem ser compartilhados incluem identificadores para objetos de usuário como Windows (**HWND**), identificadores para objetos GDI, como canetas e pincéis (**HBRUSH** e **HPEN**), e identificadores para objetos nomeados, como mutexes, semáforos e identificadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0313-108">Handles that can be shared include handles to user objects such as windows (**HWND**), handles to GDI objects such as pens and brushes (**HBRUSH** and **HPEN**), and handles to named objects such as mutexes, semaphores, and file handles.</span></span>
-   <span data-ttu-id="c0313-109">RPC (chamadas de procedimento remoto) podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="c0313-109">Remote procedure calls (RPC) can be used.</span></span>
-   <span data-ttu-id="c0313-110">O COM LocalServers pode ser usado se as DLLs de proxy/stub de 32 bits e de 64 bits estiverem registradas para todas as interfaces usadas.</span><span class="sxs-lookup"><span data-stu-id="c0313-110">COM LocalServers can be used if both 32-bit and 64-bit proxy/stub DLLs are registered for all interfaces used.</span></span>
-   <span data-ttu-id="c0313-111">A memória compartilhada poderá ser usada se tipos dependentes de ponteiro forem convertidos corretamente (ou evitados).</span><span class="sxs-lookup"><span data-stu-id="c0313-111">Shared memory can be used if pointer-dependent types are converted properly (or avoided).</span></span>
-   <span data-ttu-id="c0313-112">As funções [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) podem iniciar processos de 32 bits e 64 bits a partir de processos de 32 bits ou de 64 bits com certas limitações.</span><span class="sxs-lookup"><span data-stu-id="c0313-112">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) and [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) functions can launch 32-bit and 64-bit processes from either 32-bit or 64-bit processes with certain limitations.</span></span>

<span data-ttu-id="c0313-113">Um arquivo executável de 64 bits localizado em% windir% \\ system32 não pode ser iniciado a partir de um processo de 32 bits, pois o redirecionador do sistema de arquivos redireciona o caminho.</span><span class="sxs-lookup"><span data-stu-id="c0313-113">A 64-bit executable file located under %windir%\\System32 cannot be launched from a 32-bit process, because the file system redirector redirects the path.</span></span> <span data-ttu-id="c0313-114">Não desabilite o redirecionamento para fazer isso; \\em vez disso, use% windir% SysNative.</span><span class="sxs-lookup"><span data-stu-id="c0313-114">Do not disable redirection to accomplish this; use %windir%\\Sysnative instead.</span></span> <span data-ttu-id="c0313-115">Para obter mais informações, consulte [redirecionador de sistema de arquivos](file-system-redirector.md).</span><span class="sxs-lookup"><span data-stu-id="c0313-115">For more information, see [File System Redirector](file-system-redirector.md).</span></span>

 

 