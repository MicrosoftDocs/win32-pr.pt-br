---
description: Gerenciador de recursos de cartão inteligente
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Gerenciador de recursos de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756572"
---
# <a name="smart-card-resource-manager"></a><span data-ttu-id="4596d-103">Gerenciador de recursos de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="4596d-103">Smart Card Resource Manager</span></span>

<span data-ttu-id="4596d-104">O [*Gerenciador de recursos*](../secgloss/r-gly.md) de [*cartão inteligente*](../secgloss/s-gly.md) gerencia o acesso a [*leitores*](../secgloss/r-gly.md) e a *cartões inteligentes*.</span><span class="sxs-lookup"><span data-stu-id="4596d-104">The [*smart card*](../secgloss/s-gly.md) [*resource manager*](../secgloss/r-gly.md) manages access to [*readers*](../secgloss/r-gly.md) and to *smart cards*.</span></span> <span data-ttu-id="4596d-105">Para gerenciar esses recursos, ele executa as seguintes funções.</span><span class="sxs-lookup"><span data-stu-id="4596d-105">To manage these resources, it performs the following functions.</span></span>

-   <span data-ttu-id="4596d-106">Identifica e controla os recursos.</span><span class="sxs-lookup"><span data-stu-id="4596d-106">Identifies and tracks resources.</span></span>
-   <span data-ttu-id="4596d-107">Aloca leitores e recursos em vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4596d-107">Allocates readers and resources across multiple applications.</span></span>
-   <span data-ttu-id="4596d-108">Dá suporte a primitivos de [*transação*](../secgloss/t-gly.md) para acessar serviços disponíveis em um determinado cartão.</span><span class="sxs-lookup"><span data-stu-id="4596d-108">Supports [*transaction*](../secgloss/t-gly.md) primitives for accessing services available on a given card.</span></span>
    > [!Note]  
    > <span data-ttu-id="4596d-109">Esse é um ponto importante porque os cartões atuais são dispositivos de thread único que geralmente exigem a execução de vários comandos para concluir uma única função.</span><span class="sxs-lookup"><span data-stu-id="4596d-109">This is an important point because current cards are single-threaded devices that often require the execution of multiple commands to complete a single function.</span></span> <span data-ttu-id="4596d-110">[*As transações*](../secgloss/t-gly.md) permitem que vários comandos sejam executados sem interrupção, garantindo que as informações de [*estado*](../secgloss/s-gly.md) intermediário não estejam corrompidas.</span><span class="sxs-lookup"><span data-stu-id="4596d-110">[*Transactions*](../secgloss/t-gly.md) allow multiple commands to be executed without interruption, ensuring that intermediate [*state*](../secgloss/s-gly.md) information is not corrupted.</span></span>

     

<span data-ttu-id="4596d-111">O Gerenciador de recursos pode ser acessado diretamente por meio da API do Resource Manager ou indiretamente por meio de qualquer [*provedor de serviço*](../secgloss/s-gly.md)de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="4596d-111">The resource manager can be accessed directly by way of the resource manager API or indirectly through any smart card [*service provider*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="4596d-112">A API do Gerenciador de recursos é um conjunto de funções do Windows que fornecem acesso direto aos serviços do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="4596d-112">The resource manager API is a set of Windows functions that provide direct access to the resource manager's services.</span></span> <span data-ttu-id="4596d-113">Para obter uma visão geral das funções do Windows fornecidas pela API, consulte [API do Gerenciador de recursos de cartão inteligente](smart-card-resource-manager-api.md).</span><span class="sxs-lookup"><span data-stu-id="4596d-113">For an overview of the Windows functions provided by the API, see [Smart Card Resource Manager API](smart-card-resource-manager-api.md).</span></span> <span data-ttu-id="4596d-114">Em comparação, os provedores de serviço de cartão inteligente usam interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="4596d-114">In comparison, smart card service providers use COM interfaces.</span></span>

<span data-ttu-id="4596d-115">Muitas das funções do Windows na API do Gerenciador de recursos têm equivalentes nas propriedades e nos métodos das interfaces COM dos provedores de serviço de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="4596d-115">Many of the Windows functions in the resource manager API have equivalents in the properties and methods of the smart card service providers' COM interfaces.</span></span> <span data-ttu-id="4596d-116">E, embora a maioria dos desenvolvedores de aplicativos encontre com mais facilidade para trabalhar, alguns aplicativos ainda precisarão usar as funções do Windows para executar determinadas tarefas.</span><span class="sxs-lookup"><span data-stu-id="4596d-116">And although most application developers will find COM easier to work with, some applications will still need to use the Windows functions to perform certain tasks.</span></span> <span data-ttu-id="4596d-117">Por exemplo, os aplicativos que precisam manipular a lista de leitores ou grupos de leitor no [*banco de dados de cartão inteligente*](../secgloss/s-gly.md), e aqueles que precisam de controle direto de um leitor, devem usar a API do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="4596d-117">For example, applications that need to manipulate the list of readers or reader groups in the [*smart card database*](../secgloss/s-gly.md), and those that need direct control of a reader, must use the resource manager API.</span></span> <span data-ttu-id="4596d-118">Os serviços que fornecem esses recursos estão disponíveis apenas nas funções do Windows, não no COM fornecido pelos provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="4596d-118">The services that provide these capabilities are available only in the Windows functions, not in the COM provided by the service providers.</span></span>

<span data-ttu-id="4596d-119">Para obter informações sobre como o [*Gerenciador de recursos*](../secgloss/r-gly.md) é implementado no Windows, consulte implementação do [Resource Manager](resource-manager-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4596d-119">For information about how the [*resource manager*](../secgloss/r-gly.md) is implemented in Windows, see [Resource Manager Implementation](resource-manager-implementation.md).</span></span>

 

 
