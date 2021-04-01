---
title: Tratamento de exceção sob WOW64
description: O WOW64 usa exceções nativas x64, IA64 ou ARM64 como um transporte para exceções x86. Portanto, em um aplicativo de 32 bits em execução no WOW64, exceções não capturadas se comportam como exceções nativas de 64 bits.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008028"
---
# <a name="exception-handling-under-wow64"></a><span data-ttu-id="33265-104">Tratamento de exceção sob WOW64</span><span class="sxs-lookup"><span data-stu-id="33265-104">Exception Handling under WOW64</span></span>

<span data-ttu-id="33265-105">O WOW64 usa exceções nativas x64, IA64 ou ARM64 como um transporte para exceções x86.</span><span class="sxs-lookup"><span data-stu-id="33265-105">WOW64 uses native x64, ia64, or ARM64 exceptions as a transport for x86 exceptions.</span></span> <span data-ttu-id="33265-106">Portanto, em um aplicativo de 32 bits em execução no WOW64, exceções não capturadas se comportam como exceções nativas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="33265-106">Therefore, in a 32-bit application running under WOW64, uncaught exceptions behave like native 64-bit exceptions.</span></span>

<span data-ttu-id="33265-107">Em um aplicativo executado em uma versão de 32 bits do Windows, exceções não capturadas são passadas para manipuladores de exceção de nível superior do aplicativo, quando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="33265-107">In an application running on a 32-bit version of Windows, uncaught exceptions are passed on to higher-level exception handlers of the application, when available.</span></span> <span data-ttu-id="33265-108">No mesmo aplicativo de 32 bits em execução no WOW64, o sistema pode suprimir exceções não capturadas.</span><span class="sxs-lookup"><span data-stu-id="33265-108">In the same 32-bit application running under WOW64, the system may suppress uncaught exceptions.</span></span>

<span data-ttu-id="33265-109">**Windows Vista, Windows Server 2003 e Windows XP:** No mesmo aplicativo de 32 bits em execução no WOW64, o sistema chama os filtros de exceção, mas pode suprimir exceções não capturadas sem invocar os manipuladores associados.</span><span class="sxs-lookup"><span data-stu-id="33265-109">**Windows Vista, Windows Server 2003 and Windows XP:** In the same 32-bit application running under WOW64, the system calls the exception filters but may suppress uncaught exceptions without invoking the associated handlers.</span></span> <span data-ttu-id="33265-110">Esse comportamento mudou a partir do Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="33265-110">This behavior changed starting with Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="33265-111">Para obter mais informações sobre exceções não capturadas em procedimentos de janela, consulte a função [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="33265-111">For more information about uncaught exceptions in window procedures, see the [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

 

 