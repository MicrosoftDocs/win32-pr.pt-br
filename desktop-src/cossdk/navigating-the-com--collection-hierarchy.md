---
description: Navegando na hierarquia da coleção COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navegando na hierarquia da coleção COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766936"
---
# <a name="navigating-the-com-collection-hierarchy"></a><span data-ttu-id="99bce-103">Navegando na hierarquia da coleção COM+</span><span class="sxs-lookup"><span data-stu-id="99bce-103">Navigating the COM+ Collection Hierarchy</span></span>

<span data-ttu-id="99bce-104">Algumas coleções que você pode recuperar facilmente usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) no objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="99bce-104">Some collections you can retrieve easily by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="99bce-105">Esse método recupera uma coleção de "nível superior"; ou seja, uma coleção, como [**aplicativos**](applications.md), que tem seu próprio e que é exclusiva e não logicamente incorporadas em outra coleção.</span><span class="sxs-lookup"><span data-stu-id="99bce-105">This method retrieves a "top-level" collection; that is, a collection such as [**Applications**](applications.md), which stands on its own and which is unique and not logically subsumed under another collection.</span></span>

<span data-ttu-id="99bce-106">No entanto, muitas coleções são logicamente incorporadasdas em outra coleção porque contêm elementos que fazem parte de uma estrutura maior.</span><span class="sxs-lookup"><span data-stu-id="99bce-106">Many collections, however, are logically subsumed under another collection because they contain elements that are part of some larger structure.</span></span> <span data-ttu-id="99bce-107">Por exemplo, a coleção de [**componentes**](components.md) é incorporadas, ou relacionada, à coleção de [**aplicativos**](applications.md) porque ela contém os componentes instalados em um aplicativo com+ específico, que por sua vez corresponde a um item na coleção de **aplicativos** .</span><span class="sxs-lookup"><span data-stu-id="99bce-107">For example, the [**Components**](components.md) collection is subsumed, or related, to the [**Applications**](applications.md) collection because it contains the components installed in a particular COM+ application, which itself corresponds to an item in the **Applications** collection.</span></span> <span data-ttu-id="99bce-108">Coleções relacionadas como esta não são exclusivas; Há uma coleção de **componentes** para cada aplicativo distinto.</span><span class="sxs-lookup"><span data-stu-id="99bce-108">Related collections such as this are not unique; there is a **Components** collection for each distinct application.</span></span>

<span data-ttu-id="99bce-109">Portanto, as coleções são organizadas em uma estrutura hierárquica que corresponde naturalmente às relações lógicas entre os itens que elas contêm.</span><span class="sxs-lookup"><span data-stu-id="99bce-109">Therefore, collections are arranged in a hierarchical structure that corresponds naturally to the logical relationships between the items they contain.</span></span> <span data-ttu-id="99bce-110">Um diagrama da hierarquia de coleção pode ser encontrado em [coleções de administração do com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="99bce-110">A diagram of the collection hierarchy can be found at [COM+ Administration Collections](com--administration-collections.md).</span></span> <span data-ttu-id="99bce-111">Para muitos dos elementos que você deseja configurar usando os objetos COMAdmin, você precisa navegar por alguma parte da hierarquia de coleção para recuperar o item apropriado.</span><span class="sxs-lookup"><span data-stu-id="99bce-111">For many of the elements that you want to configure using the COMAdmin objects, you need to navigate through some portion of the collection hierarchy to retrieve the appropriate item.</span></span>

<span data-ttu-id="99bce-112">O que isso significa na prática é que, se você quiser obter um item em uma coleção relacionada, será necessário percorrer todas as coleções de subsuming de nível superior necessárias primeiro.</span><span class="sxs-lookup"><span data-stu-id="99bce-112">What this means in practice is that if you want to get an item in a related collection, you need to go through all the necessary higher level, subsuming collections first.</span></span> <span data-ttu-id="99bce-113">E para recuperar uma coleção relacionada, você precisa recuperar o item específico na coleção pai à qual a coleção filho está relacionada.</span><span class="sxs-lookup"><span data-stu-id="99bce-113">And to retrieve a related collection, you need to retrieve the specific item in the parent collection to which the child collection is related.</span></span> <span data-ttu-id="99bce-114">Por exemplo, se você quiser configurar um item correspondente a um componente em um aplicativo COM+ específico, você deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="99bce-114">For example, if you want to configure an item corresponding to a component in a particular COM+ application, you must perform the following steps:</span></span>

1.  <span data-ttu-id="99bce-115">Obter a coleção de [**aplicativos**](applications.md) e preenchê-la.</span><span class="sxs-lookup"><span data-stu-id="99bce-115">Get the [**Applications**](applications.md) collection and populate it.</span></span>
2.  <span data-ttu-id="99bce-116">Enumere o conteúdo da coleção de [**aplicativos**](applications.md) até chegar ao item correspondente ao aplicativo com+ correto.</span><span class="sxs-lookup"><span data-stu-id="99bce-116">Enumerate through the contents of the [**Applications**](applications.md) collection until you get to the item corresponding to the correct COM+ application.</span></span>
3.  <span data-ttu-id="99bce-117">Obtenha e preencha a coleção de [**componentes**](components.md) para esse aplicativo com+ específico.</span><span class="sxs-lookup"><span data-stu-id="99bce-117">Get and populate the [**Components**](components.md) collection for that particular COM+ application.</span></span>
4.  <span data-ttu-id="99bce-118">Enumere o conteúdo da coleção de [**componentes**](components.md) até chegar ao item correspondente ao componente correto.</span><span class="sxs-lookup"><span data-stu-id="99bce-118">Enumerate through the contents of the [**Components**](components.md) collection until you get to the item corresponding to the correct component.</span></span>

<span data-ttu-id="99bce-119">O exemplo de Visual Basic a seguir da Microsoft mostra como executar as etapas anteriores:</span><span class="sxs-lookup"><span data-stu-id="99bce-119">The following Microsoft Visual Basic example shows how to perform the preceding steps:</span></span>


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



<span data-ttu-id="99bce-120">Dois métodos **GetCollection** distintos são usados no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="99bce-120">Two distinct **GetCollection** methods are used in the preceding example.</span></span> <span data-ttu-id="99bce-121">O primeiro é exposto por [**COMAdminCatalog**](comadmincatalog.md) e é usado para obter uma coleção de nível superior — neste caso, "Applications".</span><span class="sxs-lookup"><span data-stu-id="99bce-121">The first is exposed by [**COMAdminCatalog**](comadmincatalog.md) and is used to get a top-level collection—in this case, "Applications".</span></span> <span data-ttu-id="99bce-122">O segundo é exposto por [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e é usado para obter uma coleção relacionada à coleção atual; Você indica precisamente qual coleção deseja passando o nome "Components" e o valor da propriedade de chave do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="99bce-122">The second is exposed by [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and is used to get a collection related to the present collection; you indicate precisely which collection you want by passing in the name "Components" and the Key property value of the parent object.</span></span> <span data-ttu-id="99bce-123">O valor da propriedade de chave é geralmente um nome ou um GUID que identifica exclusivamente o objeto; Esse valor é identificado na documentação de cada coleção.</span><span class="sxs-lookup"><span data-stu-id="99bce-123">The Key property value is often a name or a GUID that uniquely identifies the object; this value is identified in the documentation for each collection.</span></span>

<span data-ttu-id="99bce-124">No caso mais geral, você precisa obter coleções relacionadas iterativamente na hierarquia de coleção até recuperar a coleção desejada.</span><span class="sxs-lookup"><span data-stu-id="99bce-124">In the most general case, you need to get related collections iteratively down the collection hierarchy until you retrieve the collection you want.</span></span> <span data-ttu-id="99bce-125">As etapas que você seguiria seguem o mesmo modelo geral, repetidamente.</span><span class="sxs-lookup"><span data-stu-id="99bce-125">The steps you would take follow the same general model, repetitively.</span></span> <span data-ttu-id="99bce-126">Para obter uma lista completa de coleções, consulte [coleções de administração do com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="99bce-126">For a complete list of collections, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="99bce-127">Em alguns casos, talvez você queira usar um método de atalho na segunda vez que seguir um caminho por meio da hierarquia de coleção.</span><span class="sxs-lookup"><span data-stu-id="99bce-127">In some cases, you might want to use a shortcut method the second time you follow a path through the collection hierarchy.</span></span> <span data-ttu-id="99bce-128">Você pode usar esse método somente depois que você já armazenou em cache todos os valores de chave intermediários.</span><span class="sxs-lookup"><span data-stu-id="99bce-128">You can use this method only after you have already cached all the intervening Key values.</span></span> <span data-ttu-id="99bce-129">Para obter detalhes, consulte [**ICOMAdminCatalog:: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span><span class="sxs-lookup"><span data-stu-id="99bce-129">For details, see [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99bce-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99bce-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99bce-131">Populando coleções COM+</span><span class="sxs-lookup"><span data-stu-id="99bce-131">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="99bce-132">Consultando coleções relacionadas disponíveis</span><span class="sxs-lookup"><span data-stu-id="99bce-132">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="99bce-133">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="99bce-133">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



