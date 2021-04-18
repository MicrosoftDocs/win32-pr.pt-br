---
description: Uma ação é executada no Windows Installer chamando a função MsiDoAction ou incluindo a ação em uma tabela de sequência.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Usando ações padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750589"
---
# <a name="using-standard-actions"></a><span data-ttu-id="60a0d-103">Usando ações padrão</span><span class="sxs-lookup"><span data-stu-id="60a0d-103">Using Standard Actions</span></span>

<span data-ttu-id="60a0d-104">Uma ação é executada no Windows Installer chamando a função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou incluindo a ação em uma tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="60a0d-104">An action is executed in the Windows Installer either by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function or including the action in a sequence table.</span></span> <span data-ttu-id="60a0d-105">Como a maioria das ações encapsula uma única finalidade, a maneira mais comum de usar ações é ordenar uma série de ações em uma sequência para realizar uma tarefa maior.</span><span class="sxs-lookup"><span data-stu-id="60a0d-105">Because most actions encapsulate a single purpose, the most common way to use actions is to order a series of actions into a sequence to accomplish a larger task.</span></span> <span data-ttu-id="60a0d-106">O instalador tem três ações de nível superior padrão que chamam um conjunto associado de tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="60a0d-106">The installer has three standard top-level actions that call an associated set of sequence tables.</span></span> <span data-ttu-id="60a0d-107">Essas tabelas de sequência associadas podem conter ações padrão, ações personalizadas e elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60a0d-107">These associated sequence tables may contain standard actions, custom actions, and user-interface elements.</span></span> <span data-ttu-id="60a0d-108">Cada ação em uma tabela de sequência tem um número de sequência associado e também pode ter uma expressão condicional associada.</span><span class="sxs-lookup"><span data-stu-id="60a0d-108">Each action in a sequence table has an associated sequence number and may also have an associated conditional expression.</span></span> <span data-ttu-id="60a0d-109">Todas as ações em uma tabela de sequência são visitadas em ordem e são executadas somente se a expressão condicional for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="60a0d-109">All actions in a sequence table are visited in order and are only executed if the conditional expression evaluates to True.</span></span>

<span data-ttu-id="60a0d-110">Embora uma ação padrão possa ter qualquer número de sequência associado a ela, muitas têm restrições de sequência que devem ser seguidas para que a ação funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="60a0d-110">While a standard action can have any sequence number associated with it, many have sequence restrictions which must be followed for the action to function properly.</span></span> <span data-ttu-id="60a0d-111">Por exemplo, a [ação filecusto](filecost-action.md)deve ser chamada após a [ação CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="60a0d-111">For example the [FileCost action](filecost-action.md), must be called after the [CostInitialize action](costinitialize-action.md).</span></span> <span data-ttu-id="60a0d-112">Para obter mais informações sobre as restrições de sequenciamento de ação padrão, consulte [ações com restrições de sequenciamento](actions-with-sequencing-restrictions.md), [ações sem restrições de sequenciamento](actions-without-sequencing-restrictions.md)ou [referência de ações padrão](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="60a0d-112">For more information on standard action sequencing restrictions, see [Actions with Sequencing Restrictions](actions-with-sequencing-restrictions.md), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md), or [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="60a0d-113">Os tópicos a seguir fornecem mais informações sobre o uso de ações padrão.</span><span class="sxs-lookup"><span data-stu-id="60a0d-113">The following topics provide more information about using standard actions.</span></span>

-   [<span data-ttu-id="60a0d-114">Publicando produtos, recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="60a0d-114">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)
-   [<span data-ttu-id="60a0d-115">Pesquisa de arquivos</span><span class="sxs-lookup"><span data-stu-id="60a0d-115">File Searching</span></span>](file-searching.md)
-   [<span data-ttu-id="60a0d-116">Custo do arquivo</span><span class="sxs-lookup"><span data-stu-id="60a0d-116">File Costing</span></span>](file-costing.md)
-   [<span data-ttu-id="60a0d-117">Instalação de arquivo</span><span class="sxs-lookup"><span data-stu-id="60a0d-117">File Installation</span></span>](file-installation.md)
-   [<span data-ttu-id="60a0d-118">Modificando o registro</span><span class="sxs-lookup"><span data-stu-id="60a0d-118">Modifying the Registry</span></span>](modifying-the-registry.md)
-   [<span data-ttu-id="60a0d-119">Executando ações</span><span class="sxs-lookup"><span data-stu-id="60a0d-119">Running Actions</span></span>](running-actions.md)

<span data-ttu-id="60a0d-120">Consulte também [sobre ações padrão](about-standard-actions.md) ou [referência de ações padrão](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="60a0d-120">See also [About Standard Actions](about-standard-actions.md) or [Standard Actions Reference](standard-actions-reference.md).</span></span>

 

 



