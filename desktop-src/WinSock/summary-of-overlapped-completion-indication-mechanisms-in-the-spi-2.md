---
description: Resumo dos mecanismos de indicação de conclusão sobreposta no SPI do Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Resumo dos mecanismos de indicação de conclusão sobreposta no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090354"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a><span data-ttu-id="280c1-103">Resumo dos mecanismos de indicação de conclusão sobreposta no SPI</span><span class="sxs-lookup"><span data-stu-id="280c1-103">Summary of Overlapped Completion Indication Mechanisms in the SPI</span></span>

<span data-ttu-id="280c1-104">A tabela a seguir resume a semântica de conclusão para um Soquete sobreposto, mostrando a várias combinações de *lpOverlapped*, **hEvent** e *lpCompletionRoutine*.</span><span class="sxs-lookup"><span data-stu-id="280c1-104">The following table summarizes the completion semantics for an overlapped socket, showing the various combination of *lpOverlapped*, **hEvent**, and *lpCompletionRoutine*.</span></span>



| <span data-ttu-id="280c1-105">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="280c1-105">*lpOverlapped*</span></span> | <span data-ttu-id="280c1-106">**hEvent**</span><span class="sxs-lookup"><span data-stu-id="280c1-106">**hEvent**</span></span>     | <span data-ttu-id="280c1-107">*lpCompletionRoutine*</span><span class="sxs-lookup"><span data-stu-id="280c1-107">*lpCompletionRoutine*</span></span> | <span data-ttu-id="280c1-108">Indicação de conclusão</span><span class="sxs-lookup"><span data-stu-id="280c1-108">Completion indication</span></span>                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="280c1-109">NULO</span><span class="sxs-lookup"><span data-stu-id="280c1-109">NULL</span></span>           | <span data-ttu-id="280c1-110">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="280c1-110">Not applicable</span></span> | <span data-ttu-id="280c1-111">Ignored</span><span class="sxs-lookup"><span data-stu-id="280c1-111">Ignored</span></span>               | <span data-ttu-id="280c1-112">A operação é concluída de forma síncrona, ou seja, se comporta como se fosse um soquete não sobreposto.</span><span class="sxs-lookup"><span data-stu-id="280c1-112">Operation completes synchronously, that is, it behaves as if it were a nonoverlapped socket.</span></span>                                                                                                                                 |
| <span data-ttu-id="280c1-113">não nulo</span><span class="sxs-lookup"><span data-stu-id="280c1-113">not NULL</span></span>       | <span data-ttu-id="280c1-114">NULO</span><span class="sxs-lookup"><span data-stu-id="280c1-114">NULL</span></span>           | <span data-ttu-id="280c1-115">NULO</span><span class="sxs-lookup"><span data-stu-id="280c1-115">NULL</span></span>                  | <span data-ttu-id="280c1-116">A operação é concluída sobreposta, mas não há nenhum mecanismo de conclusão com suporte do Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="280c1-116">Operation completes overlapped, but there is no Windows Sockets 2-supported completion mechanism.</span></span> <span data-ttu-id="280c1-117">O mecanismo de porta de conclusão (se houver suporte) pode ser usado nesse caso, caso contrário, não haverá nenhuma notificação de conclusão.</span><span class="sxs-lookup"><span data-stu-id="280c1-117">The completion port mechanism (if supported) may be used in this case, otherwise there will be no completion notification.</span></span> |
| <span data-ttu-id="280c1-118">não nulo</span><span class="sxs-lookup"><span data-stu-id="280c1-118">not NULL</span></span>       | <span data-ttu-id="280c1-119">não nulo</span><span class="sxs-lookup"><span data-stu-id="280c1-119">not NULL</span></span>       | <span data-ttu-id="280c1-120">NULO</span><span class="sxs-lookup"><span data-stu-id="280c1-120">NULL</span></span>                  | <span data-ttu-id="280c1-121">A operação é concluída sobreposta, notificação por objeto de evento de sinalização.</span><span class="sxs-lookup"><span data-stu-id="280c1-121">Operation completes overlapped, notification by signaling event object.</span></span>                                                                                                                                                      |
| <span data-ttu-id="280c1-122">não nulo</span><span class="sxs-lookup"><span data-stu-id="280c1-122">not NULL</span></span>       | <span data-ttu-id="280c1-123">Ignored</span><span class="sxs-lookup"><span data-stu-id="280c1-123">Ignored</span></span>        | <span data-ttu-id="280c1-124">não nulo</span><span class="sxs-lookup"><span data-stu-id="280c1-124">not NULL</span></span>              | <span data-ttu-id="280c1-125">A operação é concluída sobreposta, notificação pela rotina de conclusão do agendamento.</span><span class="sxs-lookup"><span data-stu-id="280c1-125">Operation completes overlapped, notification by scheduling completion routine.</span></span>                                                                                                                                               |



 

 

 



