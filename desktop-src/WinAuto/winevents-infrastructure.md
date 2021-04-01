---
title: Infraestrutura de WinEvents
description: O sistema operacional Microsoft Windows inclui um recurso, chamado WinEvents, que permite que processos e aplicativos em execução na área de trabalho do Windows troquem determinados tipos de informações.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103639076"
---
# <a name="winevents"></a><span data-ttu-id="0db05-103">WinEvents</span><span class="sxs-lookup"><span data-stu-id="0db05-103">WinEvents</span></span>

<span data-ttu-id="0db05-104">O sistema operacional Microsoft Windows inclui um recurso, chamado *WinEvents*, que permite que processos e aplicativos em execução na área de trabalho do Windows troquem determinados tipos de informações.</span><span class="sxs-lookup"><span data-stu-id="0db05-104">The Microsoft Windows operating system includes a feature, called *WinEvents*, that enables processes and applications running on the Windows desktop to exchange certain types of information.</span></span> <span data-ttu-id="0db05-105">As ferramentas de acessibilidade que usam a automação da interface do usuário da Microsoft e o Microsoft Acessibilidade Ativa estão entre os usuários primários do WinEvents.</span><span class="sxs-lookup"><span data-stu-id="0db05-105">Accessibility tools that use Microsoft UI Automation and Microsoft Active Accessibility are among the primary users of the WinEvents.</span></span>

<span data-ttu-id="0db05-106">No contexto de acessibilidade, os provedores de automação da interface do usuário e os Microsoft Acessibilidade Ativa Servers usam WinEvents para notificar os clientes sobre alterações em uma interface do usuário do aplicativo, como quando um elemento de interface do usuário foi criado ou destruído, ou quando um nome de elemento, estado ou valor foi alterado.</span><span class="sxs-lookup"><span data-stu-id="0db05-106">In the context of accessibility, UI Automation providers and Microsoft Active Accessibility servers use WinEvents to notify clients of changes in an application UI, such as when a UI element has been created or destroyed, or when an element name, state, or value has changed.</span></span>

<span data-ttu-id="0db05-107">Esta seção fornece sugestões, diretrizes e exemplos para ajudar os clientes a lidar com o WinEvents e para ajudar os servidores a determinar quando disparar o WinEvent apropriado.</span><span class="sxs-lookup"><span data-stu-id="0db05-107">This section provides suggestions, guidelines, and examples to help clients handle WinEvents and to help servers determine when to trigger the appropriate WinEvent.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0db05-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0db05-108">In this section</span></span>

-   [<span data-ttu-id="0db05-109">O que são WinEvents?</span><span class="sxs-lookup"><span data-stu-id="0db05-109">What Are WinEvents?</span></span>](what-are-winevents.md)
-   [<span data-ttu-id="0db05-110">Registrando uma função de gancho</span><span class="sxs-lookup"><span data-stu-id="0db05-110">Registering a Hook Function</span></span>](registering-a-hook-function.md)
-   [<span data-ttu-id="0db05-111">Eventos de nível de sistema e Object-Level</span><span class="sxs-lookup"><span data-stu-id="0db05-111">System-Level and Object-Level Events</span></span>](system-level-and-object-level-events.md)
-   [<span data-ttu-id="0db05-112">Funções de gancho in-context e out-of-Context</span><span class="sxs-lookup"><span data-stu-id="0db05-112">In-Context and Out-of-Context Hook Functions</span></span>](in-context-and-out-of-context-hook-functions.md)
-   [<span data-ttu-id="0db05-113">Proteção contra reentrância em funções de Hook</span><span class="sxs-lookup"><span data-stu-id="0db05-113">Guarding Against Reentrancy in Hook Functions</span></span>](guarding-against-reentrancy-in-hook-functions.md)
-   [<span data-ttu-id="0db05-114">Alocação de IDs WinEvent</span><span class="sxs-lookup"><span data-stu-id="0db05-114">Allocation of WinEvent IDs</span></span>](allocation-of-winevent-ids.md)

<span data-ttu-id="0db05-115">Para obter uma visão geral do processo de notificação de eventos no Microsoft Acessibilidade Ativa, consulte [WinEvents](winevents-overview.md) na [visão geral técnica](technical-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0db05-115">For an overview of the event notification process in Microsoft Active Accessibility, see [WinEvents](winevents-overview.md) in the [Technical Overview](technical-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0db05-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0db05-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0db05-117">Infraestrutura comum</span><span class="sxs-lookup"><span data-stu-id="0db05-117">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




