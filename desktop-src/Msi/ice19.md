---
description: O ICE19 valida que os componentes anunciados fazem referência a um arquivo na coluna KeyPath da tabela de componentes e que um atalho anunciado faz referência a um diretório nesta coluna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170233"
---
# <a name="ice19"></a><span data-ttu-id="71e1b-103">ICE19</span><span class="sxs-lookup"><span data-stu-id="71e1b-103">ICE19</span></span>

<span data-ttu-id="71e1b-104">O ICE19 valida que os componentes anunciados fazem referência a um arquivo na coluna KeyPath da [tabela de componentes](component-table.md) e que um atalho anunciado faz referência a um diretório nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="71e1b-104">ICE19 validates that advertised components reference a file in the KeyPath column of the [Component table](component-table.md) and that an advertised shortcut references a directory in this column.</span></span>

<span data-ttu-id="71e1b-105">ICE19 valida que os componentes ou atalhos anunciados têm um ComponentID.</span><span class="sxs-lookup"><span data-stu-id="71e1b-105">ICE19 validates that advertised components or shortcuts have a ComponentId.</span></span> <span data-ttu-id="71e1b-106">Os componentes na [tabela PublishComponent](publishcomponent-table.md), que não são anunciados em outra tabela, só são verificados para ver se eles têm um ComponentID.</span><span class="sxs-lookup"><span data-stu-id="71e1b-106">Components in the [PublishComponent table](publishcomponent-table.md), which are not advertised in another table, are only checked to see whether they have a ComponentId.</span></span>

## <a name="result"></a><span data-ttu-id="71e1b-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="71e1b-107">Result</span></span>

<span data-ttu-id="71e1b-108">ICE19 posta uma mensagem de erro se a coluna KeyPath da tabela Component não faz referência a um arquivo no caso de um componente anunciado ou um diretório no caso de um atalho anunciado.</span><span class="sxs-lookup"><span data-stu-id="71e1b-108">ICE19 posts an error message if the KeyPath column of the Component table does not reference a file in the case of an advertised component or a directory in the case of an advertised shortcut.</span></span> <span data-ttu-id="71e1b-109">ICE19 posta uma mensagem de erro se algum componente ou atalho anunciado não tiver um ComponentID.</span><span class="sxs-lookup"><span data-stu-id="71e1b-109">ICE19 posts an error message if any advertised components or shortcuts do not have a ComponentId.</span></span>

## <a name="example"></a><span data-ttu-id="71e1b-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="71e1b-110">Example</span></span>

<span data-ttu-id="71e1b-111">ICE19 posta as seguintes mensagens de erro para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="71e1b-111">ICE19 posts the following error messages for the example shown:</span></span>

-   <span data-ttu-id="71e1b-112">A extensão FLP faz referência ao componente comp1 que não tem um ComponentID especificado na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="71e1b-112">Extension flp references the component Comp1 which does not have a ComponentId specified in the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="71e1b-113">A extensão exe faz referência ao componente Comp4 que faz referência a um diretório como seu caminho KeyPath.</span><span class="sxs-lookup"><span data-stu-id="71e1b-113">Extension exe references the component Comp4 which references a directory as its KeyPath.</span></span> <span data-ttu-id="71e1b-114">O caminho keyé nulo na tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="71e1b-114">The KeyPath is Null in the Component table.</span></span>
-   <span data-ttu-id="71e1b-115">O atalho Shortcut2 faz referência ao componente Comp3 que faz referência a uma entrada do registro como o caminho da chave.</span><span class="sxs-lookup"><span data-stu-id="71e1b-115">Shortcut Shortcut2 references the component Comp3 which references a Registry entry as the key path.</span></span> <span data-ttu-id="71e1b-116">O valor da coluna atributos na tabela de componentes é 4.</span><span class="sxs-lookup"><span data-stu-id="71e1b-116">The value of the Attributes column in the Component table is 4.</span></span>

<span data-ttu-id="71e1b-117">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="71e1b-117">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="71e1b-118">Componente</span><span class="sxs-lookup"><span data-stu-id="71e1b-118">Component</span></span> | <span data-ttu-id="71e1b-119">ComponentId</span><span class="sxs-lookup"><span data-stu-id="71e1b-119">ComponentId</span></span>                            | <span data-ttu-id="71e1b-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="71e1b-120">Attributes</span></span> | <span data-ttu-id="71e1b-121">KeyPath</span><span class="sxs-lookup"><span data-stu-id="71e1b-121">KeyPath</span></span> |
|-----------|----------------------------------------|------------|---------|
| <span data-ttu-id="71e1b-122">Comp1</span><span class="sxs-lookup"><span data-stu-id="71e1b-122">Comp1</span></span>     | <span data-ttu-id="71e1b-123">Nulo</span><span class="sxs-lookup"><span data-stu-id="71e1b-123">Null</span></span>                                   | <span data-ttu-id="71e1b-124">0</span><span class="sxs-lookup"><span data-stu-id="71e1b-124">0</span></span>          | <span data-ttu-id="71e1b-125">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="71e1b-125">File1</span></span>   |
| <span data-ttu-id="71e1b-126">Comp2</span><span class="sxs-lookup"><span data-stu-id="71e1b-126">Comp2</span></span>     | {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="71e1b-127">0</span><span class="sxs-lookup"><span data-stu-id="71e1b-127">0</span></span>          | <span data-ttu-id="71e1b-128">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="71e1b-128">File2</span></span>   |
| <span data-ttu-id="71e1b-129">Comp3</span><span class="sxs-lookup"><span data-stu-id="71e1b-129">Comp3</span></span>     | {00000003-0003-0000-0000-624474736554} | <span data-ttu-id="71e1b-130">4</span><span class="sxs-lookup"><span data-stu-id="71e1b-130">4</span></span>          | <span data-ttu-id="71e1b-131">Reg3</span><span class="sxs-lookup"><span data-stu-id="71e1b-131">Reg3</span></span>    |
| <span data-ttu-id="71e1b-132">Comp4</span><span class="sxs-lookup"><span data-stu-id="71e1b-132">Comp4</span></span>     | {00000004-0003-0000-0000-624474736554} | <span data-ttu-id="71e1b-133">0</span><span class="sxs-lookup"><span data-stu-id="71e1b-133">0</span></span>          | <span data-ttu-id="71e1b-134">Nulo</span><span class="sxs-lookup"><span data-stu-id="71e1b-134">Null</span></span>    |



 

<span data-ttu-id="71e1b-135">[Tabela de extensão](extension-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="71e1b-135">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="71e1b-136">Extensão</span><span class="sxs-lookup"><span data-stu-id="71e1b-136">Extension</span></span> | <span data-ttu-id="71e1b-137">Componente\_</span><span class="sxs-lookup"><span data-stu-id="71e1b-137">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="71e1b-138">FLP</span><span class="sxs-lookup"><span data-stu-id="71e1b-138">flp</span></span>       | <span data-ttu-id="71e1b-139">Comp1</span><span class="sxs-lookup"><span data-stu-id="71e1b-139">Comp1</span></span>       |
| <span data-ttu-id="71e1b-140">TST</span><span class="sxs-lookup"><span data-stu-id="71e1b-140">tst</span></span>       | <span data-ttu-id="71e1b-141">Comp2</span><span class="sxs-lookup"><span data-stu-id="71e1b-141">Comp2</span></span>       |
| <span data-ttu-id="71e1b-142">exe</span><span class="sxs-lookup"><span data-stu-id="71e1b-142">exe</span></span>       | <span data-ttu-id="71e1b-143">Comp4</span><span class="sxs-lookup"><span data-stu-id="71e1b-143">Comp4</span></span>       |



 

<span data-ttu-id="71e1b-144">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="71e1b-144">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="71e1b-145">Atalho</span><span class="sxs-lookup"><span data-stu-id="71e1b-145">Shortcut</span></span>  | <span data-ttu-id="71e1b-146">Componente\_</span><span class="sxs-lookup"><span data-stu-id="71e1b-146">Component\_</span></span> | <span data-ttu-id="71e1b-147">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="71e1b-147">Feature\_</span></span>      |
|-----------|-------------|----------------|
| <span data-ttu-id="71e1b-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="71e1b-148">Shortcut1</span></span> | <span data-ttu-id="71e1b-149">Comp4</span><span class="sxs-lookup"><span data-stu-id="71e1b-149">Comp4</span></span>       | <span data-ttu-id="71e1b-150">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="71e1b-150">ProductFeature</span></span> |
| <span data-ttu-id="71e1b-151">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="71e1b-151">Shortcut2</span></span> | <span data-ttu-id="71e1b-152">Comp3</span><span class="sxs-lookup"><span data-stu-id="71e1b-152">Comp3</span></span>       | <span data-ttu-id="71e1b-153">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="71e1b-153">ProductFeature</span></span> |



 

<span data-ttu-id="71e1b-154">[Tabela de recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="71e1b-154">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="71e1b-155">Recurso</span><span class="sxs-lookup"><span data-stu-id="71e1b-155">Feature</span></span>        |
|----------------|
| <span data-ttu-id="71e1b-156">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="71e1b-156">ProductFeature</span></span> |



 

> [!Note]  
> <span data-ttu-id="71e1b-157">Se a extensão FLP e o exe referenciarem o mesmo componente, o EXE ou o servidor COM que os abre deve ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="71e1b-157">If the extension flp and exe both reference the same component, the EXE or COM server that opens them must be the same.</span></span> <span data-ttu-id="71e1b-158">Esse EXE é normalmente o caminho Keypara o componente.</span><span class="sxs-lookup"><span data-stu-id="71e1b-158">This EXE is normally the KeyPath for the Component.</span></span> <span data-ttu-id="71e1b-159">Para o OFFICE, as extensões doc e XLS não podem referenciar o mesmo componente porque o mesmo EXE não abre ambas as extensões.</span><span class="sxs-lookup"><span data-stu-id="71e1b-159">For OFFICE, the extensions doc and xls cannot reference the same component because the same EXE does not open both extensions.</span></span> <span data-ttu-id="71e1b-160">Você precisa winword.exe para abrir as extensões de documento e precisa excel.exe abrir as extensões xls.</span><span class="sxs-lookup"><span data-stu-id="71e1b-160">You need winword.exe to open doc extensions and you need excel.exe to open xls extensions.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="71e1b-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71e1b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71e1b-162">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="71e1b-162">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



