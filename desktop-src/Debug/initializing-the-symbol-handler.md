---
description: O código a seguir demonstra como inicializar o manipulador de símbolo.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Inicializando o manipulador de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920174"
---
# <a name="initializing-the-symbol-handler"></a><span data-ttu-id="87db6-103">Inicializando o manipulador de símbolo</span><span class="sxs-lookup"><span data-stu-id="87db6-103">Initializing the Symbol Handler</span></span>

<span data-ttu-id="87db6-104">O código a seguir demonstra como inicializar o manipulador de símbolo.</span><span class="sxs-lookup"><span data-stu-id="87db6-104">The following code demonstrates how to initialize the symbol handler.</span></span> <span data-ttu-id="87db6-105">A função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) adia o carregamento de símbolos até que as informações de símbolo sejam solicitadas.</span><span class="sxs-lookup"><span data-stu-id="87db6-105">The [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function defers symbol loading until symbol information is requested.</span></span> <span data-ttu-id="87db6-106">O código carrega os símbolos para cada módulo no processo especificado, passando um valor de **true** para o parâmetro *BInvade* da função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="87db6-106">The code loads the symbols for each module in the specified process by passing a value of **TRUE** for the *bInvade* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="87db6-107">(Essa função chama a função [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) para cada módulo que o processo mapeou em seu espaço de endereço.)</span><span class="sxs-lookup"><span data-stu-id="87db6-107">(This function calls the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) function for each module the process has mapped into its address space.)</span></span>

<span data-ttu-id="87db6-108">Se o processo especificado não for o processo que chamou [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), o código passará um identificador de processo como o primeiro parâmetro de **SymInitialize**.</span><span class="sxs-lookup"><span data-stu-id="87db6-108">If the specified process is not the process that called [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), the code passes a process identifier as the first parameter of **SymInitialize**.</span></span>

<span data-ttu-id="87db6-109">A especificação de **NULL** como o segundo parâmetro de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indica que o manipulador de símbolo deve usar o caminho de pesquisa padrão para localizar arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="87db6-109">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="87db6-110">Para obter informações detalhadas sobre como o manipulador de símbolo localiza arquivos de símbolo ou como um aplicativo pode especificar um caminho de pesquisa de símbolo, consulte [caminhos de símbolo](symbol-paths.md).</span><span class="sxs-lookup"><span data-stu-id="87db6-110">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



