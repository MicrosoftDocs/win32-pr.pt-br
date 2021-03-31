---
description: A tabela FeatureComponents define a relação entre recursos e componentes. Para cada recurso, esta tabela lista todos os componentes que compõem esse recurso.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabela FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661563"
---
# <a name="featurecomponents-table"></a><span data-ttu-id="1ef17-104">Tabela FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="1ef17-104">FeatureComponents Table</span></span>

<span data-ttu-id="1ef17-105">A tabela FeatureComponents define a relação entre recursos e componentes.</span><span class="sxs-lookup"><span data-stu-id="1ef17-105">The FeatureComponents table defines the relationship between features and components.</span></span> <span data-ttu-id="1ef17-106">Para cada recurso, esta tabela lista todos os componentes que compõem esse recurso.</span><span class="sxs-lookup"><span data-stu-id="1ef17-106">For each feature, this table lists all the components that make up that feature.</span></span>

<span data-ttu-id="1ef17-107">A tabela FeatureComponents tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ef17-107">The FeatureComponents table has the following columns.</span></span>



| <span data-ttu-id="1ef17-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="1ef17-108">Column</span></span>      | <span data-ttu-id="1ef17-109">Type</span><span class="sxs-lookup"><span data-stu-id="1ef17-109">Type</span></span>                         | <span data-ttu-id="1ef17-110">Chave</span><span class="sxs-lookup"><span data-stu-id="1ef17-110">Key</span></span> | <span data-ttu-id="1ef17-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="1ef17-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="1ef17-112">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="1ef17-112">Feature\_</span></span>   | [<span data-ttu-id="1ef17-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="1ef17-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="1ef17-114">S</span><span class="sxs-lookup"><span data-stu-id="1ef17-114">Y</span></span>   | <span data-ttu-id="1ef17-115">N</span><span class="sxs-lookup"><span data-stu-id="1ef17-115">N</span></span>        |
| <span data-ttu-id="1ef17-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="1ef17-116">Component\_</span></span> | [<span data-ttu-id="1ef17-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="1ef17-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="1ef17-118">S</span><span class="sxs-lookup"><span data-stu-id="1ef17-118">Y</span></span>   | <span data-ttu-id="1ef17-119">N</span><span class="sxs-lookup"><span data-stu-id="1ef17-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1ef17-120">Colunas</span><span class="sxs-lookup"><span data-stu-id="1ef17-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1ef17-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="1ef17-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="1ef17-122">Uma chave externa na primeira coluna da [tabela](feature-table.md)de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ef17-122">An external key into the first column of the Feature [table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ef17-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="1ef17-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="1ef17-124">Uma chave externa na primeira coluna da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ef17-124">An external key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ef17-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ef17-125">Remarks</span></span>

<span data-ttu-id="1ef17-126">Há um limite máximo de 1600 componentes por recurso.</span><span class="sxs-lookup"><span data-stu-id="1ef17-126">There is a maximum limit of 1600 components per feature.</span></span>

<span data-ttu-id="1ef17-127">Os componentes podem ser compartilhados por dois ou mais recursos, ou seja, o mesmo componente pode ser referenciado por mais de um recurso.</span><span class="sxs-lookup"><span data-stu-id="1ef17-127">Components can be shared by two or more features, that is, the same component can be referred to by more than one feature.</span></span>

<span data-ttu-id="1ef17-128">Essa tabela é referida quando a ação [PublishFeatures](publishfeatures-action.md) ou a [ação UnpublishFeatures](unpublishfeatures-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="1ef17-128">This table is referred to when the [PublishFeatures action](publishfeatures-action.md) or the [UnpublishFeatures action](unpublishfeatures-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="1ef17-129">Validação</span><span class="sxs-lookup"><span data-stu-id="1ef17-129">Validation</span></span>

<dl>

[<span data-ttu-id="1ef17-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="1ef17-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1ef17-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="1ef17-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1ef17-132">ICE21</span><span class="sxs-lookup"><span data-stu-id="1ef17-132">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="1ef17-133">ICE22</span><span class="sxs-lookup"><span data-stu-id="1ef17-133">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="1ef17-134">ICE32</span><span class="sxs-lookup"><span data-stu-id="1ef17-134">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="1ef17-135">ICE41</span><span class="sxs-lookup"><span data-stu-id="1ef17-135">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="1ef17-136">ICE47</span><span class="sxs-lookup"><span data-stu-id="1ef17-136">ICE47</span></span>](ice47.md)  
[<span data-ttu-id="1ef17-137">ICE59</span><span class="sxs-lookup"><span data-stu-id="1ef17-137">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="1ef17-138">ICE62</span><span class="sxs-lookup"><span data-stu-id="1ef17-138">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="1ef17-139">ICE69</span><span class="sxs-lookup"><span data-stu-id="1ef17-139">ICE69</span></span>](ice69.md)  
</dl>

 

 



