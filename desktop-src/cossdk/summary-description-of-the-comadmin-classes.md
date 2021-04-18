---
description: Há três classes fornecidas pela biblioteca COMAdmin (comadmin.dll), cada uma implementando uma interface COM dupla.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Descrição resumida das classes COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753204"
---
# <a name="summary-description-of-the-comadmin-classes"></a><span data-ttu-id="44a7f-103">Descrição resumida das classes COMAdmin</span><span class="sxs-lookup"><span data-stu-id="44a7f-103">Summary Description of the COMAdmin Classes</span></span>

<span data-ttu-id="44a7f-104">Há três classes fornecidas pela biblioteca COMAdmin (comadmin.dll), cada uma implementando uma interface COM dupla.</span><span class="sxs-lookup"><span data-stu-id="44a7f-104">There are three classes provided by the COMAdmin library (comadmin.dll), each of which implements a COM dual interface.</span></span> <span data-ttu-id="44a7f-105">Você usa objetos criados a partir dessas classes para obter acesso ao catálogo, para representar as coleções no catálogo e para representar os itens contidos nas coleções.</span><span class="sxs-lookup"><span data-stu-id="44a7f-105">You use objects created from these classes to gain access to the catalog, to represent collections in the catalog, and to represent the items contained within collections.</span></span>

## <a name="comadmincatalog"></a><span data-ttu-id="44a7f-106">COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="44a7f-106">COMAdminCatalog</span></span>

<span data-ttu-id="44a7f-107">A classe [**COMAdminCatalog**](comadmincatalog.md) representa o próprio catálogo.</span><span class="sxs-lookup"><span data-stu-id="44a7f-107">The [**COMAdminCatalog**](comadmincatalog.md) class represents the catalog itself.</span></span> <span data-ttu-id="44a7f-108">Um objeto criado a partir de **COMAdminCatalog** é o objeto fundamental que você usa na administração programática.</span><span class="sxs-lookup"><span data-stu-id="44a7f-108">An object created from **COMAdminCatalog** is the fundamental object that you use in programmatic administration.</span></span> <span data-ttu-id="44a7f-109">Além de estabelecer a conexão básica com o servidor de catálogo ao instanciá-lo, o **COMAdminCatalog** fornece métodos que permitem que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="44a7f-109">Besides establishing the basic connection with the catalog server when you instantiate it, **COMAdminCatalog** provides methods that enable you to do the following:</span></span>

-   <span data-ttu-id="44a7f-110">Obter coleções no catálogo.</span><span class="sxs-lookup"><span data-stu-id="44a7f-110">Get collections on the catalog.</span></span>
-   <span data-ttu-id="44a7f-111">Conecte-se ao servidor de catálogo em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="44a7f-111">Connect to the catalog server on a remote machine.</span></span>
-   <span data-ttu-id="44a7f-112">Instale, exporte, inicie, desligue e obtenha informações sobre aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="44a7f-112">Install, export, start, shut down, and obtain information regarding COM+ applications.</span></span>
-   <span data-ttu-id="44a7f-113">Instale componentes em aplicativos COM+ e obtenha informações sobre componentes.</span><span class="sxs-lookup"><span data-stu-id="44a7f-113">Install components into COM+ applications and obtain information regarding components.</span></span>
-   <span data-ttu-id="44a7f-114">Iniciar, parar ou atualizar serviços em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="44a7f-114">Start, stop, or refresh services running on the machine.</span></span>
-   <span data-ttu-id="44a7f-115">Atualizar, restaurar ou fazer backup de informações do catálogo.</span><span class="sxs-lookup"><span data-stu-id="44a7f-115">Refresh, restore, or back up catalog information.</span></span>

<span data-ttu-id="44a7f-116">No COM+ 1,0, a classe [**COMAdminCatalog**](comadmincatalog.md) implementa a interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="44a7f-116">In COM+ 1.0, the [**COMAdminCatalog**](comadmincatalog.md) class implements the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span> <span data-ttu-id="44a7f-117">No COM+ 1,5, a classe **COMAdminCatalog** implementa [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) como sua interface padrão.</span><span class="sxs-lookup"><span data-stu-id="44a7f-117">In COM+ 1.5, the **COMAdminCatalog** class implements [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) as its default interface.</span></span>

## <a name="comadmincatalogcollection"></a><span data-ttu-id="44a7f-118">COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="44a7f-118">COMAdminCatalogCollection</span></span>

<span data-ttu-id="44a7f-119">A classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) representa qualquer coleção no catálogo, fornecendo uma cadeia de caracteres que nomeia a coleção específica no tempo de instanciação do objeto.</span><span class="sxs-lookup"><span data-stu-id="44a7f-119">The [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class represents any collection in the catalog, by supplying a string naming the particular collection at object instantiation time.</span></span> <span data-ttu-id="44a7f-120">(As coleções de catálogos disponíveis são nomeadas na tabela em [coleções de administração com+](com--administration-collections.md).) Os objetos são criados dessa classe ao recuperar uma coleção de nível superior chamando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) do objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="44a7f-120">(Available catalog collections are named in the table at [COM+ Administration Collections](com--administration-collections.md).) Objects are created from this class when retrieving a top-level collection by calling the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method of the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="44a7f-121">Esses objetos também são criados ao recuperar uma coleção filho chamando o método **GetCollection** de seu objeto de coleção pai.</span><span class="sxs-lookup"><span data-stu-id="44a7f-121">These objects are also created when retrieving a child collection by calling the **GetCollection** method of its parent collection object.</span></span> <span data-ttu-id="44a7f-122">Os objetos **COMAdminCatalogCollection** permitem que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="44a7f-122">**COMAdminCatalogCollection** objects enable you to do the following:</span></span>

-   <span data-ttu-id="44a7f-123">Enumere os itens contidos na coleção.</span><span class="sxs-lookup"><span data-stu-id="44a7f-123">Enumerate through the items contained within the collection.</span></span>
-   <span data-ttu-id="44a7f-124">Recuperar um item da coleção.</span><span class="sxs-lookup"><span data-stu-id="44a7f-124">Retrieve an item from the collection.</span></span>
-   <span data-ttu-id="44a7f-125">Adicionar ou remover itens da coleção.</span><span class="sxs-lookup"><span data-stu-id="44a7f-125">Add or remove items to or from the collection.</span></span>
-   <span data-ttu-id="44a7f-126">Salve ou descarte as alterações pendentes feitas na coleção ou nos itens que ela contém.</span><span class="sxs-lookup"><span data-stu-id="44a7f-126">Save or discard any pending changes made to the collection or to the items it contains.</span></span>
-   <span data-ttu-id="44a7f-127">Obtenha uma coleção diferente no catálogo.</span><span class="sxs-lookup"><span data-stu-id="44a7f-127">Get a different collection in the catalog.</span></span>

<span data-ttu-id="44a7f-128">A classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa a interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .</span><span class="sxs-lookup"><span data-stu-id="44a7f-128">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface.</span></span>

## <a name="comadmincatalogobject"></a><span data-ttu-id="44a7f-129">COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="44a7f-129">COMAdminCatalogObject</span></span>

<span data-ttu-id="44a7f-130">A classe [**COMAdminCatalogObject**](comadmincatalogobject.md) representa qualquer item contido em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="44a7f-130">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class represents any item that is contained within a collection.</span></span> <span data-ttu-id="44a7f-131">Os objetos são criados dessa classe ao obter um item por meio da propriedade [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) de um objeto de coleção de catálogo.</span><span class="sxs-lookup"><span data-stu-id="44a7f-131">Objects are created from this class when getting an item through the [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) property of a catalog collection object.</span></span> <span data-ttu-id="44a7f-132">Os objetos criados a partir da classe **COMAdminCatalogObject** permitem que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="44a7f-132">Objects created from the **COMAdminCatalogObject** class enable you to do the following:</span></span>

-   <span data-ttu-id="44a7f-133">As propriedades Get ou set com suporte no item que o objeto está sendo usado para representar.</span><span class="sxs-lookup"><span data-stu-id="44a7f-133">Get or set properties supported by the item that the object is being used to represent.</span></span>
-   <span data-ttu-id="44a7f-134">Obtenha informações sobre o item e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="44a7f-134">Obtain information about the item and its properties.</span></span>

<span data-ttu-id="44a7f-135">A classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa a interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="44a7f-135">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44a7f-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44a7f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44a7f-137">Acessando o catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="44a7f-137">Accessing the COM+ Catalog</span></span>](accessing-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="44a7f-138">Visão geral dos objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="44a7f-138">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



