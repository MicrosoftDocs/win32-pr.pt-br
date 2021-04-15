---
description: Há uma variedade de funções para obter informações sobre processos.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Obtendo informações adicionais sobre o processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505873"
---
# <a name="obtaining-additional-process-information"></a><span data-ttu-id="d348e-103">Obtendo informações adicionais sobre o processo</span><span class="sxs-lookup"><span data-stu-id="d348e-103">Obtaining Additional Process Information</span></span>

<span data-ttu-id="d348e-104">Há uma variedade de funções para obter informações sobre processos.</span><span class="sxs-lookup"><span data-stu-id="d348e-104">There are a variety of functions for obtaining information about processes.</span></span> <span data-ttu-id="d348e-105">Algumas dessas funções podem ser usadas somente para o processo de chamada, pois não usam um identificador de processo como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d348e-105">Some of these functions can be used only for the calling process, because they do not take a process handle as a parameter.</span></span> <span data-ttu-id="d348e-106">Você pode usar funções que usam um identificador de processo para obter informações sobre outros processos.</span><span class="sxs-lookup"><span data-stu-id="d348e-106">You can use functions that take a process handle to obtain information about other processes.</span></span>

-   <span data-ttu-id="d348e-107">Para obter a cadeia de caracteres de linha de comando para o processo atual, use a função [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="d348e-107">To obtain the command-line string for the current process, use the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function.</span></span>
-   <span data-ttu-id="d348e-108">Para recuperar a estrutura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especificada quando o processo atual foi criado, use a função [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .</span><span class="sxs-lookup"><span data-stu-id="d348e-108">To retrieve the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specified when the current process was created, use the [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) function.</span></span>
-   <span data-ttu-id="d348e-109">Para obter as informações de versão do cabeçalho executável, use a função [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .</span><span class="sxs-lookup"><span data-stu-id="d348e-109">To obtain the version information from the executable header, use the [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) function.</span></span>
-   <span data-ttu-id="d348e-110">Para obter o caminho completo e o nome do arquivo executável que contém o código do processo, use a função [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="d348e-110">To obtain the full path and file name for the executable file containing the process code, use the [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>
-   <span data-ttu-id="d348e-111">Para obter a contagem de identificadores para objetos GUI (interface gráfica do usuário) em uso, use a função [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .</span><span class="sxs-lookup"><span data-stu-id="d348e-111">To obtain the count of handles to graphical user interface (GUI) objects in use, use the [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) function.</span></span>
-   <span data-ttu-id="d348e-112">Para determinar se um processo está sendo depurado, use a função [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="d348e-112">To determine whether a process is being debugged, use the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>
-   <span data-ttu-id="d348e-113">Para recuperar informações de estatísticas de todas as operações de e/s executadas pelo processo, use a função [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .</span><span class="sxs-lookup"><span data-stu-id="d348e-113">To retrieve accounting information for all I/O operations performed by the process, use the [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) function.</span></span>

 

 
