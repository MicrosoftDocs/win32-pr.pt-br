---
description: O \_ mutex MSIExecute é definido somente durante o processamento da tabela InstallExecuteSequence, tabela AdminExecuteSequence ou tabela AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828107"
---
# <a name="_msiexecute-mutex"></a><span data-ttu-id="f59d0-103">\_Mutex MSIExecute</span><span class="sxs-lookup"><span data-stu-id="f59d0-103">\_MSIExecute Mutex</span></span>

<span data-ttu-id="f59d0-104">O \_ mutex MSIExecute é definido somente durante o processamento da tabela [InstallExecuteSequence](installexecutesequence-table.md), [tabela AdminExecuteSequence](adminexecutesequence-table.md)ou [tabela AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f59d0-104">The \_MSIExecute Mutex is set only while processing the [InstallExecuteSequence table](installexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

<span data-ttu-id="f59d0-105">Como duas instalações não podem ser executadas no mesmo processo, uma tentativa de chamar a API (interface de programação de aplicativo) do instalador retorna um erro \_ \_ de instalação já \_ em execução (1618) em dois casos:</span><span class="sxs-lookup"><span data-stu-id="f59d0-105">Because two installations cannot be run in the same process, an attempt to call the installer's application programming interface (API) returns ERROR\_INSTALL\_ALREADY\_RUNNING (1618) in two cases:</span></span>

-   <span data-ttu-id="f59d0-106">Enquanto o \_ mutex MSIExecute é definido.</span><span class="sxs-lookup"><span data-stu-id="f59d0-106">While the \_MSIExecute Mutex is set.</span></span>
-   <span data-ttu-id="f59d0-107">Enquanto o processo atual está processando a tabela [InstallUISequence](installuisequence-table.md) ou a [tabela AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f59d0-107">While the current process is processing the [InstallUISequence table](installuisequence-table.md) or [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="f59d0-108">Consulte as mensagens de [log de eventos](event-logging.md) para obter informações sobre qual aplicativo está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="f59d0-108">See the [Event Logging](event-logging.md) messages for information about what application is being installed.</span></span>

<span data-ttu-id="f59d0-109">Nos casos em que é impraticável retornar um erro de \_ instalação \_ já \_ em execução, você pode recuperar o status atual do serviço de Windows Installer antes de tentar iniciar a instalação usando a função [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) .</span><span class="sxs-lookup"><span data-stu-id="f59d0-109">In cases where it is impractical to return an ERROR\_INSTALL\_ALREADY\_RUNNING error, you can retrieve the current status of the Windows Installer service before attempting to start the installation by using the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function.</span></span> <span data-ttu-id="f59d0-110">O serviço de Windows Installer está em execução no momento se o valor do membro **dwControlsAccepted** da estrutura de [**processo de \_ status \_ do serviço**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) retornado for **serviço de \_ \_ desligamento de aceitação**.</span><span class="sxs-lookup"><span data-stu-id="f59d0-110">The Windows Installer service is currently running if the value of the **dwControlsAccepted** member of the returned [**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) structure is **SERVICE\_ACCEPT\_SHUTDOWN**.</span></span>

<span data-ttu-id="f59d0-111">**Windows Installer 2,0:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f59d0-111">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="f59d0-112">O uso da função [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) para recuperar o status atual do serviço de Windows Installer requer Windows Installer versão 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="f59d0-112">The use of the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function to retrieve the current status of the Windows Installer service requires Windows Installer version 3.0 or greater.</span></span>

 

 
