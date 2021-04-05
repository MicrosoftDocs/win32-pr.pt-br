---
description: As funções a seguir são usadas com o desligamento do sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funções de desligamento do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921837"
---
# <a name="system-shutdown-functions"></a><span data-ttu-id="9bf04-103">Funções de desligamento do sistema</span><span class="sxs-lookup"><span data-stu-id="9bf04-103">System Shutdown Functions</span></span>

<span data-ttu-id="9bf04-104">As funções a seguir são usadas com o desligamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="9bf04-104">The following functions are used with system shutdown.</span></span>



| <span data-ttu-id="9bf04-105">Função</span><span class="sxs-lookup"><span data-stu-id="9bf04-105">Function</span></span>                                                         | <span data-ttu-id="9bf04-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bf04-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bf04-107">**AbortSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="9bf04-107">**AbortSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | <span data-ttu-id="9bf04-108">Interrompe um desligamento do sistema que foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="9bf04-108">Stops a system shutdown that has been initiated.</span></span>                                                                                    |
| [<span data-ttu-id="9bf04-109">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="9bf04-109">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | <span data-ttu-id="9bf04-110">Faz logoff do usuário interativo.</span><span class="sxs-lookup"><span data-stu-id="9bf04-110">Logs off the interactive user.</span></span>                                                                                                      |
| [<span data-ttu-id="9bf04-111">**ExitWindowsEx**</span><span class="sxs-lookup"><span data-stu-id="9bf04-111">**ExitWindowsEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | <span data-ttu-id="9bf04-112">Faz logoff do usuário interativo, desliga o sistema ou desliga e reinicia o sistema.</span><span class="sxs-lookup"><span data-stu-id="9bf04-112">Logs off the interactive user, shuts down the system, or shuts down and restarts the system.</span></span>                                        |
| [<span data-ttu-id="9bf04-113">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="9bf04-113">**InitiateShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | <span data-ttu-id="9bf04-114">Inicia um desligamento e reinicialização do computador especificado e reinicia todos os aplicativos que foram registrados para reinicialização.</span><span class="sxs-lookup"><span data-stu-id="9bf04-114">Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.</span></span>    |
| [<span data-ttu-id="9bf04-115">**InitiateSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="9bf04-115">**InitiateSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | <span data-ttu-id="9bf04-116">Inicia um desligamento e uma reinicialização opcional do computador especificado.</span><span class="sxs-lookup"><span data-stu-id="9bf04-116">Initiates a shutdown and optional restart of the specified computer.</span></span>                                                                |
| [<span data-ttu-id="9bf04-117">**InitiateSystemShutdownEx**</span><span class="sxs-lookup"><span data-stu-id="9bf04-117">**InitiateSystemShutdownEx**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | <span data-ttu-id="9bf04-118">Inicia um desligamento e uma reinicialização opcional do computador especificado e, opcionalmente, registra o motivo do desligamento.</span><span class="sxs-lookup"><span data-stu-id="9bf04-118">Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.</span></span>            |
| [<span data-ttu-id="9bf04-119">**LockWorkStation**</span><span class="sxs-lookup"><span data-stu-id="9bf04-119">**LockWorkStation**</span></span>](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | <span data-ttu-id="9bf04-120">Bloqueia a exibição da estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9bf04-120">Locks the workstation's display.</span></span>                                                                                                    |
| [<span data-ttu-id="9bf04-121">**ShutdownBlockReasonCreate**</span><span class="sxs-lookup"><span data-stu-id="9bf04-121">**ShutdownBlockReasonCreate**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | <span data-ttu-id="9bf04-122">Indica que o sistema não pode ser desligado e define uma cadeia de caracteres de motivo a ser exibida para o usuário se o desligamento do sistema for iniciado.</span><span class="sxs-lookup"><span data-stu-id="9bf04-122">Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.</span></span> |
| [<span data-ttu-id="9bf04-123">**ShutdownBlockReasonDestroy**</span><span class="sxs-lookup"><span data-stu-id="9bf04-123">**ShutdownBlockReasonDestroy**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | <span data-ttu-id="9bf04-124">Indica que o sistema pode ser desligado e libera a cadeia de caracteres de motivo.</span><span class="sxs-lookup"><span data-stu-id="9bf04-124">Indicates that the system can be shut down and frees the reason string.</span></span>                                                             |
| [<span data-ttu-id="9bf04-125">**ShutdownBlockReasonQuery**</span><span class="sxs-lookup"><span data-stu-id="9bf04-125">**ShutdownBlockReasonQuery**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | <span data-ttu-id="9bf04-126">Recupera a cadeia de caracteres de motivo definida pela função [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="9bf04-126">Retrieves the reason string set by the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span>                     |



 

 

 



