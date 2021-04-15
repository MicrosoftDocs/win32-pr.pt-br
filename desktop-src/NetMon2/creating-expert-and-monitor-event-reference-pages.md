---
description: Esta seção descreve como planejar, desenvolver e testar páginas de referência de eventos (ERPs) e como implantá-las em um especialista ou monitor. Para obter informações sobre ERPs e como usá-las com Monitor de Rede, consulte página de referência de evento.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Criando páginas de referência de evento expert e monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747305"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a><span data-ttu-id="521c5-104">Criando páginas de referência de evento expert e monitor</span><span class="sxs-lookup"><span data-stu-id="521c5-104">Creating Expert and Monitor Event Reference Pages</span></span>

<span data-ttu-id="521c5-105">Esta seção descreve como planejar, desenvolver e testar páginas de referência de eventos (ERPs) e como implantá-las em um especialista ou monitor.</span><span class="sxs-lookup"><span data-stu-id="521c5-105">This section describes how to plan, develop, and test event reference pages (ERPs) and how to deploy them in an expert or monitor.</span></span> <span data-ttu-id="521c5-106">Para obter informações sobre ERPs e como usá-las com Monitor de Rede, consulte [página de referência de evento](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="521c5-106">For information about ERPs and how to use them with Network Monitor, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="521c5-107">Para desenvolver um novo ERP, a primeira etapa é determinar os eventos que exigem ERPs individuais para seu [especialista](experts.md) ou [Monitor](monitors.md)personalizado.</span><span class="sxs-lookup"><span data-stu-id="521c5-107">To develop a new ERP, the first step is determining the events that require individual ERPs for your custom [expert](experts.md) or [monitor](monitors.md).</span></span> <span data-ttu-id="521c5-108">Você deve criar ERPs separadas para cada evento que deseja exibir no Visualizador de Eventos de Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="521c5-108">You must create separate ERPs for each event you wish to display in the Network Monitor Event Viewer.</span></span> <span data-ttu-id="521c5-109">Por exemplo, suponha que:</span><span class="sxs-lookup"><span data-stu-id="521c5-109">For example, suppose that:</span></span>

-   <span data-ttu-id="521c5-110">Você desenvolve um monitor chamado game monitor e o observador de estoque.</span><span class="sxs-lookup"><span data-stu-id="521c5-110">You develop a monitor named Game Monitor and Stock Watcher.</span></span>
-   <span data-ttu-id="521c5-111">O monitor está localizado em um arquivo chamado Gamemon.dll.</span><span class="sxs-lookup"><span data-stu-id="521c5-111">The monitor is located in a file called Gamemon.dll.</span></span>
-   <span data-ttu-id="521c5-112">O monitor gera dois eventos, jogos em execução e minhas ações de Internet alcança.</span><span class="sxs-lookup"><span data-stu-id="521c5-112">The monitor generates two events, Game Running and My Internet Stock Soars.</span></span>
-   <span data-ttu-id="521c5-113">Você planeja desenvolver dois ERPs, Gamemon1.htm e Gamemon2.htm.</span><span class="sxs-lookup"><span data-stu-id="521c5-113">You plan to develop two ERPs, Gamemon1.htm and Gamemon2.htm.</span></span>

> [!Note]  
> <span data-ttu-id="521c5-114">Não é necessário ter uma correspondência de um para um de ERPs para monitorar ou eventos de especialistas.</span><span class="sxs-lookup"><span data-stu-id="521c5-114">It's not necessary to have a one-to-one correspondence of ERPs to monitor or expert events.</span></span>

 

<span data-ttu-id="521c5-115">Depois de estabelecer uma lista de ERPs exclusivos, siga estas etapas para criar cada ERP.</span><span class="sxs-lookup"><span data-stu-id="521c5-115">After you have established a list of unique ERPs, follow these steps to create each ERP.</span></span>

-   <span data-ttu-id="521c5-116">[Escreva o documento de origem HTML](writing-an-event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="521c5-116">[Write the HTML source document](writing-an-event-reference-page.md).</span></span>
-   <span data-ttu-id="521c5-117">[Salve e nomeie](naming-an-event-reference-page.md) o arquivo de origem HTML como um arquivo. htm.</span><span class="sxs-lookup"><span data-stu-id="521c5-117">[Save and name](naming-an-event-reference-page.md) the HTML source file as an .htm file.</span></span>
-   <span data-ttu-id="521c5-118">[Teste o ERP](testing-an-event-reference-page.md) com o especialista ou o monitor concluído.</span><span class="sxs-lookup"><span data-stu-id="521c5-118">[Test the ERP](testing-an-event-reference-page.md) with the completed expert or monitor.</span></span>

 

 



