---
title: Afinidade de processador no WOW64
description: o Windows de 32 bits dá suporte a um máximo de 32 processadores. Portanto, as funções como GetProcessAffinityMask simulam um computador com processadores 32 quando chamados sob WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- afinidade do processador – programação de 64 bits do Windows
- Programação WOW64 de 64 bits do Windows, afinidade do processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641377"
---
# <a name="processor-affinity-under-wow64"></a><span data-ttu-id="942b5-106">Afinidade de processador no WOW64</span><span class="sxs-lookup"><span data-stu-id="942b5-106">Processor Affinity Under WOW64</span></span>

<span data-ttu-id="942b5-107">o Windows de 32 bits dá suporte a um máximo de 32 processadores.</span><span class="sxs-lookup"><span data-stu-id="942b5-107">32-bit Windows supports a maximum of 32 processors.</span></span> <span data-ttu-id="942b5-108">Portanto, as funções como [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulam um computador com processadores 32 quando chamados sob WOW64.</span><span class="sxs-lookup"><span data-stu-id="942b5-108">Therefore, functions such as [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulate a computer with 32 processors when called under WOW64.</span></span>

<span data-ttu-id="942b5-109">A máscara de afinidade é obtida com a execução de uma operação or bits ou de bit superior da máscara dos principais 32 de bits com o bit 32 inferior.</span><span class="sxs-lookup"><span data-stu-id="942b5-109">The affinity mask is obtained by performing a bitwise OR operation of the top 32 bits of the mask with the low 32 bits.</span></span> <span data-ttu-id="942b5-110">Portanto, se um thread tiver afinidade para os processadores 0, 1 e 32, o WOW64 relatará a afinidade como 0 e 1, porque o processador 32 é mapeado para o processador 0.</span><span class="sxs-lookup"><span data-stu-id="942b5-110">Therefore, if a thread has affinity for processors 0, 1, and 32, WOW64 reports the affinity as 0 and 1, because processor 32 maps to processor 0.</span></span> <span data-ttu-id="942b5-111">As funções que definem a afinidade do processador, como [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restringem os processadores aos primeiros 32 processadores em WOW64.</span><span class="sxs-lookup"><span data-stu-id="942b5-111">Functions that set processor affinity, such as [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restrict processors to the first 32 processors under WOW64.</span></span>

<span data-ttu-id="942b5-112">Para obter mais informações sobre a afinidade do processador, consulte [vários processadores](/windows/desktop/ProcThread/multiple-processors).</span><span class="sxs-lookup"><span data-stu-id="942b5-112">For more information about processor affinity, see [Multiple Processors](/windows/desktop/ProcThread/multiple-processors).</span></span>

 

 