---
description: Obtendo e definindo propriedades
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Obtendo e definindo propriedades (serviços de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457056"
---
# <a name="getting-and-setting-properties-component-services"></a><span data-ttu-id="f1c27-103">Obtendo e definindo propriedades (serviços de componentes)</span><span class="sxs-lookup"><span data-stu-id="f1c27-103">Getting and Setting Properties (Component Services)</span></span>

<span data-ttu-id="f1c27-104">Antes de ler ou gravar propriedades específicas expostas por um item em uma coleção, você deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="f1c27-104">Before you can read or write particular properties exposed by an item in a collection, you must take the following steps:</span></span>

1.  <span data-ttu-id="f1c27-105">Recupere a coleção.</span><span class="sxs-lookup"><span data-stu-id="f1c27-105">Retrieve the collection.</span></span>
2.  <span data-ttu-id="f1c27-106">Preencha a coleção para ler os dados do catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="f1c27-106">Populate the collection to read in data for it from the COM+ catalog.</span></span>
3.  <span data-ttu-id="f1c27-107">Recupere o item específico na coleção, representando-o com um objeto da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c27-107">Retrieve the specific item in the collection, representing it with an object from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="f1c27-108">Para obter um exemplo que ilustra essas etapas, consulte [navegando na hierarquia da coleção com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="f1c27-108">For an example that illustrates these steps, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="f1c27-109">Porque as propriedades específicas expostas podem variar dependendo do que o item representa; ou seja, um item que representa um componente tem propriedades diferentes de um que representa um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="f1c27-109">Because the particular properties exposed can vary depending on what the item represents; that is, an item representing a component has different properties than one representing a COM+ application.</span></span> <span data-ttu-id="f1c27-110">Defina qualquer uma dessas propriedades usando uma única propriedade genérica, a propriedade Value, em [**COMAdminCatalogObject**](comadmincatalogobject.md).</span><span class="sxs-lookup"><span data-stu-id="f1c27-110">Set any of these properties using a single generic property, the Value property, on [**COMAdminCatalogObject**](comadmincatalogobject.md).</span></span>

<span data-ttu-id="f1c27-111">A propriedade Value permite que você obtenha ou defina qualquer propriedade nomeada específica exposta por um item, retornando um valor para uma propriedade nomeada ao obter e tomando um nome e um valor ao definir.</span><span class="sxs-lookup"><span data-stu-id="f1c27-111">The Value property enables you to get or set any specific named property exposed by an item, returning a value for a named property when getting, and taking a name and value when setting.</span></span>

<span data-ttu-id="f1c27-112">No entanto, nenhuma alteração é registrada no catálogo COM+ até que você salve explicitamente as alterações usando o método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c27-112">No changes are actually recorded to the COM+ catalog until you explicitly save changes using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="f1c27-113">As alterações pendentes para todas as propriedades em todos os itens em uma determinada coleção são salvas de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="f1c27-113">Pending changes for all properties on all items in a given collection are saved all at once.</span></span> <span data-ttu-id="f1c27-114">Para obter detalhes, consulte [salvando ou descartando alterações](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="f1c27-114">For details, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="f1c27-115">Nem todas as alterações feitas serão aceitas.</span><span class="sxs-lookup"><span data-stu-id="f1c27-115">Not all changes that you make will be accepted.</span></span> <span data-ttu-id="f1c27-116">O catálogo COM+ impõe alguma lógica de coerência para garantir que você configure as coisas de forma razoável.</span><span class="sxs-lookup"><span data-stu-id="f1c27-116">The COM+ catalog enforces some coherency logic to ensure that you configure things in a reasonable way.</span></span> <span data-ttu-id="f1c27-117">Além disso, quando você altera algumas propriedades, outras podem ser alteradas automaticamente pela mesma lógica de coerência.</span><span class="sxs-lookup"><span data-stu-id="f1c27-117">Additionally, when you change some properties, others might change automatically by the same coherency logic.</span></span> <span data-ttu-id="f1c27-118">Esses efeitos aparecem quando você tenta salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="f1c27-118">These effects show up when you attempt to save changes.</span></span>

> [!Note]  
> <span data-ttu-id="f1c27-119">É possível que você esteja em contenção com outro gravador no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="f1c27-119">It is possible for you to be in contention with another writer to the COM+ catalog.</span></span> <span data-ttu-id="f1c27-120">Entre as chamadas para [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para uma determinada coleção, você não tem um bloqueio em nenhum desses dados no catálogo.</span><span class="sxs-lookup"><span data-stu-id="f1c27-120">Between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) for a given collection, you do not have a lock on any of that data in the catalog.</span></span> <span data-ttu-id="f1c27-121">Várias partes podem estar simultaneamente Configurando itens em uma determinada coleção e podem ser contendedas quando salvam alterações.</span><span class="sxs-lookup"><span data-stu-id="f1c27-121">Multiple parties may simultaneously be configuring items in a given collection and could be contending when they save changes.</span></span> <span data-ttu-id="f1c27-122">Isso significa que outra pessoa pode alterar as configurações de um objeto antes ou depois de fazer isso, executando algum tipo de programa usando os objetos COMAdmin ou usando a ferramenta administrativa serviços de componentes, seja local ou remotamente.</span><span class="sxs-lookup"><span data-stu-id="f1c27-122">This means that someone else might change settings on an object before or after you do, either running some kind of program using the COMAdmin objects or using the Component Services administrative tool, either locally or remotely.</span></span> <span data-ttu-id="f1c27-123">A regra geral com a gravação de objetos no catálogo é que todas as propriedades em um objeto são gravadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="f1c27-123">The general rule with writing objects on the catalog is that all properties on an object are written at once.</span></span> <span data-ttu-id="f1c27-124">Ou seja, o último gravador vence — o objeto é salvo no catálogo precisamente como o último gravador o configurou.</span><span class="sxs-lookup"><span data-stu-id="f1c27-124">That is, the last writer wins—the object is saved in the catalog precisely as the last writer configured it.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f1c27-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1c27-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c27-126">Interdependências entre propriedades</span><span class="sxs-lookup"><span data-stu-id="f1c27-126">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="f1c27-127">Consultando as propriedades disponíveis</span><span class="sxs-lookup"><span data-stu-id="f1c27-127">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="f1c27-128">Salvando ou descartando alterações</span><span class="sxs-lookup"><span data-stu-id="f1c27-128">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



