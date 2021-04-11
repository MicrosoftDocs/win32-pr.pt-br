---
description: Os objetos COMAdmin oferecem um modelo de objeto simples que fornece acesso ao catálogo COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Visão geral dos objetos COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089691"
---
# <a name="overview-of-the-comadmin-objects"></a><span data-ttu-id="06726-103">Visão geral dos objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="06726-103">Overview of the COMAdmin Objects</span></span>

<span data-ttu-id="06726-104">Os objetos COMAdmin oferecem um modelo de objeto simples que fornece acesso ao catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="06726-104">The COMAdmin objects offer a simple object model that provides you with access to the COM+ catalog.</span></span> <span data-ttu-id="06726-105">Ao fazer isso, eles servem para modelar toda a funcionalidade fornecida pela ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="06726-105">In doing so, they serve to model all the functionality provided by the Component Services administrative tool.</span></span> <span data-ttu-id="06726-106">Sempre que você fizer qualquer tipo de administração COM+, estará interagindo com o catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="06726-106">Whenever you do any kind of COM+ administration, you are interacting with the COM+ catalog.</span></span> <span data-ttu-id="06726-107">Para obter uma descrição do catálogo, consulte [acessando o catálogo com+](accessing-the-com--catalog.md).</span><span class="sxs-lookup"><span data-stu-id="06726-107">For a description of the catalog, see [Accessing the COM+ Catalog](accessing-the-com--catalog.md).</span></span>

<span data-ttu-id="06726-108">As informações obtidas da ferramenta administrativa serviços de componentes ou usando os objetos COMAdmin são estruturadas da mesma forma, e as ações executadas em qualquer contexto são análogas.</span><span class="sxs-lookup"><span data-stu-id="06726-108">The information you obtain either from the Component Services administrative tool or by using the COMAdmin objects is structured similarly, and the actions you perform in either context are analogous.</span></span> <span data-ttu-id="06726-109">A correlação básica entre usar o snap-in Serviços de componentes e a administração programática é que as pastas na árvore de console do snap-in correspondem às coleções no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="06726-109">The basic correlation between using the Component Services snap-in and programmatic administration is that folders in the console tree of the snap-in correspond to collections in the COM+ catalog.</span></span> <span data-ttu-id="06726-110">Ou seja, assim como cada pasta no snap-in contém itens de um tipo; por exemplo, **os aplicativos com+** mantêm aplicativos com+ instalados – cada coleção no catálogo com+ contém itens de um tipo uniforme.</span><span class="sxs-lookup"><span data-stu-id="06726-110">That is, just as each folder in the snap-in contains items all of a kind; for example, **COM+ Applications** holds installed COM+ applications—each collection in the COM+ catalog holds items of a uniform kind.</span></span> <span data-ttu-id="06726-111">Além disso, assim como cada item em uma pasta tem propriedades que podem ser definidas em uma folha de propriedades, cada item em uma coleção expõe as propriedades que podem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="06726-111">Further, just as each item in a folder has properties that you can set on a property sheet, each item in a collection exposes properties that you can set.</span></span>

<span data-ttu-id="06726-112">Para permitir que você configure objetos nessa estrutura, os objetos COMAdmin fornecem os meios para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="06726-112">To enable you to configure objects within this structure, the COMAdmin objects provide you with the means to do the following:</span></span>

-   <span data-ttu-id="06726-113">Acessar o catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="06726-113">Access the COM+ catalog</span></span>
-   <span data-ttu-id="06726-114">Coleções de acesso no catálogo</span><span class="sxs-lookup"><span data-stu-id="06726-114">Access collections in the catalog</span></span>
-   <span data-ttu-id="06726-115">Acessar itens em coleções</span><span class="sxs-lookup"><span data-stu-id="06726-115">Access items in collections</span></span>
-   <span data-ttu-id="06726-116">Acessar propriedades nos itens nas coleções</span><span class="sxs-lookup"><span data-stu-id="06726-116">Access properties on the items in the collections</span></span>

<span data-ttu-id="06726-117">Para dar suporte a essas ações, a biblioteca COMAdmin fornece as três seguintes classes:</span><span class="sxs-lookup"><span data-stu-id="06726-117">To support these actions, the COMAdmin Library provides the following three classes:</span></span>

-   <span data-ttu-id="06726-118">[**COMAdminCatalog**](comadmincatalog.md), que representa o próprio catálogo.</span><span class="sxs-lookup"><span data-stu-id="06726-118">[**COMAdminCatalog**](comadmincatalog.md), which represents the catalog itself.</span></span>
-   <span data-ttu-id="06726-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), que representa qualquer coleção.</span><span class="sxs-lookup"><span data-stu-id="06726-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), which represents any collection.</span></span>
-   <span data-ttu-id="06726-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), que representa qualquer item em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="06726-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), which represents any item in a collection.</span></span>

<span data-ttu-id="06726-121">Para obter descrições mais completas dessas classes, consulte [descrição resumida das classes COMAdmin](summary-description-of-the-comadmin-classes.md) nesta seção.</span><span class="sxs-lookup"><span data-stu-id="06726-121">For fuller descriptions of these classes, see [Summary Description of the COMAdmin Classes](summary-description-of-the-comadmin-classes.md) in this section.</span></span>

<span data-ttu-id="06726-122">Para ter uma ideia rápida das ações típicas executadas na administração programática, consulte [o exemplo introdutório usando o catálogo de administração do com+](introductory-example-using-the-com--administration-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="06726-122">To get a quick idea of typical actions you perform in programmatic administration, see [Introductory Example Using the COM+ Administration Catalog](introductory-example-using-the-com--administration-catalog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06726-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06726-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06726-124">Operações de administração COM+ em transações</span><span class="sxs-lookup"><span data-stu-id="06726-124">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="06726-125">Manipulando erros de administração COM+</span><span class="sxs-lookup"><span data-stu-id="06726-125">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="06726-126">Exemplo introdutório usando o catálogo de administração do COM+</span><span class="sxs-lookup"><span data-stu-id="06726-126">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="06726-127">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="06726-127">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="06726-128">Definindo propriedades e salvando alterações no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="06726-128">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



