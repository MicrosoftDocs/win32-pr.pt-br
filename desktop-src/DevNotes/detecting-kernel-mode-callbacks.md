---
description: Se um thread estiver aguardando a conclusão de um retorno de chamada de modo kernel, o lado do modo de usuário do thread será atrasado em uma chamada para a função ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Detectando retornos de chamada Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920475"
---
# <a name="detecting-kernel-mode-callbacks"></a><span data-ttu-id="47cc2-103">Detectando retornos de chamada Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="47cc2-103">Detecting Kernel-Mode Callbacks</span></span>

<span data-ttu-id="47cc2-104">A maior parte do código para o sistema operacional Windows é executada no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="47cc2-104">Most of the code for the Windows operating system runs in kernel mode.</span></span> <span data-ttu-id="47cc2-105">O modo de processador muda de modo de usuário para modo kernel sempre que um thread de aplicativo chama uma função da API do Windows que, por sua vez, chama uma função interna do sistema que deve ser executada no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="47cc2-105">The processor mode switches from user mode to kernel mode whenever an application thread calls a function from the Windows API that in turn calls an internal system function that must execute in kernel mode.</span></span> <span data-ttu-id="47cc2-106">O modo de processador retorna ao modo de usuário antes de o controle retornar à função para que os dados do sistema sejam protegidos.</span><span class="sxs-lookup"><span data-stu-id="47cc2-106">The processor mode returns to user mode before control returns to the function so that the system data is protected.</span></span>

<span data-ttu-id="47cc2-107">Se um thread estiver aguardando a conclusão de um retorno de chamada de modo kernel, o lado do modo de usuário do thread será atrasado em uma chamada para a função **ZwCallbackReturn** .</span><span class="sxs-lookup"><span data-stu-id="47cc2-107">If a thread is waiting for a kernel-mode callback to complete, the user-mode side of the thread will delay at a call to the **ZwCallbackReturn** function.</span></span>

 

 



