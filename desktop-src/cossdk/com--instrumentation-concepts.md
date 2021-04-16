---
description: O serviço de instrumentação COM+ permite que você crie seus próprios programas de log e gerenciamento de eventos COM+ quando desejar exibir várias métricas de desempenho para seus componentes COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Conceitos de instrumentação COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765146"
---
# <a name="com-instrumentation-concepts"></a><span data-ttu-id="710a7-103">Conceitos de instrumentação COM+</span><span class="sxs-lookup"><span data-stu-id="710a7-103">COM+ Instrumentation Concepts</span></span>

<span data-ttu-id="710a7-104">O serviço de instrumentação COM+ permite que você crie seus próprios programas de log e gerenciamento de eventos COM+ quando desejar exibir várias métricas de desempenho para seus componentes COM+.</span><span class="sxs-lookup"><span data-stu-id="710a7-104">The COM+ instrumentation service enables you to build your own COM+ event management and logging programs when you want to display various performance metrics for your COM+ components.</span></span> <span data-ttu-id="710a7-105">A instrumentação COM+ também pode ser usada para configurar eventos definidos pelo usuário e para converter eventos COM+ em formato Visual Studio Analyzer (VSA) quando você estiver atualizando pacotes MTS que estão recebendo eventos MTS.</span><span class="sxs-lookup"><span data-stu-id="710a7-105">COM+ instrumentation can also be used to configure user-defined events and to convert COM+ events to Visual Studio Analyzer (VSA) format when you are upgrading MTS packages that are receiving MTS events.</span></span>

> [!Note]  
> <span data-ttu-id="710a7-106">A partir do Windows Server 2003, somente os administradores têm privilégios de acesso de leitura aos logs de rastreamento para eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="710a7-106">As of Windows Server 2003, only administrators have read access privileges to the trace logs for system events.</span></span>

 

<span data-ttu-id="710a7-107">Ao assinar os eventos publicados pelo editor de eventos do sistema, os clientes podem implementar as [interfaces de instrumentação do com+](com--instrumentation-interfaces.md) para receber notificações para uma variedade de métricas de desempenho do com+, como informações sobre objetos com+ específicos, aplicativos com+ e serviços com+.</span><span class="sxs-lookup"><span data-stu-id="710a7-107">By subscribing to the events published by the system events publisher, clients can implement the [COM+ instrumentation interfaces](com--instrumentation-interfaces.md) to receive notifications for a variety of COM+ performance metrics, such as information about specific COM+ objects, COM+ applications, and COM+ services.</span></span> <span data-ttu-id="710a7-108">As métricas são publicadas no cliente usando o [serviço de eventos com+](com--events.md), um sistema LCE (eventos menos acoplados) que armazena informações de eventos de editores diferentes em um repositório de eventos no catálogo com+.</span><span class="sxs-lookup"><span data-stu-id="710a7-108">The metrics are published to the client by using the [COM+ events service](com--events.md), a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.</span></span>

> [!Note]  
> <span data-ttu-id="710a7-109">A instrumentação COM+ não garante a entrega de um evento.</span><span class="sxs-lookup"><span data-stu-id="710a7-109">COM+ instrumentation does not guarantee the delivery of an event.</span></span>

 

<span data-ttu-id="710a7-110">Cada métrica tem um carimbo de data/hora que indica o horário em que a métrica foi gerada, não a hora em que foi expedida ou recebida.</span><span class="sxs-lookup"><span data-stu-id="710a7-110">Every metric has a timestamp that indicates the time when the metric was generated, not the time that it was dispatched or received.</span></span> <span data-ttu-id="710a7-111">O cliente pode correlacionar o carimbo de data/hora e descobrir o custo da execução de um aplicativo COM+, o custo de uma transação executada dentro de um aplicativo COM+ ou o custo de uma chamada de método dentro de um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="710a7-111">The client can correlate the timestamp and find out the cost of running a COM+ application, the cost of a transaction executed inside a COM+ application, or the cost of a method call inside of a COM+ application.</span></span>

<span data-ttu-id="710a7-112">Você também pode usar o serviço de instrumentação COM+ para filtrar as informações de métricas de desempenho específicas que você deseja ver.</span><span class="sxs-lookup"><span data-stu-id="710a7-112">You can also use the COM+ Instrumentation service to filter for the specific performance metrics information that you want to see.</span></span> <span data-ttu-id="710a7-113">Por exemplo, ao assinar um método ou uma interface de instrumentação COM+, você pode especificar propriedades para a assinatura na estrutura [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , como a ID do aplicativo (membro **guidApp** ) ou a ID do processo (membro **dwPid** ).</span><span class="sxs-lookup"><span data-stu-id="710a7-113">For example, when you subscribe to a COM+ instrumentation interface or method, you can specify properties for the subscription in the [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) structure, such as the application ID (**guidApp** member) or the process ID (**dwPid** member).</span></span>

<span data-ttu-id="710a7-114">Quando a ID do aplicativo é especificada, você recebe apenas as métricas do aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="710a7-114">When the application ID is specified, you receive only the metrics from the specified application.</span></span> <span data-ttu-id="710a7-115">Quando a ID do processo é especificada, você recebe métricas do aplicativo de servidor especificado e dos aplicativos de biblioteca que são carregados nesse processo.</span><span class="sxs-lookup"><span data-stu-id="710a7-115">When the process ID is specified, you receive metrics from the specified server application and library applications that are loaded in that process.</span></span> <span data-ttu-id="710a7-116">O usuário pode especificar a ID do aplicativo e a ID do processo, mas a ID do aplicativo deve ser a do aplicativo de servidor em execução no processo com a ID de processo especificada.</span><span class="sxs-lookup"><span data-stu-id="710a7-116">The user can specify both the application ID and the process ID, but the application ID has to be that of the server application running in the process with the specified process ID.</span></span> <span data-ttu-id="710a7-117">Se nenhum for especificado, o usuário receberá métricas de todos os aplicativos de servidor e de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="710a7-117">If neither is specified, the user receives metrics from all the server and library applications.</span></span>

<span data-ttu-id="710a7-118">As métricas de instrumentação COM+ fornecem informações suficientes para o aplicativo de monitoramento correlacioná-las com as métricas do sistema operacional para análise de desempenho, planejamento de capacidade e modelagem e previsão.</span><span class="sxs-lookup"><span data-stu-id="710a7-118">The COM+ instrumentation metrics provide enough information for the monitoring application to correlate them with the operating system metrics for performance analysis, capacity planning, and for modeling and prediction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="710a7-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="710a7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="710a7-120">Interfaces de instrumentação COM+</span><span class="sxs-lookup"><span data-stu-id="710a7-120">COM+ Instrumentation Interfaces</span></span>](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



