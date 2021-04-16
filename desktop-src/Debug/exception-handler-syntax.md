---
description: As \_ \_ \_ \_ palavras-chave try e Except são usadas para construir um manipulador de exceção baseado em quadros. O exemplo a seguir mostra a estrutura de um manipulador de exceção.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Sintaxe de Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500756"
---
# <a name="exception-handler-syntax"></a><span data-ttu-id="db7c2-104">Sintaxe de Exception-Handler</span><span class="sxs-lookup"><span data-stu-id="db7c2-104">Exception-Handler Syntax</span></span>

<span data-ttu-id="db7c2-105">As palavras-chave **\_ \_ try** e **\_ \_ Except** são usadas para construir um manipulador de exceção baseado em quadros.</span><span class="sxs-lookup"><span data-stu-id="db7c2-105">The **\_\_try** and **\_\_except** keywords are used to construct a frame-based exception handler.</span></span> <span data-ttu-id="db7c2-106">O exemplo a seguir mostra a estrutura de um manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="db7c2-106">The following example shows the structure of an exception handler.</span></span>


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



<span data-ttu-id="db7c2-107">Observe que o bloco **\_ \_ try** e o bloco de manipulador de exceção exigem chaves ( {} ).</span><span class="sxs-lookup"><span data-stu-id="db7c2-107">Note that the **\_\_try** block and the exception-handler block require braces ({}).</span></span> <span data-ttu-id="db7c2-108">Não é permitido usar uma instrução **goto** para saltar no corpo de um bloco **\_ \_ try** ou em um bloco de manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="db7c2-108">Using a **goto** statement to jump into the body of a **\_\_try** block or into an exception-handler block is not permitted.</span></span> <span data-ttu-id="db7c2-109">Essa regra se aplica a manipuladores de exceção e manipuladores de terminação.</span><span class="sxs-lookup"><span data-stu-id="db7c2-109">This rule applies to both exception handlers and termination handlers.</span></span>

<span data-ttu-id="db7c2-110">O bloco **\_ \_ try** contém o corpo protegido de código que o manipulador de exceção protege.</span><span class="sxs-lookup"><span data-stu-id="db7c2-110">The **\_\_try** block contains the guarded body of code that the exception handler protects.</span></span> <span data-ttu-id="db7c2-111">Uma função pode ter qualquer número de manipuladores de exceção, e essas instruções de tratamento de exceções podem ser aninhadas dentro da mesma função ou em funções diferentes.</span><span class="sxs-lookup"><span data-stu-id="db7c2-111">A function can have any number of exception handlers, and these exception-handling statements can be nested within the same function or in different functions.</span></span> <span data-ttu-id="db7c2-112">Se ocorrer uma exceção dentro do bloco **\_ \_ try** , o sistema usará o controle e iniciará a pesquisa de um manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="db7c2-112">If an exception occurs within the **\_\_try** block, the system takes control and begins the search for an exception handler.</span></span> <span data-ttu-id="db7c2-113">Para obter uma descrição detalhada dessa pesquisa, consulte [manipulação de exceção](exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="db7c2-113">For a detailed description of this search, see [Exception Handling](exception-handling.md).</span></span>

<span data-ttu-id="db7c2-114">O manipulador de exceção recebe apenas exceções que ocorrem em um único thread.</span><span class="sxs-lookup"><span data-stu-id="db7c2-114">The exception handler receives only exceptions that occur within a single thread.</span></span> <span data-ttu-id="db7c2-115">Isso significa que, se um bloco **\_ \_ try** contiver uma chamada para a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , as exceções que ocorrerem no novo processo ou thread não serão expedidas para esse manipulador.</span><span class="sxs-lookup"><span data-stu-id="db7c2-115">This means that if a **\_\_try** block contains a call to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function, exceptions that occur within the new process or thread are not dispatched to this handler.</span></span>

<span data-ttu-id="db7c2-116">O sistema avalia a expressão de filtro de cada manipulador de exceção, protegendo o código no qual a exceção ocorreu até que a exceção seja tratada ou não haja mais manipuladores.</span><span class="sxs-lookup"><span data-stu-id="db7c2-116">The system evaluates the filter expression of each exception handler guarding the code in which the exception occurred until either the exception is handled or there are no more handlers.</span></span> <span data-ttu-id="db7c2-117">Uma expressão de filtro deve ser avaliada como um dos três valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="db7c2-117">A filter expression must be evaluated as one of the three following values.</span></span>



| <span data-ttu-id="db7c2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db7c2-118">Value</span></span>                              | <span data-ttu-id="db7c2-119">Significado</span><span class="sxs-lookup"><span data-stu-id="db7c2-119">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db7c2-120">**\_manipulador de execução de exceção \_**</span><span class="sxs-lookup"><span data-stu-id="db7c2-120">**EXCEPTION\_EXECUTE\_HANDLER**</span></span>    | <span data-ttu-id="db7c2-121">O sistema transfere o controle para o manipulador de exceção e a execução continua no registro de ativação no qual o manipulador é encontrado.</span><span class="sxs-lookup"><span data-stu-id="db7c2-121">The system transfers control to the exception handler, and execution continues in the stack frame in which the handler is found.</span></span>                                                                                       |
| <span data-ttu-id="db7c2-122">**EXCEÇÃO de \_ continuação da \_ pesquisa**</span><span class="sxs-lookup"><span data-stu-id="db7c2-122">**EXCEPTION\_CONTINUE\_SEARCH**</span></span>    | <span data-ttu-id="db7c2-123">O sistema continua a procurar um manipulador.</span><span class="sxs-lookup"><span data-stu-id="db7c2-123">The system continues to search for a handler.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="db7c2-124">**EXCEÇÃO de \_ continuação de \_ execução**</span><span class="sxs-lookup"><span data-stu-id="db7c2-124">**EXCEPTION\_CONTINUE\_EXECUTION**</span></span> | <span data-ttu-id="db7c2-125">O sistema interrompe a pesquisa de um manipulador e retorna o controle para o ponto em que a exceção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="db7c2-125">The system stops its search for a handler and returns control to the point at which the exception occurred.</span></span> <span data-ttu-id="db7c2-126">Se a exceção for não continuável, isso resultará em uma exceção de exceção de **\_ \_ não continuável de exceção** .</span><span class="sxs-lookup"><span data-stu-id="db7c2-126">If the exception is noncontinuable, this results in an **EXCEPTION\_NONCONTINUABLE\_EXCEPTION** exception.</span></span> |



 

<span data-ttu-id="db7c2-127">A expressão de filtro é avaliada no contexto da função na qual o manipulador de exceção está localizado, embora a exceção tenha ocorrido em uma função diferente.</span><span class="sxs-lookup"><span data-stu-id="db7c2-127">The filter expression is evaluated in the context of the function in which the exception handler is located, even though the exception may have occurred in a different function.</span></span> <span data-ttu-id="db7c2-128">Isso significa que a expressão de filtro pode acessar as variáveis locais da função.</span><span class="sxs-lookup"><span data-stu-id="db7c2-128">This means that the filter expression can access the function's local variables.</span></span> <span data-ttu-id="db7c2-129">Da mesma forma, o bloco do manipulador de exceção pode acessar as variáveis locais da função na qual ela está localizada.</span><span class="sxs-lookup"><span data-stu-id="db7c2-129">Similarly, the exception-handler block can access the local variables of the function in which it is located.</span></span>

<span data-ttu-id="db7c2-130">Para obter mais exemplos, consulte [usando um manipulador de exceção](using-an-exception-handler.md).</span><span class="sxs-lookup"><span data-stu-id="db7c2-130">For more examples, see [Using an Exception Handler](using-an-exception-handler.md).</span></span>

<span data-ttu-id="db7c2-131">Para obter mais informações sobre expressões de filtro e funções de filtro, consulte [manipulação de exceção baseada em quadros](frame-based-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="db7c2-131">For more information about filter expressions and filter functions, see [Frame-based Exception Handling](frame-based-exception-handling.md).</span></span>

 

 
