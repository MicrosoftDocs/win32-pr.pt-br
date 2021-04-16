---
title: Falhas de alinhamento
description: Falhas de alinhamento
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- falhas de alinhamento de 64-programação do Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105768385"
---
# <a name="alignment-faults"></a><span data-ttu-id="83c71-104">Falhas de alinhamento</span><span class="sxs-lookup"><span data-stu-id="83c71-104">Alignment Faults</span></span>

<span data-ttu-id="83c71-105">O manipulador de falha de alinhamento do sistema é desativado por padrão em sistemas baseados em Itanium.</span><span class="sxs-lookup"><span data-stu-id="83c71-105">The system alignment-fault handler is turned off by default on Itanium-based systems.</span></span> <span data-ttu-id="83c71-106">Portanto, qualquer acesso a dados não alinhado gera uma exceção que não será automaticamente corrigida pelo sistema, a menos que o aplicativo Capture a exceção em um [manipulador de exceção baseado em quadro](/windows/desktop/Debug/frame-based-exception-handling).</span><span class="sxs-lookup"><span data-stu-id="83c71-106">Therefore, any unaligned data access generates an exception that will not automatically be fixed by the system unless the application catches the exception in a [frame-based exception handler](/windows/desktop/Debug/frame-based-exception-handling).</span></span> <span data-ttu-id="83c71-107">Para habilitar o alinhamento do sistema-falha no manipulador, chame a função [**SetError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) com **sem \_ NOALIGNMENTFAULTEXCEPT**.</span><span class="sxs-lookup"><span data-stu-id="83c71-107">To enable the system alignment-fault hander, call the [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with **SEM\_NOALIGNMENTFAULTEXCEPT**.</span></span> <span data-ttu-id="83c71-108">No entanto, observe que os processos podem apresentar uma degradação de desempenho grave se o manipulador de falhas de alinhamento do sistema estiver habilitado e o processo gerar falhas de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="83c71-108">However, note that processes may experience severe performance degradation if the system alignment-fault handler is enabled and the process generates alignment faults.</span></span>

<span data-ttu-id="83c71-109">Se o depurador do WinDbg tiver sido instalado como o depurador do sistema, o WinDbg será iniciado automaticamente se qualquer processo no sistema gerar uma exceção sem tratamento.</span><span class="sxs-lookup"><span data-stu-id="83c71-109">If the WinDbg debugger has been installed as the system debugger, WinDbg will automatically be launched if any process on the system generates an unhandled exception.</span></span> <span data-ttu-id="83c71-110">Se você não tiver um depurador instalado como o depurador do sistema, o sistema exibirá uma caixa de diálogo informando que seu aplicativo encontrou um erro e fornecendo a oportunidade de relatar o problema à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83c71-110">If you do not have a debugger installed as your system debugger, the system displays a dialog box stating that your application has encountered an error and providing the opportunity to report the problem to Microsoft.</span></span>

<span data-ttu-id="83c71-111">Em sistemas x64 e ARM64, quaisquer falhas de alinhamento são tratadas por uma combinação de hardware e software.</span><span class="sxs-lookup"><span data-stu-id="83c71-111">On x64 and ARM64 systems, any alignment faults are handled by a combination of hardware and software.</span></span> <span data-ttu-id="83c71-112">Para obter o melhor desempenho, todo o acesso à memória deve ser corretamente alinhado.</span><span class="sxs-lookup"><span data-stu-id="83c71-112">For best performance, all access to memory should be properly aligned.</span></span> <span data-ttu-id="83c71-113">Além disso, o [acesso a variáveis interprotegidas](/windows/desktop/Sync/interlocked-variable-access) não alinhadas deve ser evitado em ARM64, pois essas operações não são seguras Atomic.</span><span class="sxs-lookup"><span data-stu-id="83c71-113">In addition, unaligned [interlocked variable access](/windows/desktop/Sync/interlocked-variable-access) should be avoided on ARM64, as these operations are not atomic-safe.</span></span>

 

 