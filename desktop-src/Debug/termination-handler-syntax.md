---
description: As \_ \_ \_ \_ palavras-chave try e finally são usadas para construir um manipulador de terminação. O exemplo a seguir mostra a estrutura de um manipulador de encerramento.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Sintaxe de Termination-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749657"
---
# <a name="termination-handler-syntax"></a><span data-ttu-id="8c654-104">Sintaxe de Termination-Handler</span><span class="sxs-lookup"><span data-stu-id="8c654-104">Termination-Handler Syntax</span></span>

<span data-ttu-id="8c654-105">As palavras-chave **\_ \_ try** e **\_ \_ finally** são usadas para construir um manipulador de terminação.</span><span class="sxs-lookup"><span data-stu-id="8c654-105">The **\_\_try** and **\_\_finally** keywords are used to construct a termination handler.</span></span> <span data-ttu-id="8c654-106">O exemplo a seguir mostra a estrutura de um manipulador de encerramento.</span><span class="sxs-lookup"><span data-stu-id="8c654-106">The following example shows the structure of a termination handler.</span></span>


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



<span data-ttu-id="8c654-107">Para obter exemplos, consulte [usando um manipulador de encerramento](using-a-termination-handler.md).</span><span class="sxs-lookup"><span data-stu-id="8c654-107">For examples, see [Using a Termination Handler](using-a-termination-handler.md).</span></span>

<span data-ttu-id="8c654-108">Assim como ocorre com o manipulador de exceção, o bloco **\_ \_ try** e o bloco **\_ \_ finally** exigem chaves ( {} ) e o uso de uma instrução **goto** para saltar em um dos blocos não é permitido.</span><span class="sxs-lookup"><span data-stu-id="8c654-108">As with the exception handler, both the **\_\_try** block and the **\_\_finally** block require braces ({}), and using a **goto** statement to jump into either block is not permitted.</span></span>

<span data-ttu-id="8c654-109">O bloco **\_ \_ try** contém o corpo protegido de código que é protegido pelo manipulador de encerramento.</span><span class="sxs-lookup"><span data-stu-id="8c654-109">The **\_\_try** block contains the guarded body of code that is protected by the termination handler.</span></span> <span data-ttu-id="8c654-110">Uma função pode ter qualquer número de manipuladores de terminação e esses blocos de tratamento de terminação podem ser aninhados dentro da mesma função ou em funções diferentes.</span><span class="sxs-lookup"><span data-stu-id="8c654-110">A function can have any number of termination handlers, and these termination-handling blocks can be nested within the same function or in different functions.</span></span>

<span data-ttu-id="8c654-111">O bloco **\_ \_ finally** é executado sempre que o fluxo de controle deixa o bloco **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="8c654-111">The **\_\_finally** block is executed whenever the flow of control leaves the **\_\_try** block.</span></span> <span data-ttu-id="8c654-112">No entanto, o bloco **\_ \_ finally** não será executado se você chamar qualquer uma das funções a seguir dentro do bloco **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)ou **Abort**.</span><span class="sxs-lookup"><span data-stu-id="8c654-112">However, the **\_\_finally** block is not executed if you call any of the following functions within the **\_\_try** block: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), or **abort**.</span></span>

<span data-ttu-id="8c654-113">O bloco **\_ \_ finally** é executado no contexto da função na qual o manipulador de terminação está localizado.</span><span class="sxs-lookup"><span data-stu-id="8c654-113">The **\_\_finally** block is executed in the context of the function in which the termination handler is located.</span></span> <span data-ttu-id="8c654-114">Isso significa que o bloco **\_ \_ finally** pode acessar as variáveis locais da função.</span><span class="sxs-lookup"><span data-stu-id="8c654-114">This means that the **\_\_finally** block can access that function's local variables.</span></span> <span data-ttu-id="8c654-115">A execução do bloco **\_ \_ finally** pode terminar por qualquer um dos seguintes meios.</span><span class="sxs-lookup"><span data-stu-id="8c654-115">Execution of the **\_\_finally** block can terminate by any of the following means.</span></span>

-   <span data-ttu-id="8c654-116">Execução da última instrução no bloco e continuação para a próxima instrução</span><span class="sxs-lookup"><span data-stu-id="8c654-116">Execution of the last statement in the block and continuation to the next instruction</span></span>
-   <span data-ttu-id="8c654-117">Uso de uma instrução de controle (**Return**, **Break**, **continue** ou **goto**)</span><span class="sxs-lookup"><span data-stu-id="8c654-117">Use of a control statement (**return**, **break**, **continue**, or **goto**)</span></span>
-   <span data-ttu-id="8c654-118">Uso de **longjmp** ou um salto para um manipulador de exceção</span><span class="sxs-lookup"><span data-stu-id="8c654-118">Use of **longjmp** or a jump to an exception handler</span></span>

<span data-ttu-id="8c654-119">Se a execução do bloco **\_ \_ try** for encerrada devido a uma exceção que invoca o bloco de tratamento de exceção de um manipulador de exceção baseado em quadro, o bloco **\_ \_ finally** será executado antes que o bloco de tratamento de exceção seja executado.</span><span class="sxs-lookup"><span data-stu-id="8c654-119">If execution of the **\_\_try** block terminates because of an exception that invokes the exception-handling block of a frame-based exception handler, the **\_\_finally** block is executed before the exception-handling block is executed.</span></span> <span data-ttu-id="8c654-120">Da mesma forma, uma chamada para a função de biblioteca de tempo de execução **longjmp** C do bloco **\_ \_ try** causa a execução do bloco **\_ \_ finally** antes da execução ser retomada no destino da operação **longjmp** .</span><span class="sxs-lookup"><span data-stu-id="8c654-120">Similarly, a call to the **longjmp** C run-time library function from the **\_\_try** block causes execution of the **\_\_finally** block before execution resumes at the target of the **longjmp** operation.</span></span> <span data-ttu-id="8c654-121">Se a execução do bloco **\_ \_ try** for encerrada devido a uma instrução de controle (**Return**, **Break**, **continue** ou **goto**), o bloco **\_ \_ finally** será executado.</span><span class="sxs-lookup"><span data-stu-id="8c654-121">If **\_\_try** block execution terminates due to a control statement (**return**, **break**, **continue**, or **goto**), the **\_\_finally** block is executed.</span></span>

<span data-ttu-id="8c654-122">A função [**AbnormalTermination**](abnormaltermination.md) pode ser usada no bloco **\_ \_ finally** para determinar se o bloco **\_ \_ try** foi encerrado sequencialmente – ou seja, se ele atingiu a chave de fechamento (}).</span><span class="sxs-lookup"><span data-stu-id="8c654-122">The [**AbnormalTermination**](abnormaltermination.md) function can be used within the **\_\_finally** block to determine whether the **\_\_try** block terminated sequentially — that is, whether it reached the closing brace (}).</span></span> <span data-ttu-id="8c654-123">Deixar o bloco **\_ \_ try** devido a uma chamada para **longjmp**, um salto para um manipulador de exceção ou uma instrução **Return**, **Break**, **continue** ou **goto** , é considerado um encerramento anormal.</span><span class="sxs-lookup"><span data-stu-id="8c654-123">Leaving the **\_\_try** block because of a call to **longjmp**, a jump to an exception handler, or a **return**, **break**, **continue**, or **goto** statement, is considered an abnormal termination.</span></span> <span data-ttu-id="8c654-124">Observe que a falha ao terminar sequencialmente faz com que o sistema Pesquise todos os quadros de pilha em ordem inversa para determinar se os manipuladores de encerramento devem ser chamados.</span><span class="sxs-lookup"><span data-stu-id="8c654-124">Note that failure to terminate sequentially causes the system to search through all stack frames in reverse order to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="8c654-125">Isso pode resultar em degradação do desempenho devido à execução de centenas de instruções.</span><span class="sxs-lookup"><span data-stu-id="8c654-125">This can result in performance degradation due to the execution of hundreds of instructions.</span></span>

<span data-ttu-id="8c654-126">Para evitar o encerramento anormal do manipulador de encerramento, a execução deve continuar no final do bloco.</span><span class="sxs-lookup"><span data-stu-id="8c654-126">To avoid abnormal termination of the termination handler, execution should continue to the end of the block.</span></span> <span data-ttu-id="8c654-127">Você também pode executar a instrução **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="8c654-127">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="8c654-128">A instrução **\_ \_ Leave** permite o encerramento imediato do bloco **\_ \_ try** sem causar um encerramento anormal e sua penalidade de desempenho.</span><span class="sxs-lookup"><span data-stu-id="8c654-128">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="8c654-129">Verifique a documentação do compilador para determinar se a instrução **\_ \_ Leave** tem suporte.</span><span class="sxs-lookup"><span data-stu-id="8c654-129">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

<span data-ttu-id="8c654-130">Se a execução do bloco **\_ \_ finally** terminar devido à instrução de controle de **retorno** , será equivalente a **goto** para a chave de fechamento na função de circunscrição.</span><span class="sxs-lookup"><span data-stu-id="8c654-130">If execution of the **\_\_finally** block terminates because of the **return** control statement, it is equivalent to a **goto** to the closing brace in the enclosing function.</span></span> <span data-ttu-id="8c654-131">Portanto, a função de circunscrição será retornada.</span><span class="sxs-lookup"><span data-stu-id="8c654-131">Therefore, the enclosing function will return.</span></span>

 

 
