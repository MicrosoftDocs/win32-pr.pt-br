---
description: Use o log de eventos para registrar erros que ocorrem na DLL de desempenho.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Tratamento de erro na DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a64dcfdf360a1dcc2301b5496d3f4630631cd7bfbc3fffb0e2cd5408120351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517466"
---
# <a name="error-handling-in-the-dll"></a>Tratamento de erro na DLL

Use o log de eventos para registrar erros que ocorrem na DLL de desempenho. O registro em log de eventos de erro auxilia na solução de problemas de aplicativos que fornecem dados de desempenho durante o desenvolvimento e após a instalação. Você deve limitar a quantidade de log de erros que ocorre na [**função CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) porque a coleta de dados pode ser frequente.

O sistema registra os seguintes erros no log de eventos se houver problemas com a [**função OpenPerformanceData.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) Se ocorrer um dos erros a seguir, o sistema não chamará a DLL de desempenho novamente. Em vez disso, a DLL é descarregada.

-   **PERFLIB \_ OPEN \_ PROC \_ NOT \_ FOUND**— registrado quando o nome do procedimento definido no Registro não pôde ser encontrado na DLL como uma função exportada. Isso geralmente ocorre quando a DLL ou o serviço não está instalado corretamente ou o nome da função foi renomeado sem atualizar o procedimento de instalação.
-   **PERFLIB \_ OPEN \_ PROC \_ FAILURE**— registrado quando o procedimento aberto retornou um status de erro diferente de ERROR \_ SUCCESS. Se isso acontecer, a DLL também deve ter inserido uma entrada de log de eventos que descreve as condições que causaram a falha.
-   **PERFLIB \_ OPEN \_ PROC \_ EXCEPTION**— registrado quando o procedimento aberto encontra uma exceção sem-manuseio. Isso geralmente ocorre devido a uma condição de erro inesperada encontrada pelo procedimento aberto.

 

 
