---
description: Para conservar o tempo e a memória ao trabalhar com muitos arquivos de símbolo, use a função SymSetOptions para definir a opção de carregamento de símbolo deferido ( \_ cargas DEferidas de SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Carregamento de símbolo adiado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920117"
---
# <a name="deferred-symbol-loading"></a><span data-ttu-id="402d2-103">Carregamento de símbolo adiado</span><span class="sxs-lookup"><span data-stu-id="402d2-103">Deferred Symbol Loading</span></span>

<span data-ttu-id="402d2-104">Para conservar o tempo e a memória ao trabalhar com muitos arquivos de símbolo, use a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para definir a opção de carregamento de símbolo deferido ( \_ cargas deferidas de SYMOPT \_ ) e, em seguida, use a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) ou [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) para carregar símbolos adiados para todos os módulos.</span><span class="sxs-lookup"><span data-stu-id="402d2-104">To conserve time and memory when working with many symbol files, use the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to set the deferred symbol loading (SYMOPT\_DEFERRED\_LOADS) option, then use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function to load symbols deferred for all modules.</span></span> <span data-ttu-id="402d2-105">O manipulador de símbolo listará os símbolos que estão disponíveis para os módulos, mas não mapeará as informações de depuração na memória até que ela seja solicitada.</span><span class="sxs-lookup"><span data-stu-id="402d2-105">The symbol handler will list symbols that are available for the modules, but will not map the debug information into memory until it is requested.</span></span> <span data-ttu-id="402d2-106">Esse é o método preferencial para usar com eficiência os símbolos de depuração.</span><span class="sxs-lookup"><span data-stu-id="402d2-106">This is the preferred method to efficiently use debugging symbols.</span></span> <span data-ttu-id="402d2-107">Todas as funções que usam símbolos são afetadas pelo carregamento de símbolo adiado.</span><span class="sxs-lookup"><span data-stu-id="402d2-107">All functions that use symbols are affected by deferred symbol loading.</span></span>

 

 



