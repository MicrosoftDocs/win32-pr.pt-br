---
description: Práticas recomendadas para minimizar serviços sem resposta
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Práticas recomendadas para minimizar serviços sem resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087994"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="8a663-103">Práticas recomendadas para minimizar serviços sem resposta</span><span class="sxs-lookup"><span data-stu-id="8a663-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="8a663-104">Plataforma afetada</span><span class="sxs-lookup"><span data-stu-id="8a663-104">Affected Platform</span></span>

 <span data-ttu-id="8a663-105">**Clientes** – Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a663-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="8a663-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a663-106">Description</span></span>

<span data-ttu-id="8a663-107">Os serviços sem resposta podem resultar em tempos limite, sessões encerradas e até mesmo perda de dados.</span><span class="sxs-lookup"><span data-stu-id="8a663-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="8a663-108">O emprego das práticas recomendadas pode reduzir muito a ocorrência de serviços sem resposta.</span><span class="sxs-lookup"><span data-stu-id="8a663-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="8a663-109">Práticas Recomendadas</span><span class="sxs-lookup"><span data-stu-id="8a663-109">Best Practices</span></span>

<span data-ttu-id="8a663-110">Verifique se seus aplicativos e todos os seus serviços e drivers dependentes respondem às notificações de energia e desligamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="8a663-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="8a663-111">Todos os aplicativos devem responder de forma imediata e apropriada para desligar mensagens como o WM \_ QUERYENDSESSION e \_ o WM EndSession que indicam que um desligamento está em andamento.</span><span class="sxs-lookup"><span data-stu-id="8a663-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="8a663-112">Todos os serviços devem responder imediatamente às notificações de desligamento do SCM.</span><span class="sxs-lookup"><span data-stu-id="8a663-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="8a663-113">Se eles não conseguirem fazer isso, o computador os tratará como sem resposta e iniciará um tempo limite de 20 segundos e os interromperá, abrindo a possibilidade de perda de dados.</span><span class="sxs-lookup"><span data-stu-id="8a663-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="8a663-114">Isso também adiciona 20 segundos ao tempo de desligamento de um computador desligado.</span><span class="sxs-lookup"><span data-stu-id="8a663-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="8a663-115">Todos os serviços que têm dependências de driver de dispositivo de kernel devem responder imediatamente e adequadamente para a \_ \_ notificação de desligamento do IRP MJ em suas rotinas de DispatchShutdown.</span><span class="sxs-lookup"><span data-stu-id="8a663-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="8a663-116">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="8a663-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="8a663-117">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="8a663-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



