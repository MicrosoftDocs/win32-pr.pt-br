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
# <a name="using-an-exception-handler"></a>Usando um manipulador de exceção

Os exemplos a seguir demonstram o uso de um manipulador de exceção.

## <a name="example-1"></a>Exemplo 1

O fragmento de código a seguir usa a manipulação de exceção estruturada para verificar se uma operação de divisão em inteiros de 2 32 bits resultará em um erro de divisão por zero. Se isso ocorrer, a função retornará **false**; caso contrário, retornará **true**.


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



## <a name="example-2"></a>Exemplo 2

A função de exemplo a seguir chama a função [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) e usa a manipulação de exceção estruturada para verificar se há uma exceção de ponto de interrupção. Se ocorrer um, a função retornará **false**; caso contrário, retornará **true**.

A expressão de filtro no exemplo usa a função [**GetExceptionCode**](getexceptioncode.md) para verificar o tipo de exceção antes de executar o manipulador. Isso permite que o sistema continue sua pesquisa para um manipulador apropriado se algum outro tipo de exceção ocorrer.

Além disso, o uso da instrução **Return** no bloco **\_ \_ try** de um manipulador de exceção difere do uso de **Return** no bloco **\_ \_ try** de um manipulador de encerramento, o que causa um encerramento anormal do bloco **\_ \_ try** . Esse é um uso válido da instrução return em um manipulador de exceção.


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



Só retorna o \_ \_ manipulador de execução de exceção de um filtro de exceção quando o tipo de exceção é esperado e o endereço com falha é conhecido. Você deve permitir que o manipulador de exceção padrão processe tipos de exceção inesperados e endereços com falha.

## <a name="example-3"></a>Exemplo 3

O exemplo a seguir mostra a interação de manipuladores aninhados. A função [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) causa uma exceção no corpo protegido de um manipulador de encerramento que está dentro do corpo protegido de um manipulador de exceção. A exceção faz com que o sistema avalie a função FilterFunction, cujo valor de retorno, por sua vez, faz com que o manipulador de exceção seja invocado. No entanto, antes da execução do bloco de manipulador de exceção, o bloco **\_ \_ finally** do manipulador de encerramento é executado porque o fluxo de controle saiu do bloco **\_ \_ try** do manipulador de encerramento.


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



 

 
