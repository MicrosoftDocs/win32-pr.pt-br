---
description: ICE41 valida que as entradas nas tabelas de classe e extensão se referem a entradas na tabela de componentes que implementam o objeto de classe ou a extensão do componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748777"
---
# <a name="ice41"></a><span data-ttu-id="46d5b-103">ICE41</span><span class="sxs-lookup"><span data-stu-id="46d5b-103">ICE41</span></span>

<span data-ttu-id="46d5b-104">ICE41 valida que as entradas nas tabelas de [classe](class-table.md) e [extensão](extension-table.md) se referem a entradas na [tabela de componentes](component-table.md) que implementam o objeto de classe ou a extensão do componente.</span><span class="sxs-lookup"><span data-stu-id="46d5b-104">ICE41 validates that the entries in the [Class](class-table.md) and [Extension](extension-table.md) tables refer to entries in the [Component table](component-table.md) that implement the class object or extension of the component.</span></span>

## <a name="result"></a><span data-ttu-id="46d5b-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="46d5b-105">Result</span></span>

<span data-ttu-id="46d5b-106">ICE41 posta um erro se houver um recurso que não contém o componente que implementa a extensão ou o objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="46d5b-106">ICE41 posts an error if there is a feature that does not contain the component implementing the class object or extension.</span></span>

## <a name="example"></a><span data-ttu-id="46d5b-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="46d5b-107">Example</span></span>

<span data-ttu-id="46d5b-108">ICE41 relata os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="46d5b-108">ICE41 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="46d5b-109">Erro de ICE41</span><span class="sxs-lookup"><span data-stu-id="46d5b-109">ICE41 error</span></span>                                                                                                                                                                                    | <span data-ttu-id="46d5b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="46d5b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d5b-111">{00000000-0000-0000-0000-0000000000000}A classe referencia o recurso Feature2 e o componente Component1, mas o componente não está associado a esse recurso na tabela FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="46d5b-111">Class {00000000-0000-0000-0000-0000000000000} references feature Feature2 and component Component1, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span> | <span data-ttu-id="46d5b-112">Há um recurso que não contém o componente que implementa o objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="46d5b-112">There is a feature that does not contain the component implementing the class object.</span></span> <span data-ttu-id="46d5b-113">Isso significa que o instalador não instala o componente com o recurso e que o anúncio pode não funcionar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="46d5b-113">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="46d5b-114">Para corrigir esse erro, altere a entrada na coluna recurso \_ da entrada da [tabela de classes](class-table.md) para fazer referência a um recurso que instala o componente listado na \_ coluna componente ou altere o recurso e o componente associados na [tabela FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="46d5b-114">To fix this error, change the entry in the Feature\_ column of the [Class table](class-table.md) entry to reference a feature that installs component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/>          |
| <span data-ttu-id="46d5b-115">A extensão. Yip referencia o recurso Feature1 e o componente Component2, mas o componente não está associado a esse recurso na tabela FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="46d5b-115">Extension .yip references feature Feature1 and component Component2, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span>                                | <span data-ttu-id="46d5b-116">Há um recurso que não contém o componente que implementa a extensão.</span><span class="sxs-lookup"><span data-stu-id="46d5b-116">There is a feature that does not contain the component implementing the extension.</span></span> <span data-ttu-id="46d5b-117">Isso significa que o instalador não instala o componente com o recurso e que o anúncio pode não funcionar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="46d5b-117">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="46d5b-118">Para corrigir esse erro, altere a entrada na coluna recurso \_ da entrada da [tabela de extensão](extension-table.md) para fazer referência a um recurso que instala o componente listado na \_ coluna componente ou altere o recurso e o componente associados na [tabela FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="46d5b-118">To fix this error, change the entry in the Feature\_ column of the [Extension table](extension-table.md) entry to reference a feature that installs the component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/> |



 

<span data-ttu-id="46d5b-119">[Tabela FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="46d5b-119">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="46d5b-120">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="46d5b-120">Feature\_</span></span> |
|-----------|
| <span data-ttu-id="46d5b-121">Feature1</span><span class="sxs-lookup"><span data-stu-id="46d5b-121">Feature1</span></span>  |
| <span data-ttu-id="46d5b-122">Feature2</span><span class="sxs-lookup"><span data-stu-id="46d5b-122">Feature2</span></span>  |



 

<span data-ttu-id="46d5b-123">[Tabela de classes](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="46d5b-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="46d5b-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="46d5b-124">CLSID</span></span>                                  | <span data-ttu-id="46d5b-125">Componente\_</span><span class="sxs-lookup"><span data-stu-id="46d5b-125">Component\_</span></span> | <span data-ttu-id="46d5b-126">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="46d5b-126">Feature\_</span></span> |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | <span data-ttu-id="46d5b-127">Component1</span><span class="sxs-lookup"><span data-stu-id="46d5b-127">Component1</span></span>  | <span data-ttu-id="46d5b-128">Feature2</span><span class="sxs-lookup"><span data-stu-id="46d5b-128">Feature2</span></span>  |



 

<span data-ttu-id="46d5b-129">[Tabela de classes](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="46d5b-129">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="46d5b-130">Extensão</span><span class="sxs-lookup"><span data-stu-id="46d5b-130">Extension</span></span> | <span data-ttu-id="46d5b-131">Componente\_</span><span class="sxs-lookup"><span data-stu-id="46d5b-131">Component\_</span></span> | <span data-ttu-id="46d5b-132">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="46d5b-132">Feature\_</span></span> |
|-----------|-------------|-----------|
| <span data-ttu-id="46d5b-133">.yip</span><span class="sxs-lookup"><span data-stu-id="46d5b-133">.yip</span></span>      | <span data-ttu-id="46d5b-134">Component2</span><span class="sxs-lookup"><span data-stu-id="46d5b-134">Component2</span></span>  | <span data-ttu-id="46d5b-135">Feature1</span><span class="sxs-lookup"><span data-stu-id="46d5b-135">Feature1</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="46d5b-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46d5b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46d5b-137">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="46d5b-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




