---
description: ICEM05 verifica se o módulo de mesclagem está corretamente associado aos componentes no módulo. A associação incorreta de um componente a um módulo faz com que o componente seja associado incorretamente ao banco de dados de destino.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010908"
---
# <a name="icem05"></a><span data-ttu-id="bc0c9-104">ICEM05</span><span class="sxs-lookup"><span data-stu-id="bc0c9-104">ICEM05</span></span>

<span data-ttu-id="bc0c9-105">ICEM05 verifica se o módulo de mesclagem está corretamente associado aos componentes no módulo.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-105">ICEM05 verifies that the merge module is correctly associated with components in the module.</span></span> <span data-ttu-id="bc0c9-106">A associação incorreta de um componente a um módulo faz com que o componente seja associado incorretamente ao banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-106">Incorrectly associating a component with a module causes the component to be incorrectly associated with the target database.</span></span>

<span data-ttu-id="bc0c9-107">O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="bc0c9-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="bc0c9-108">Result</span></span>

<span data-ttu-id="bc0c9-109">ICEM05 posta um erro se o banco de dados do módulo associa incorretamente componentes e o módulo.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-109">ICEM05 posts an error if the module database incorrectly associates components and the module.</span></span>

## <a name="example"></a><span data-ttu-id="bc0c9-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bc0c9-110">Example</span></span>

<span data-ttu-id="bc0c9-111">ICEM05 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-111">ICEM05 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[<span data-ttu-id="bc0c9-112">Tabela ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="bc0c9-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="bc0c9-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="bc0c9-113">ModuleID</span></span>         | <span data-ttu-id="bc0c9-114">Idioma</span><span class="sxs-lookup"><span data-stu-id="bc0c9-114">Language</span></span> | <span data-ttu-id="bc0c9-115">Versão</span><span class="sxs-lookup"><span data-stu-id="bc0c9-115">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="bc0c9-116">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="bc0c9-116">MyModule.*GUID1*</span></span> | <span data-ttu-id="bc0c9-117">1046</span><span class="sxs-lookup"><span data-stu-id="bc0c9-117">1033</span></span>     | <span data-ttu-id="bc0c9-118">1,0</span><span class="sxs-lookup"><span data-stu-id="bc0c9-118">1.0</span></span>     |



 

[<span data-ttu-id="bc0c9-119">**Tabela ModuleComponents**</span><span class="sxs-lookup"><span data-stu-id="bc0c9-119">**ModuleComponents Table**</span></span>](modulecomponents-table.md)



| <span data-ttu-id="bc0c9-120">Componente</span><span class="sxs-lookup"><span data-stu-id="bc0c9-120">Component</span></span>  | <span data-ttu-id="bc0c9-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="bc0c9-121">ModuleID</span></span>            | <span data-ttu-id="bc0c9-122">Idioma</span><span class="sxs-lookup"><span data-stu-id="bc0c9-122">Language</span></span> |
|------------|---------------------|----------|
| <span data-ttu-id="bc0c9-123">Component1</span><span class="sxs-lookup"><span data-stu-id="bc0c9-123">Component1</span></span> | <span data-ttu-id="bc0c9-124">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="bc0c9-124">MyModule.*GUID1*</span></span>    | <span data-ttu-id="bc0c9-125">1046</span><span class="sxs-lookup"><span data-stu-id="bc0c9-125">1033</span></span>     |
| <span data-ttu-id="bc0c9-126">Component2</span><span class="sxs-lookup"><span data-stu-id="bc0c9-126">Component2</span></span> | <span data-ttu-id="bc0c9-127">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="bc0c9-127">OtherModule.*GUID2*</span></span> | <span data-ttu-id="bc0c9-128">1046</span><span class="sxs-lookup"><span data-stu-id="bc0c9-128">1033</span></span>     |



 

<span data-ttu-id="bc0c9-129">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="bc0c9-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="bc0c9-130">Componente</span><span class="sxs-lookup"><span data-stu-id="bc0c9-130">Component</span></span>  | <span data-ttu-id="bc0c9-131">ComponentID</span><span class="sxs-lookup"><span data-stu-id="bc0c9-131">ComponentID</span></span> |
|------------|-------------|
| <span data-ttu-id="bc0c9-132">Component3</span><span class="sxs-lookup"><span data-stu-id="bc0c9-132">Component3</span></span> | <span data-ttu-id="bc0c9-133">*GUID4*</span><span class="sxs-lookup"><span data-stu-id="bc0c9-133">*GUID4*</span></span>     |
| <span data-ttu-id="bc0c9-134">Component2</span><span class="sxs-lookup"><span data-stu-id="bc0c9-134">Component2</span></span> | <span data-ttu-id="bc0c9-135">*GUID5*</span><span class="sxs-lookup"><span data-stu-id="bc0c9-135">*GUID5*</span></span>     |



 

<span data-ttu-id="bc0c9-136">O ICE do módulo de mesclagem relata o primeiro erro porque a tabela ModuleComponents tenta associar um componente a outro módulo que não é o módulo atual especificado na tabela ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-136">The merge module ICE reports the first error because the ModuleComponents table attempts to associate a component with another module that is not the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="bc0c9-137">Para corrigir isso, altere as colunas ModuleID e Language do registro ModuleComponents para Component2 para o módulo atual, MyModule. *GUID1*.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-137">To fix this, change the ModuleID and Language columns of the ModuleComponents record for Component2 to that for the current module, MyModule.*GUID1*.</span></span>

<span data-ttu-id="bc0c9-138">A ICE do módulo de mesclagem relata o segundo erro porque o primeiro registro na tabela ModuleComponents tenta associar Component1 ao módulo.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-138">The merge module ICE reports the second error because the first record in the ModuleComponents table attempts to associate Component1 with the module.</span></span> <span data-ttu-id="bc0c9-139">Este componente não existe na tabela de componentes do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-139">This component does not exist in the Component Table of the merge module.</span></span> <span data-ttu-id="bc0c9-140">Um módulo só pode ser associado a um componente existente no módulo.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-140">A module can only be associated with a component that exists in the module.</span></span> <span data-ttu-id="bc0c9-141">Para corrigir isso, remova o registro do componente não existente.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-141">To fix this, remove the record for the non-existent component.</span></span>

<span data-ttu-id="bc0c9-142">O ICE do módulo de mesclagem relata o terceiro erro porque o módulo tenta adicionar Component3 ao banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-142">The merge module ICE reports the third error because the module attempts to add Component3 to the target database.</span></span> <span data-ttu-id="bc0c9-143">Este componente não foi associado ao módulo na tabela ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-143">This component has not been associated with the module in the ModuleComponents table.</span></span> <span data-ttu-id="bc0c9-144">Para corrigir esse erro, adicione um registro para Component3 à tabela ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="bc0c9-144">To fix this error, add a record for Component3 to the ModuleComponents table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc0c9-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc0c9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc0c9-146">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="bc0c9-146">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



