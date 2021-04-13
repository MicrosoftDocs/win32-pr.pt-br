---
description: Funções de depuração de seção crítica
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funções de depuração de seção crítica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500285"
---
# <a name="critical-section-debugging-functions"></a><span data-ttu-id="aae46-103">Funções de depuração de seção crítica</span><span class="sxs-lookup"><span data-stu-id="aae46-103">Critical Section Debugging Functions</span></span>

<span data-ttu-id="aae46-104">Essas funções ajudam a depurar seções críticas em seu código, o que pode facilitar a localização da causa de um deadlock.</span><span class="sxs-lookup"><span data-stu-id="aae46-104">These functions help to debug critical sections in your code, which can make it easier to find the cause of a deadlock.</span></span> <span data-ttu-id="aae46-105">Essas funções usam a classe auxiliar [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="aae46-105">These functions use the [**CCritSec**](ccritsec.md) helper class.</span></span>



| <span data-ttu-id="aae46-106">Função</span><span class="sxs-lookup"><span data-stu-id="aae46-106">Function</span></span>                             | <span data-ttu-id="aae46-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aae46-107">Description</span></span>                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="aae46-108">**CritCheckIn**</span><span class="sxs-lookup"><span data-stu-id="aae46-108">**CritCheckIn**</span></span>](critcheckin.md)   | <span data-ttu-id="aae46-109">Retornará **true** se o thread atual possuir a seção crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="aae46-109">Returns **TRUE** if the current thread owns the specified critical section.</span></span>  |
| [<span data-ttu-id="aae46-110">**CritCheckOut**</span><span class="sxs-lookup"><span data-stu-id="aae46-110">**CritCheckOut**</span></span>](critcheckout.md) | <span data-ttu-id="aae46-111">Retorna **false** se o thread atual possui a seção crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="aae46-111">Returns **FALSE** if the current thread owns the specified critical section.</span></span> |
| [<span data-ttu-id="aae46-112">**DbgLockTrace**</span><span class="sxs-lookup"><span data-stu-id="aae46-112">**DbgLockTrace**</span></span>](dbglocktrace.md) | <span data-ttu-id="aae46-113">Habilita ou desabilita o log de depuração para uma determinada seção crítica.</span><span class="sxs-lookup"><span data-stu-id="aae46-113">Enables or disables debug logging for a given critical section.</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="aae46-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aae46-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aae46-115">Utilitários de depuração</span><span class="sxs-lookup"><span data-stu-id="aae46-115">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



