---
description: As funções a seguir são usadas na manipulação de exceção estruturada.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funções de manipulação de exceção estruturada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762732"
---
# <a name="structured-exception-handling-functions"></a><span data-ttu-id="101d3-103">Funções de manipulação de exceção estruturada</span><span class="sxs-lookup"><span data-stu-id="101d3-103">Structured Exception Handling Functions</span></span>

<span data-ttu-id="101d3-104">As funções a seguir são usadas na manipulação de exceção estruturada.</span><span class="sxs-lookup"><span data-stu-id="101d3-104">The following functions are used in structured exception handling.</span></span>

-   [<span data-ttu-id="101d3-105">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="101d3-105">**AbnormalTermination**</span></span>](abnormaltermination.md)

    <span data-ttu-id="101d3-106">Indica se o bloco **\_ \_ try** de um manipulador de encerramento foi encerrado normalmente.</span><span class="sxs-lookup"><span data-stu-id="101d3-106">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span>

-   [<span data-ttu-id="101d3-107">**AddVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="101d3-107">**AddVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    <span data-ttu-id="101d3-108">Registra um manipulador de continuação em vetor.</span><span class="sxs-lookup"><span data-stu-id="101d3-108">Registers a vectored continue handler.</span></span>

-   [<span data-ttu-id="101d3-109">**AddVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="101d3-109">**AddVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    <span data-ttu-id="101d3-110">Registra um manipulador de exceção em vetor.</span><span class="sxs-lookup"><span data-stu-id="101d3-110">Registers a vectored exception handler.</span></span>

-   [<span data-ttu-id="101d3-111">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="101d3-111">**GetExceptionCode**</span></span>](getexceptioncode.md)

    <span data-ttu-id="101d3-112">Recupera um código que identifica o tipo de exceção que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="101d3-112">Retrieves a code that identifies the type of exception that occurred.</span></span>

-   [<span data-ttu-id="101d3-113">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="101d3-113">**GetExceptionInformation**</span></span>](getexceptioninformation.md)

    <span data-ttu-id="101d3-114">Recupera uma descrição independente de computador de uma exceção e informações sobre o estado da máquina que existia para o thread quando a exceção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="101d3-114">Retrieves a machine-independent description of an exception, and information about the machine state that existed for the thread when the exception occurred.</span></span>

-   [<span data-ttu-id="101d3-115">**RaiseException**</span><span class="sxs-lookup"><span data-stu-id="101d3-115">**RaiseException**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    <span data-ttu-id="101d3-116">Gera uma exceção no thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="101d3-116">Raises an exception in the calling thread.</span></span>

-   [<span data-ttu-id="101d3-117">**RemoveVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="101d3-117">**RemoveVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    <span data-ttu-id="101d3-118">Cancela o registro de um manipulador de continuação em vetor.</span><span class="sxs-lookup"><span data-stu-id="101d3-118">Unregisters a vectored continue handler.</span></span>

-   [<span data-ttu-id="101d3-119">**RemoveVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="101d3-119">**RemoveVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    <span data-ttu-id="101d3-120">Cancela o registro de um manipulador de exceção em vetor.</span><span class="sxs-lookup"><span data-stu-id="101d3-120">Unregisters a vectored exception handler.</span></span>

-   [<span data-ttu-id="101d3-121">**RtlAddGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="101d3-121">**RtlAddGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    <span data-ttu-id="101d3-122">Informa ao sistema de uma tabela de função dinâmica que representa uma região de memória que contém o código.</span><span class="sxs-lookup"><span data-stu-id="101d3-122">Informs the system of a dynamic function table representing a region of memory containing code.</span></span>

-   [<span data-ttu-id="101d3-123">**RtlDeleteGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="101d3-123">**RtlDeleteGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    <span data-ttu-id="101d3-124">Informa ao sistema que uma tabela de função dinâmica relatada anteriormente não está mais em uso.</span><span class="sxs-lookup"><span data-stu-id="101d3-124">Informs the system that a previously reported dynamic function table is no longer in use.</span></span>

-   [<span data-ttu-id="101d3-125">**RtlGrowFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="101d3-125">**RtlGrowFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    <span data-ttu-id="101d3-126">Relata que uma tabela de funções dinâmicas aumentou em tamanho.</span><span class="sxs-lookup"><span data-stu-id="101d3-126">Reports that a dynamic function table has increased in size.</span></span>

-   [<span data-ttu-id="101d3-127">**SetUnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="101d3-127">**SetUnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    <span data-ttu-id="101d3-128">Permite que um aplicativo substitua o manipulador de exceção de nível superior de cada thread e processo.</span><span class="sxs-lookup"><span data-stu-id="101d3-128">Enables an application to supersede the top-level exception handler of each thread and process.</span></span>

-   [<span data-ttu-id="101d3-129">**UnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="101d3-129">**UnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    <span data-ttu-id="101d3-130">Passa exceções sem tratamento para o depurador, se o processo estiver sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="101d3-130">Passes unhandled exceptions to the debugger, if the process is being debugged.</span></span>

-   [<span data-ttu-id="101d3-131">**VectoredHandler**</span><span class="sxs-lookup"><span data-stu-id="101d3-131">**VectoredHandler**</span></span>](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    <span data-ttu-id="101d3-132">Uma função definida pelo aplicativo que serve como um manipulador de exceção em vetor.</span><span class="sxs-lookup"><span data-stu-id="101d3-132">An application-defined function that serves as a vectored exception handler.</span></span>

<span data-ttu-id="101d3-133">As funções a seguir são usadas somente no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="101d3-133">The following functions are used only on 64-bit Windows.</span></span>

-   [<span data-ttu-id="101d3-134">**RtlAddFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="101d3-134">**RtlAddFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    <span data-ttu-id="101d3-135">Adiciona uma tabela de funções dinâmicas à lista tabela de funções dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="101d3-135">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="101d3-136">**RtlCaptureContext**</span><span class="sxs-lookup"><span data-stu-id="101d3-136">**RtlCaptureContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    <span data-ttu-id="101d3-137">Recupera um registro de contexto no contexto do chamador.</span><span class="sxs-lookup"><span data-stu-id="101d3-137">Retrieves a context record in the context of the caller.</span></span>

-   [<span data-ttu-id="101d3-138">**RtlDeleteFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="101d3-138">**RtlDeleteFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    <span data-ttu-id="101d3-139">Remove uma tabela de funções dinâmica da lista de tabela de funções dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="101d3-139">Removes a dynamic function table from the dynamic function table list.</span></span>

-   [<span data-ttu-id="101d3-140">**RtlInstallFunctionTableCallback**</span><span class="sxs-lookup"><span data-stu-id="101d3-140">**RtlInstallFunctionTableCallback**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    <span data-ttu-id="101d3-141">Adiciona uma tabela de funções dinâmicas à lista tabela de funções dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="101d3-141">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="101d3-142">**RtlRestoreContext**</span><span class="sxs-lookup"><span data-stu-id="101d3-142">**RtlRestoreContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    <span data-ttu-id="101d3-143">Restaura o contexto do chamador para o registro de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="101d3-143">Restores the context of the caller to the specified context record.</span></span>

 

 
