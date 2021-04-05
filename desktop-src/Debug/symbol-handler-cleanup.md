---
description: Para liberar toda a memória usada pelo manipulador de símbolo para um processo, use a função SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Limpeza do manipulador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826292"
---
# <a name="symbol-handler-cleanup"></a><span data-ttu-id="720bc-103">Limpeza do manipulador de símbolos</span><span class="sxs-lookup"><span data-stu-id="720bc-103">Symbol Handler Cleanup</span></span>

<span data-ttu-id="720bc-104">Para liberar toda a memória usada pelo manipulador de símbolo para um processo, use a função [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) .</span><span class="sxs-lookup"><span data-stu-id="720bc-104">To free all the memory used by the symbol handler for a process, use the [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) function.</span></span> <span data-ttu-id="720bc-105">Essa função enumera todos os módulos carregados, libera cada módulo e libera a memória alocada para a lista de módulos.</span><span class="sxs-lookup"><span data-stu-id="720bc-105">This function enumerates all loaded modules, frees each module, and frees the memory allocated for the list of modules.</span></span> <span data-ttu-id="720bc-106">Depois de chamar **SymCleanup**, você não poderá usar o identificador de processo nas funções de tratamento de símbolos até chamar a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="720bc-106">After you call **SymCleanup**, you cannot use the process handle in the symbol handling functions until you call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

 

 



