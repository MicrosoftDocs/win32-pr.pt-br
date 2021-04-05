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
# <a name="error-handling-in-the-dll"></a><span data-ttu-id="a598f-103">Tratamento de erro na DLL</span><span class="sxs-lookup"><span data-stu-id="a598f-103">Error Handling in the DLL</span></span>

<span data-ttu-id="a598f-104">Use o log de eventos para registrar erros que ocorrem na DLL de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a598f-104">Use event logging to record errors that occur in the performance DLL.</span></span> <span data-ttu-id="a598f-105">O log de eventos de erro ajuda a solucionar problemas de aplicativos que fornecem dados de desempenho durante o desenvolvimento e após a instalação.</span><span class="sxs-lookup"><span data-stu-id="a598f-105">Logging error events aids in troubleshooting applications that provide performance data during development and after installation.</span></span> <span data-ttu-id="a598f-106">Você deve limitar a quantidade de log de erros que ocorre na função [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) porque a coleta de dados pode ser frequente.</span><span class="sxs-lookup"><span data-stu-id="a598f-106">You should limit the amount of error logging that occurs in the [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) function because data collection can be frequent.</span></span>

<span data-ttu-id="a598f-107">O sistema registra os seguintes erros no log de eventos se houver problemas com a função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a598f-107">The system logs the following errors to the event log if there are problems with the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span> <span data-ttu-id="a598f-108">Se um dos erros a seguir ocorrer, o sistema não chamará a DLL de desempenho novamente.</span><span class="sxs-lookup"><span data-stu-id="a598f-108">If one of the following errors occurs, the system does not call the performance DLL again.</span></span> <span data-ttu-id="a598f-109">Em vez disso, a DLL é descarregada.</span><span class="sxs-lookup"><span data-stu-id="a598f-109">Instead, the DLL is unloaded.</span></span>

-   <span data-ttu-id="a598f-110">**PERFLIB \_ Processo de abertura \_ \_ não \_ encontrado**— registrado quando o nome do procedimento definido no registro não foi encontrado na DLL como uma função exportada.</span><span class="sxs-lookup"><span data-stu-id="a598f-110">**PERFLIB\_OPEN\_PROC\_NOT\_FOUND**—Logged when the procedure name defined in the registry could not be found in the DLL as an exported function.</span></span> <span data-ttu-id="a598f-111">Isso geralmente ocorre quando a DLL ou o serviço não está instalado corretamente ou o nome da função foi renomeado sem Atualizar o procedimento de instalação.</span><span class="sxs-lookup"><span data-stu-id="a598f-111">This usually occurs when the DLL or the service is not installed correctly or the function name has been renamed without updating the installation procedure.</span></span>
-   <span data-ttu-id="a598f-112">**PERFLIB \_ \_ \_ Falha na abertura de proc**— registrada quando o procedimento aberto retornou um status de erro diferente de êxito do erro \_ .</span><span class="sxs-lookup"><span data-stu-id="a598f-112">**PERFLIB\_OPEN\_PROC\_FAILURE**—Logged when the open procedure returned an error status other than ERROR\_SUCCESS.</span></span> <span data-ttu-id="a598f-113">Caso isso aconteça, a DLL também deve ter inserido uma entrada de log de eventos que descreve as condições que causaram a falha.</span><span class="sxs-lookup"><span data-stu-id="a598f-113">Should this happen, the DLL should have also entered an event log entry describing the conditions that caused the failure.</span></span>
-   <span data-ttu-id="a598f-114">**PERFLIB \_ ABRIR \_ \_ exceção de proc**— registrado quando o procedimento Open encontra uma exceção sem tratamento.</span><span class="sxs-lookup"><span data-stu-id="a598f-114">**PERFLIB\_OPEN\_PROC\_EXCEPTION**—Logged when the open procedure encounters an unhandled exception.</span></span> <span data-ttu-id="a598f-115">Isso geralmente ocorre devido a uma condição de erro inesperada encontrada pelo procedimento Open.</span><span class="sxs-lookup"><span data-stu-id="a598f-115">This is usually due to an unexpected error condition encountered by the open procedure.</span></span>

 

 
