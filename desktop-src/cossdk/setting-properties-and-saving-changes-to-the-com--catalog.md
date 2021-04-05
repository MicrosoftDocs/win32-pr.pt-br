---
description: Cada item em uma coleção expõe propriedades.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Editando propriedades no catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646343"
---
# <a name="editing-properties-in-the-com-catalog"></a><span data-ttu-id="91a58-103">Editando propriedades no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="91a58-103">Editing Properties in the COM+ Catalog</span></span>

<span data-ttu-id="91a58-104">Cada item em uma coleção expõe propriedades.</span><span class="sxs-lookup"><span data-stu-id="91a58-104">Each item in a collection exposes properties.</span></span> <span data-ttu-id="91a58-105">Essas propriedades servem para manter os dados de configuração para qualquer elemento que o item representa.</span><span class="sxs-lookup"><span data-stu-id="91a58-105">These properties serve to hold configuration data for whatever element the item represents.</span></span> <span data-ttu-id="91a58-106">Na ferramenta administrativa serviços de componentes, essas propriedades aparecem em uma página de propriedades que você acessa clicando com o botão direito do mouse em um item em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="91a58-106">In the Component Services administrative tool, these properties appear on a property page that you access by right-clicking an item in a folder.</span></span>

<span data-ttu-id="91a58-107">Como os itens em uma determinada coleção representam o mesmo tipo de coisa, esses itens expõem um conjunto de propriedades que é consistente na coleção.</span><span class="sxs-lookup"><span data-stu-id="91a58-107">Because the items in a given collection all represent the same kind of thing, those items expose a set of properties that is consistent across the collection.</span></span> <span data-ttu-id="91a58-108">Por exemplo, a coleção de [**aplicativos**](applications.md) expõe uma propriedade Name, uma propriedade AppID e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="91a58-108">For example, the [**Applications**](applications.md) collection exposes a Name property, an AppID property, and so forth.</span></span> <span data-ttu-id="91a58-109">Isso é análogo a como cada aplicativo na ferramenta administrativa serviços de componentes tem uma página de propriedades estruturada consistentemente disponível para ele.</span><span class="sxs-lookup"><span data-stu-id="91a58-109">This is analogous to how each application in the Component Services administrative tool has a consistently structured property page available for it.</span></span> <span data-ttu-id="91a58-110">Para obter uma lista de propriedades disponíveis para a coleção de **aplicativos** , consulte **aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="91a58-110">For a list of properties available to the **Applications** collection, see **Applications**.</span></span> <span data-ttu-id="91a58-111">Para obter uma lista de propriedades disponíveis para a coleção de [**componentes**](components.md) , consulte **componentes**.</span><span class="sxs-lookup"><span data-stu-id="91a58-111">For a list of properties available to the [**Components**](components.md) collection, see **Components**.</span></span>

<span data-ttu-id="91a58-112">Para obter uma lista completa das propriedades expostas por itens em cada coleção, consulte [coleções de administração do com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="91a58-112">For a complete list of properties exposed by items in each collection, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="91a58-113">Você representa um item em uma coleção usando um objeto criado a partir da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="91a58-113">You represent an item in a collection by using an object created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="91a58-114">Esse objeto permite que você defina e obtenha qualquer uma das propriedades expostas pelo item.</span><span class="sxs-lookup"><span data-stu-id="91a58-114">This object enables you to set and get any of the properties exposed by the item.</span></span> <span data-ttu-id="91a58-115">Ao definir propriedades, também é possível que você esteja contendendo com outro gravador para o catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="91a58-115">When setting properties, it is also possible that you might be contending with another writer to the COM+ catalog.</span></span> <span data-ttu-id="91a58-116">Para obter mais informações, consulte [obtendo e Configurando Propriedades](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="91a58-116">For more information, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

<span data-ttu-id="91a58-117">Depois de definir as propriedades, nenhuma alteração será realmente confirmada até que você salve explicitamente as alterações.</span><span class="sxs-lookup"><span data-stu-id="91a58-117">After you have set properties, no changes are actually committed until you explicitly save changes.</span></span> <span data-ttu-id="91a58-118">Para obter mais informações, consulte [salvando ou descartando alterações](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="91a58-118">For more information, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="91a58-119">Quando você salva as alterações, o catálogo COM+ impõe algumas lógicas de configuração para garantir que você não defina coisas para configurações incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="91a58-119">When you save changes, the COM+ catalog enforces some configuration logic to ensure that you don't set things to incompatible configurations.</span></span> <span data-ttu-id="91a58-120">Ele também altera algumas propriedades para você quando você altera explicitamente determinadas propriedades.</span><span class="sxs-lookup"><span data-stu-id="91a58-120">It also changes some properties for you when you explicitly change certain other properties.</span></span> <span data-ttu-id="91a58-121">Para obter mais informações, consulte [interdependências entre Propriedades](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="91a58-121">For more information, see [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="91a58-122">Além disso, o COM+ tem um recurso que permite a consulta dinâmica para ver quais propriedades estão disponíveis para os itens em uma determinada coleção.</span><span class="sxs-lookup"><span data-stu-id="91a58-122">Additionally, COM+ has a facility that enables you to dynamically query to see what properties are available for the items in a given collection.</span></span> <span data-ttu-id="91a58-123">Para obter detalhes, consulte [consultando as propriedades disponíveis](querying-for-available-properties.md).</span><span class="sxs-lookup"><span data-stu-id="91a58-123">For details, see [Querying for Available Properties](querying-for-available-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="91a58-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91a58-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91a58-125">Operações de administração COM+ em transações</span><span class="sxs-lookup"><span data-stu-id="91a58-125">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="91a58-126">Manipulando erros de administração COM+</span><span class="sxs-lookup"><span data-stu-id="91a58-126">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="91a58-127">Exemplo introdutório usando o catálogo de administração do COM+</span><span class="sxs-lookup"><span data-stu-id="91a58-127">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="91a58-128">Visão geral dos objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="91a58-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="91a58-129">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="91a58-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



