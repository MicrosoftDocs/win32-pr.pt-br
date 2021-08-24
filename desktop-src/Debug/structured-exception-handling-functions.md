---
description: As funções a seguir são usadas no tratamento de exceções estruturadas.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funções de tratamento de exceção estruturadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947cde636051e6d51428b1d75b7d299ce196b0f4335e096f99d6da6a277ae259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815496"
---
# <a name="structured-exception-handling-functions"></a>Funções de tratamento de exceção estruturadas

As funções a seguir são usadas no tratamento de exceções estruturadas.

-   [**AbnormalTermination**](abnormaltermination.md)

    Indica se o bloco **\_ \_ try** de um manipulador de encerramento terminou normalmente.

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Registra um manipulador continue vetored.

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Registra um manipulador de exceção vetor.

-   [**Getexceptioncode**](getexceptioncode.md)

    Recupera um código que identifica o tipo de exceção que ocorreu.

-   [**Getexceptioninformation**](getexceptioninformation.md)

    Recupera uma descrição independente de computador de uma exceção e informações sobre o estado do computador que existia para o thread quando a exceção ocorreu.

-   [**Raiseexception**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Gera uma exceção no thread de chamada.

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Unregisters a vectored continue handler.

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Não registrou um manipulador de exceção vetorado.

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informa o sistema de uma tabela de funções dinâmicas que representa uma região de memória que contém código.

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informa ao sistema que uma tabela de funções dinâmicas relatada anteriormente não está mais em uso.

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Relata que uma tabela de funções dinâmicas aumentou de tamanho.

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Permite que um aplicativo supere o manipulador de exceção de nível superior de cada thread e processo.

-   [**Unhandledexceptionfilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Passa exceções sem tratamento para o depurador, se o processo estiver sendo depurado.

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Uma função definida pelo aplicativo que serve como um manipulador de exceção vetor.

As funções a seguir são usadas somente em 64 bits Windows.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Adiciona uma tabela de funções dinâmicas à lista de tabelas de funções dinâmicas.

-   [**RtlCaptureContext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Recupera um registro de contexto no contexto do chamador.

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Remove uma tabela de funções dinâmicas da lista de tabelas de funções dinâmicas.

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Adiciona uma tabela de funções dinâmicas à lista de tabelas de funções dinâmicas.

-   [**RtlRestoreContext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Restaura o contexto do chamador para o registro de contexto especificado.

 

 
