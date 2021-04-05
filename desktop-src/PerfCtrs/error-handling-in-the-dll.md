---
description: Use o log de eventos para registrar erros que ocorrem na DLL de desempenho.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Tratamento de erro na DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921745"
---
# <a name="error-handling-in-the-dll"></a>Tratamento de erro na DLL

Use o log de eventos para registrar erros que ocorrem na DLL de desempenho. O log de eventos de erro ajuda a solucionar problemas de aplicativos que fornecem dados de desempenho durante o desenvolvimento e após a instalação. Você deve limitar a quantidade de log de erros que ocorre na função [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) porque a coleta de dados pode ser frequente.

O sistema registra os seguintes erros no log de eventos se houver problemas com a função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) . Se um dos erros a seguir ocorrer, o sistema não chamará a DLL de desempenho novamente. Em vez disso, a DLL é descarregada.

-   **PERFLIB \_ Processo de abertura \_ \_ não \_ encontrado**— registrado quando o nome do procedimento definido no registro não foi encontrado na DLL como uma função exportada. Isso geralmente ocorre quando a DLL ou o serviço não está instalado corretamente ou o nome da função foi renomeado sem Atualizar o procedimento de instalação.
-   **PERFLIB \_ \_ \_ Falha na abertura de proc**— registrada quando o procedimento aberto retornou um status de erro diferente de êxito do erro \_ . Caso isso aconteça, a DLL também deve ter inserido uma entrada de log de eventos que descreve as condições que causaram a falha.
-   **PERFLIB \_ ABRIR \_ \_ exceção de proc**— registrado quando o procedimento Open encontra uma exceção sem tratamento. Isso geralmente ocorre devido a uma condição de erro inesperada encontrada pelo procedimento Open.

 

 
