---
description: Os exemplos a seguir demonstram o uso de um manipulador de exceção.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Usando um manipulador de exceção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749656"
---
# <a name="using-an-exception-handler"></a><span data-ttu-id="17a9c-103">Usando um manipulador de exceção</span><span class="sxs-lookup"><span data-stu-id="17a9c-103">Using an Exception Handler</span></span>

<span data-ttu-id="17a9c-104">Os exemplos a seguir demonstram o uso de um manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="17a9c-104">The following examples demonstrate the use of an exception handler.</span></span>

## <a name="example-1"></a><span data-ttu-id="17a9c-105">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17a9c-105">Example 1</span></span>

<span data-ttu-id="17a9c-106">O fragmento de código a seguir usa a manipulação de exceção estruturada para verificar se uma operação de divisão em inteiros de 2 32 bits resultará em um erro de divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="17a9c-106">The following code fragment uses structured exception handling to check whether a division operation on two 32-bit integers will result in an division-by-zero error.</span></span> <span data-ttu-id="17a9c-107">Se isso ocorrer, a função retornará **false**; caso contrário, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="17a9c-107">If this occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>


```C++
BOOL SafeDiv(INT32 dividend, INT32 divisor, INT32 *pResult)
{
    __try 
    { 
        *pResult = dividend / divisor; 
    } 
    __except(GetExceptionCode() == EXCEPTION_INT_DIVIDE_BY_ZERO ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
    { 
        return FALSE;
    }
    return TRUE;
} 
```



## <a name="example-2"></a><span data-ttu-id="17a9c-108">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="17a9c-108">Example 2</span></span>

<span data-ttu-id="17a9c-109">A função de exemplo a seguir chama a função [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) e usa a manipulação de exceção estruturada para verificar se há uma exceção de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="17a9c-109">The following example function calls the [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function and uses structured exception handling to check for a breakpoint exception.</span></span> <span data-ttu-id="17a9c-110">Se ocorrer um, a função retornará **false**; caso contrário, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="17a9c-110">If one occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>

<span data-ttu-id="17a9c-111">A expressão de filtro no exemplo usa a função [**GetExceptionCode**](getexceptioncode.md) para verificar o tipo de exceção antes de executar o manipulador.</span><span class="sxs-lookup"><span data-stu-id="17a9c-111">The filter expression in the example uses the [**GetExceptionCode**](getexceptioncode.md) function to check the exception type before executing the handler.</span></span> <span data-ttu-id="17a9c-112">Isso permite que o sistema continue sua pesquisa para um manipulador apropriado se algum outro tipo de exceção ocorrer.</span><span class="sxs-lookup"><span data-stu-id="17a9c-112">This enables the system to continue its search for an appropriate handler if some other type of exception occurs.</span></span>

<span data-ttu-id="17a9c-113">Além disso, o uso da instrução **Return** no bloco **\_ \_ try** de um manipulador de exceção difere do uso de **Return** no bloco **\_ \_ try** de um manipulador de encerramento, o que causa um encerramento anormal do bloco **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="17a9c-113">Also, use of the **return** statement in the **\_\_try** block of an exception handler differs from the use of **return** in the **\_\_try** block of a termination handler, which causes an abnormal termination of the **\_\_try** block.</span></span> <span data-ttu-id="17a9c-114">Esse é um uso válido da instrução return em um manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="17a9c-114">This is an valid use of the return statement in an exception handler.</span></span>


```C++
BOOL CheckForDebugger()
{
    __try 
    {
        DebugBreak();
    }
    __except(GetExceptionCode() == EXCEPTION_BREAKPOINT ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH) 
    {
        // No debugger is attached, so return FALSE 
        // and continue.
        return FALSE;
    }
    return TRUE;
}
```



<span data-ttu-id="17a9c-115">Só retorna o \_ \_ manipulador de execução de exceção de um filtro de exceção quando o tipo de exceção é esperado e o endereço com falha é conhecido.</span><span class="sxs-lookup"><span data-stu-id="17a9c-115">Only return EXCEPTION\_EXECUTE\_HANDLER from an exception filter when the exception type is expected and the faulting address is known.</span></span> <span data-ttu-id="17a9c-116">Você deve permitir que o manipulador de exceção padrão processe tipos de exceção inesperados e endereços com falha.</span><span class="sxs-lookup"><span data-stu-id="17a9c-116">You should allow the default exception handler to process unexpected exception types and faulting addresses.</span></span>

## <a name="example-3"></a><span data-ttu-id="17a9c-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="17a9c-117">Example 3</span></span>

<span data-ttu-id="17a9c-118">O exemplo a seguir mostra a interação de manipuladores aninhados.</span><span class="sxs-lookup"><span data-stu-id="17a9c-118">The following example shows the interaction of nested handlers.</span></span> <span data-ttu-id="17a9c-119">A função [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) causa uma exceção no corpo protegido de um manipulador de encerramento que está dentro do corpo protegido de um manipulador de exceção.</span><span class="sxs-lookup"><span data-stu-id="17a9c-119">The [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) function causes an exception in the guarded body of a termination handler that is inside the guarded body of an exception handler.</span></span> <span data-ttu-id="17a9c-120">A exceção faz com que o sistema avalie a função FilterFunction, cujo valor de retorno, por sua vez, faz com que o manipulador de exceção seja invocado.</span><span class="sxs-lookup"><span data-stu-id="17a9c-120">The exception causes the system to evaluate the FilterFunction function, whose return value in turn causes the exception handler to be invoked.</span></span> <span data-ttu-id="17a9c-121">No entanto, antes da execução do bloco de manipulador de exceção, o bloco **\_ \_ finally** do manipulador de encerramento é executado porque o fluxo de controle saiu do bloco **\_ \_ try** do manipulador de encerramento.</span><span class="sxs-lookup"><span data-stu-id="17a9c-121">However, before the exception-handler block is executed, the **\_\_finally** block of the termination handler is executed because the flow of control has left the **\_\_try** block of the termination handler.</span></span>


```C++
DWORD FilterFunction() 
{ 
    printf("1 ");                     // printed first 
    return EXCEPTION_EXECUTE_HANDLER; 
} 
 
VOID main(VOID) 
{ 
    __try 
    { 
        __try 
        { 
            RaiseException( 
                1,                    // exception code 
                0,                    // continuable exception 
                0, NULL);             // no arguments 
        } 
        __finally 
        { 
            printf("2 ");             // this is printed second 
        } 
    } 
    __except ( FilterFunction() ) 
    { 
        printf("3\n");                // this is printed last 
    } 
}
```



 

 
