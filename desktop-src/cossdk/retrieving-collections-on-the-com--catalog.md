---
description: Recuperando coleções no catálogo COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recuperando coleções no catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646282"
---
# <a name="retrieving-collections-on-the-com-catalog"></a><span data-ttu-id="b36d9-103">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="b36d9-103">Retrieving Collections on the COM+ Catalog</span></span>

<span data-ttu-id="b36d9-104">Os dados no catálogo COM+ são armazenados em uma hierarquia de coleções.</span><span class="sxs-lookup"><span data-stu-id="b36d9-104">Data on the COM+ catalog is stored within a hierarchy of collections.</span></span> <span data-ttu-id="b36d9-105">Na ferramenta administrativa serviços de componentes, muitas dessas coleções aparecem como pastas na árvore de console.</span><span class="sxs-lookup"><span data-stu-id="b36d9-105">In the Component Services administrative tool, many of these collections appear as folders in the console tree.</span></span> <span data-ttu-id="b36d9-106">As coleções que não aparecem como pastas só podem ser acessadas programaticamente.</span><span class="sxs-lookup"><span data-stu-id="b36d9-106">Collections that don't appear as folders can be accessed only programmatically.</span></span> <span data-ttu-id="b36d9-107">Coleções servem como contêineres para itens.</span><span class="sxs-lookup"><span data-stu-id="b36d9-107">Collections serve as containers for items.</span></span> <span data-ttu-id="b36d9-108">Os itens em uma determinada coleção são de um tipo consistente; ou seja, todos eles representam o mesmo tipo de elemento e pode haver um número arbitrário de itens em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="b36d9-108">The items in a given collection are all of a consistent type; that is, they all represent the same kind of element, and there can be an arbitrary number of items in a collection.</span></span> <span data-ttu-id="b36d9-109">Por exemplo, a coleção de [**aplicativos**](applications.md) contém um item para cada aplicativo com+ que está instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="b36d9-109">For example, the [**Applications**](applications.md) collection contains an item for each COM+ application that is installed on the machine.</span></span> <span data-ttu-id="b36d9-110">Essa coleção aparece na ferramenta administrativa como a pasta **aplicativos com+** .</span><span class="sxs-lookup"><span data-stu-id="b36d9-110">This collection appears in the administrative tool as the **COM+ Applications** folder.</span></span>

<span data-ttu-id="b36d9-111">As coleções ocorrem em uma estrutura hierárquica porque os elementos que elas contêm seguem uma ordem inato de inclusão.</span><span class="sxs-lookup"><span data-stu-id="b36d9-111">The collections occur in a hierarchical structure because the elements they contain follow an innate order of inclusion.</span></span> <span data-ttu-id="b36d9-112">Por exemplo, como os componentes são instalados em um aplicativo COM+, a coleção de [**componentes**](components.md) é logicamente incorporadasda na coleção de [**aplicativos**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="b36d9-112">For example, because components are installed into a COM+ application, the [**Components**](components.md) collection is logically subsumed under the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="b36d9-113">Mais especificamente, para manter os componentes instalados nesse aplicativo específico, há uma coleção de **componentes** distintos para cada item na coleção de **aplicativos** .</span><span class="sxs-lookup"><span data-stu-id="b36d9-113">More particularly, to hold the components installed into that particular application, there is a distinct **Components** collection for each item in the **Applications** collection.</span></span>

<span data-ttu-id="b36d9-114">Você deve obter uma coleção no catálogo sempre que desejar recuperar um item e definir propriedades nele.</span><span class="sxs-lookup"><span data-stu-id="b36d9-114">You must get a collection on the catalog whenever you want to retrieve an item and set properties on it.</span></span> <span data-ttu-id="b36d9-115">No caso geral, você precisa percorrer várias coleções para obter o elemento desejado.</span><span class="sxs-lookup"><span data-stu-id="b36d9-115">In the general case, you need to step through several collections to get to the element you want.</span></span> <span data-ttu-id="b36d9-116">Para obter o procedimento para fazer isso, consulte [navegando na hierarquia da coleção com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="b36d9-116">For the procedure for doing this, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="b36d9-117">Depois de recuperar uma coleção e antes de trabalhar diretamente com os itens que ela contém, você deve preencher a coleção, que busca dados para o conteúdo da coleção do catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="b36d9-117">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection, which fetches data for the collection's contents from the COM+ catalog.</span></span> <span data-ttu-id="b36d9-118">Para obter detalhes, consulte [populando coleções com+](populating-com--collections.md).</span><span class="sxs-lookup"><span data-stu-id="b36d9-118">For details, see [Populating COM+ Collections](populating-com--collections.md).</span></span>

<span data-ttu-id="b36d9-119">Além disso, há um recurso que você pode usar que permite consultar dinamicamente para ver quais coleções relacionadas estão disponíveis em uma determinada coleção que você está mantendo.</span><span class="sxs-lookup"><span data-stu-id="b36d9-119">Additionally, there is a facility you can use that enables you to dynamically query to see what related collections are available from a given collection you are holding.</span></span> <span data-ttu-id="b36d9-120">Para obter detalhes, consulte [consultando as coleções relacionadas disponíveis](querying-for-available-related-collections.md).</span><span class="sxs-lookup"><span data-stu-id="b36d9-120">For details, see [Querying for Available Related Collections](querying-for-available-related-collections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b36d9-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b36d9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b36d9-122">Operações de administração COM+ em transações</span><span class="sxs-lookup"><span data-stu-id="b36d9-122">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="b36d9-123">Manipulando erros de administração COM+</span><span class="sxs-lookup"><span data-stu-id="b36d9-123">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="b36d9-124">Exemplo introdutório usando o catálogo de administração do COM+</span><span class="sxs-lookup"><span data-stu-id="b36d9-124">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="b36d9-125">Visão geral dos objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="b36d9-125">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="b36d9-126">Definindo propriedades e salvando alterações no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="b36d9-126">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



