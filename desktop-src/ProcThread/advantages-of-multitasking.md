---
description: Para o usuário, a vantagem da multitarefa é a capacidade de ter vários aplicativos abertos e trabalhando ao mesmo tempo. Por exemplo, um usuário pode editar um arquivo com um aplicativo enquanto outro aplicativo está recalculando uma planilha.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Vantagens da multitarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778530"
---
# <a name="advantages-of-multitasking"></a><span data-ttu-id="21957-104">Vantagens da multitarefa</span><span class="sxs-lookup"><span data-stu-id="21957-104">Advantages of Multitasking</span></span>

<span data-ttu-id="21957-105">Para o usuário, a vantagem da multitarefa é a capacidade de ter vários aplicativos abertos e trabalhando ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="21957-105">To the user, the advantage of multitasking is the ability to have several applications open and working at the same time.</span></span> <span data-ttu-id="21957-106">Por exemplo, um usuário pode editar um arquivo com um aplicativo enquanto outro aplicativo está recalculando uma planilha.</span><span class="sxs-lookup"><span data-stu-id="21957-106">For example, a user can edit a file with one application while another application is recalculating a spreadsheet.</span></span>

<span data-ttu-id="21957-107">Para o desenvolvedor de aplicativos, a vantagem da multitarefa é a capacidade de criar aplicativos que usam mais de um processo e criar processos que usam mais de um thread de execução.</span><span class="sxs-lookup"><span data-stu-id="21957-107">To the application developer, the advantage of multitasking is the ability to create applications that use more than one process and to create processes that use more than one thread of execution.</span></span> <span data-ttu-id="21957-108">Por exemplo, um processo pode ter um thread de interface do usuário que gerencia as interações com o usuário (entrada de teclado e mouse) e threads de trabalho que executam outras tarefas enquanto o thread da interface do usuário aguarda a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="21957-108">For example, a process can have a user interface thread that manages interactions with the user (keyboard and mouse input), and worker threads that perform other tasks while the user interface thread waits for user input.</span></span> <span data-ttu-id="21957-109">Se você conceder ao thread da interface do usuário uma prioridade mais alta, o aplicativo será mais responsivo ao usuário, enquanto os threads de trabalho usam o processador com eficiência durante os horários em que não há nenhuma entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="21957-109">If you give the user interface thread a higher priority, the application will be more responsive to the user, while the worker threads use the processor efficiently during the times when there is no user input.</span></span>

 

 



