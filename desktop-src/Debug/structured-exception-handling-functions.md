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
# <a name="structured-exception-handling-functions"></a>Funções de manipulação de exceção estruturada

As funções a seguir são usadas na manipulação de exceção estruturada.

-   [**AbnormalTermination**](abnormaltermination.md)

    Indica se o bloco **\_ \_ try** de um manipulador de encerramento foi encerrado normalmente.

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Registra um manipulador de continuação em vetor.

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Registra um manipulador de exceção em vetor.

-   [**GetExceptionCode**](getexceptioncode.md)

    Recupera um código que identifica o tipo de exceção que ocorreu.

-   [**GetExceptionInformation**](getexceptioninformation.md)

    Recupera uma descrição independente de computador de uma exceção e informações sobre o estado da máquina que existia para o thread quando a exceção ocorreu.

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Gera uma exceção no thread de chamada.

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Cancela o registro de um manipulador de continuação em vetor.

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Cancela o registro de um manipulador de exceção em vetor.

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informa ao sistema de uma tabela de função dinâmica que representa uma região de memória que contém o código.

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informa ao sistema que uma tabela de função dinâmica relatada anteriormente não está mais em uso.

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Relata que uma tabela de funções dinâmicas aumentou em tamanho.

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Permite que um aplicativo substitua o manipulador de exceção de nível superior de cada thread e processo.

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Passa exceções sem tratamento para o depurador, se o processo estiver sendo depurado.

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Uma função definida pelo aplicativo que serve como um manipulador de exceção em vetor.

As funções a seguir são usadas somente no Windows de 64 bits.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Adiciona uma tabela de funções dinâmicas à lista tabela de funções dinâmicas.

-   [**RtlCaptureContext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Recupera um registro de contexto no contexto do chamador.

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Remove uma tabela de funções dinâmica da lista de tabela de funções dinâmicas.

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Adiciona uma tabela de funções dinâmicas à lista tabela de funções dinâmicas.

-   [**RtlRestoreContext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Restaura o contexto do chamador para o registro de contexto especificado.

 

 
