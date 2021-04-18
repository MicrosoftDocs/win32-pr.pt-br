---
title: Funções chamadas pelo sistema
description: Funções chamadas pelo sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- áudio de multimídia, funções do ACM
- áudio, funções do ACM
- Gerenciador de compactação de áudio (ACM), funções
- ACM (Gerenciador de compactação de áudio), funções
- Funções do ACM
- funções de retorno de chamada
- Gerenciador de compactação de áudio (ACM), funções de retorno de chamada
- ACM (Gerenciador de compactação de áudio), funções de retorno de chamada
- procedimentos de gancho
- procedimentos de driver
- Gerenciador de compactação de áudio (ACM), procedimentos de conexão
- ACM (Gerenciador de compactação de áudio), procedimentos de conexão
- Gerenciador de compactação de áudio (ACM), procedimentos de driver
- ACM (Gerenciador de compactação de áudio), procedimentos de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105749775"
---
# <a name="functions-called-by-the-system"></a><span data-ttu-id="e093c-117">Funções chamadas pelo sistema</span><span class="sxs-lookup"><span data-stu-id="e093c-117">Functions Called by the System</span></span>

<span data-ttu-id="e093c-118">O sistema chama três tipos diferentes de funções definidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e093c-118">The system calls three different kinds of application-defined functions.</span></span> <span data-ttu-id="e093c-119">As funções de retorno de chamada são funções em seu aplicativo que o sistema chama em resposta a uma solicitação feita por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e093c-119">Callback functions are functions in your application that the system calls in response to a request made by an application.</span></span> <span data-ttu-id="e093c-120">Os procedimentos de gancho ajudam um aplicativo a lidar com a personalização de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e093c-120">Hook procedures help an application handle the customization of dialog boxes.</span></span> <span data-ttu-id="e093c-121">Um procedimento de driver é a implementação de um aplicativo de seu próprio codec, conversor ou filtro.</span><span class="sxs-lookup"><span data-stu-id="e093c-121">A driver procedure is an application's implementation of its own codec, converter, or filter.</span></span>

<span data-ttu-id="e093c-122">As funções de retorno de chamada têm os seguintes nomes:</span><span class="sxs-lookup"><span data-stu-id="e093c-122">The callback functions have the following names:</span></span>

-   [<span data-ttu-id="e093c-123">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="e093c-123">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="e093c-124">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="e093c-124">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="e093c-125">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="e093c-125">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="e093c-126">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="e093c-126">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="e093c-127">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="e093c-127">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   <span data-ttu-id="e093c-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e093c-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>

<span data-ttu-id="e093c-129">A maioria das funções de enumeração no ACM usa funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e093c-129">Most of the enumeration functions in the ACM use callback functions.</span></span> <span data-ttu-id="e093c-130">Por exemplo, quando você chama uma função de enumeração, o ACM enumera os itens chamando repetidamente o aplicativo por meio da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e093c-130">For example, when you call an enumeration function, the ACM enumerates the items by repeatedly calling the application through the callback function.</span></span>

<span data-ttu-id="e093c-131">Algumas funções não podem ser chamadas de dentro dessas funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e093c-131">Some functions cannot be called from within these callback functions.</span></span> <span data-ttu-id="e093c-132">Funções que não podem ser chamadas manipular estruturas do ACM internas que são usadas pelas funções de enumeração.</span><span class="sxs-lookup"><span data-stu-id="e093c-132">Functions that cannot be called manipulate internal ACM structures that are used by the enumeration functions.</span></span> <span data-ttu-id="e093c-133">As funções a seguir não devem ser chamadas de dentro de uma função de retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="e093c-133">The following functions should not be called from within a callback function:</span></span>

-   [<span data-ttu-id="e093c-134">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="e093c-134">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="e093c-135">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="e093c-135">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="e093c-136">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="e093c-136">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

<span data-ttu-id="e093c-137">O sistema chama as seguintes funções para ajudar um aplicativo a lidar com a personalização de caixas de diálogo:</span><span class="sxs-lookup"><span data-stu-id="e093c-137">The system calls the following functions to help an application handle the customization of dialog boxes:</span></span>

-   [<span data-ttu-id="e093c-138">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="e093c-138">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="e093c-139">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="e093c-139">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

<span data-ttu-id="e093c-140">A função a seguir é especificada como um protótipo que permite que um aplicativo use um codec, conversor ou filtro personalizado.</span><span class="sxs-lookup"><span data-stu-id="e093c-140">The following function is specified as a prototype that allows an application to use a customized codec, converter, or filter.</span></span> <span data-ttu-id="e093c-141">Uma função que está de acordo com esse protótipo pode ser passada como um argumento para a função [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="e093c-141">A function conforming to this prototype may be passed as an argument to the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span>

-   [<span data-ttu-id="e093c-142">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="e093c-142">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 