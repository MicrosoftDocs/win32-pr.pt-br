---
description: A inversão de prioridade ocorre quando dois ou mais threads com prioridades diferentes estão em contenção a ser agendada.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversão de prioridade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296740"
---
# <a name="priority-inversion"></a><span data-ttu-id="614e3-103">Inversão de prioridade</span><span class="sxs-lookup"><span data-stu-id="614e3-103">Priority Inversion</span></span>

<span data-ttu-id="614e3-104">A inversão de prioridade ocorre quando dois ou mais threads com prioridades diferentes estão em contenção a ser agendada.</span><span class="sxs-lookup"><span data-stu-id="614e3-104">Priority inversion occurs when two or more threads with different priorities are in contention to be scheduled.</span></span> <span data-ttu-id="614e3-105">Considere um caso simples com três threads: thread 1, thread 2 e thread 3.</span><span class="sxs-lookup"><span data-stu-id="614e3-105">Consider a simple case with three threads: thread 1, thread 2, and thread 3.</span></span> <span data-ttu-id="614e3-106">O thread 1 é de alta prioridade e fica pronto para ser agendado.</span><span class="sxs-lookup"><span data-stu-id="614e3-106">Thread 1 is high priority and becomes ready to be scheduled.</span></span> <span data-ttu-id="614e3-107">O thread 2, um thread de baixa prioridade, está executando o código em uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="614e3-107">Thread 2, a low-priority thread, is executing code in a critical section.</span></span> <span data-ttu-id="614e3-108">O thread 1, o thread de alta prioridade, começa a aguardar um recurso compartilhado do thread 2.</span><span class="sxs-lookup"><span data-stu-id="614e3-108">Thread 1, the high-priority thread, begins waiting for a shared resource from thread 2.</span></span> <span data-ttu-id="614e3-109">O thread 3 tem prioridade média.</span><span class="sxs-lookup"><span data-stu-id="614e3-109">Thread 3 has medium priority.</span></span> <span data-ttu-id="614e3-110">O thread 3 recebe todo o tempo do processador, pois o thread de alta prioridade (thread 1) está aguardando recursos compartilhados do thread de baixa prioridade (thread 2).</span><span class="sxs-lookup"><span data-stu-id="614e3-110">Thread 3 receives all the processor time, because the high-priority thread (thread 1) is waiting for shared resources from the low-priority thread (thread 2).</span></span> <span data-ttu-id="614e3-111">O thread 2 não deixará a seção crítica, pois não tem a prioridade mais alta e não será agendado.</span><span class="sxs-lookup"><span data-stu-id="614e3-111">Thread 2 will not leave the critical section, because it does not have the highest priority and will not be scheduled.</span></span>

<span data-ttu-id="614e3-112">O Agendador resolve esse problema, aumentando aleatoriamente a prioridade dos threads prontos (nesse caso, os bloqueios de baixa prioridade).</span><span class="sxs-lookup"><span data-stu-id="614e3-112">The scheduler solves this problem by randomly boosting the priority of the ready threads (in this case, the low priority lock-holders).</span></span> <span data-ttu-id="614e3-113">Os threads de baixa prioridade são executados por tempo suficiente para sair da seção crítica e o thread de alta prioridade pode inserir a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="614e3-113">The low priority threads run long enough to exit the critical section, and the high-priority thread can enter the critical section.</span></span> <span data-ttu-id="614e3-114">Se o thread de baixa prioridade não obtiver tempo de CPU suficiente para sair da seção crítica pela primeira vez, ele receberá outra chance durante a próxima rodada de agendamento.</span><span class="sxs-lookup"><span data-stu-id="614e3-114">If the low-priority thread does not get enough CPU time to exit the critical section the first time, it will get another chance during the next round of scheduling.</span></span>

 

 



