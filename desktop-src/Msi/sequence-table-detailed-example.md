---
description: Aqui está um exemplo de uma tabela de sequência.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Exemplo detalhado da tabela de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756717"
---
# <a name="sequence-table-detailed-example"></a><span data-ttu-id="8c941-103">Exemplo detalhado da tabela de sequência</span><span class="sxs-lookup"><span data-stu-id="8c941-103">Sequence Table Detailed Example</span></span>

<span data-ttu-id="8c941-104">Aqui está um exemplo de uma tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="8c941-104">Here is an example of a sequence table.</span></span>



| <span data-ttu-id="8c941-105">Ação</span><span class="sxs-lookup"><span data-stu-id="8c941-105">Action</span></span>                                          | <span data-ttu-id="8c941-106">Condição</span><span class="sxs-lookup"><span data-stu-id="8c941-106">Condition</span></span>                                                       | <span data-ttu-id="8c941-107">Sequência</span><span class="sxs-lookup"><span data-stu-id="8c941-107">Sequence</span></span> |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [<span data-ttu-id="8c941-108">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="8c941-108">LaunchConditions</span></span>](launchconditions-action.md) |                                                                 |          |
| [<span data-ttu-id="8c941-109">AppSearch</span><span class="sxs-lookup"><span data-stu-id="8c941-109">AppSearch</span></span>](appsearch-action.md)               |                                                                 | <span data-ttu-id="8c941-110">200</span><span class="sxs-lookup"><span data-stu-id="8c941-110">200</span></span>      |
| [<span data-ttu-id="8c941-111">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="8c941-111">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="8c941-112">teste do CCP \_</span><span class="sxs-lookup"><span data-stu-id="8c941-112">CCP\_TEST</span></span>                                                       | <span data-ttu-id="8c941-113">300</span><span class="sxs-lookup"><span data-stu-id="8c941-113">300</span></span>      |
| <span data-ttu-id="8c941-114">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-114">CCPDialog</span></span>                                       | <span data-ttu-id="8c941-115">Não \_ êxito de CCP \_</span><span class="sxs-lookup"><span data-stu-id="8c941-115">NOT\_CCP\_SUCCESS</span></span>                                               | <span data-ttu-id="8c941-116">400</span><span class="sxs-lookup"><span data-stu-id="8c941-116">400</span></span>      |
| <span data-ttu-id="8c941-117">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="8c941-117">MyCustomConfig</span></span>                                  | <span data-ttu-id="8c941-118">Não [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="8c941-118">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="8c941-119">500</span><span class="sxs-lookup"><span data-stu-id="8c941-119">500</span></span>      |
| [<span data-ttu-id="8c941-120">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="8c941-120">CostInitialize</span></span>](costinitialize-action.md)     |                                                                 | <span data-ttu-id="8c941-121">600</span><span class="sxs-lookup"><span data-stu-id="8c941-121">600</span></span>      |
| [<span data-ttu-id="8c941-122">Custo de</span><span class="sxs-lookup"><span data-stu-id="8c941-122">FileCost</span></span>](filecost-action.md)                 |                                                                 | <span data-ttu-id="8c941-123">700</span><span class="sxs-lookup"><span data-stu-id="8c941-123">700</span></span>      |
| [<span data-ttu-id="8c941-124">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="8c941-124">CostFinalize</span></span>](costfinalize-action.md)         |                                                                 | <span data-ttu-id="8c941-125">800</span><span class="sxs-lookup"><span data-stu-id="8c941-125">800</span></span>      |
| <span data-ttu-id="8c941-126">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-126">InstallDialog</span></span>                                   | <span data-ttu-id="8c941-127">Não [ **instalado**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="8c941-127">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="8c941-128">900</span><span class="sxs-lookup"><span data-stu-id="8c941-128">900</span></span>      |
| <span data-ttu-id="8c941-129">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-129">MaintenanceDialog</span></span>                               | <span data-ttu-id="8c941-130">[**Instalado**](installed.md) E não [ **retomar**](resume.md)</span><span class="sxs-lookup"><span data-stu-id="8c941-130">[**Installed**](installed.md) AND NOT [**Resume**](resume.md)</span></span> | <span data-ttu-id="8c941-131">1000</span><span class="sxs-lookup"><span data-stu-id="8c941-131">1000</span></span>     |
| <span data-ttu-id="8c941-132">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-132">ActionDialog</span></span>                                    |                                                                 | <span data-ttu-id="8c941-133">1100</span><span class="sxs-lookup"><span data-stu-id="8c941-133">1100</span></span>     |
| [<span data-ttu-id="8c941-134">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="8c941-134">RegisterProduct</span></span>](registerproduct-action.md)   |                                                                 | <span data-ttu-id="8c941-135">1200</span><span class="sxs-lookup"><span data-stu-id="8c941-135">1200</span></span>     |
| [<span data-ttu-id="8c941-136">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="8c941-136">InstallValidate</span></span>](installvalidate-action.md)   |                                                                 | <span data-ttu-id="8c941-137">1300</span><span class="sxs-lookup"><span data-stu-id="8c941-137">1300</span></span>     |
| [<span data-ttu-id="8c941-138">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="8c941-138">InstallFiles</span></span>](installfiles-action.md)         |                                                                 | <span data-ttu-id="8c941-139">1.400</span><span class="sxs-lookup"><span data-stu-id="8c941-139">1400</span></span>     |
| <span data-ttu-id="8c941-140">Mycustomizable</span><span class="sxs-lookup"><span data-stu-id="8c941-140">MyCustomAction</span></span>                                  | <span data-ttu-id="8c941-141">$MyComponent > 2</span><span class="sxs-lookup"><span data-stu-id="8c941-141">$MyComponent > 2</span></span>                                             | <span data-ttu-id="8c941-142">1500</span><span class="sxs-lookup"><span data-stu-id="8c941-142">1500</span></span>     |
| [<span data-ttu-id="8c941-143">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="8c941-143">InstallFinalize</span></span>](installfinalize-action.md)   |                                                                 | <span data-ttu-id="8c941-144">1600</span><span class="sxs-lookup"><span data-stu-id="8c941-144">1600</span></span>     |



 

<span data-ttu-id="8c941-145">As seguintes ações nessa tabela de sequência são definidas pelo instalador e são exemplos de ações padrão:</span><span class="sxs-lookup"><span data-stu-id="8c941-145">The following actions in this sequence table are defined by the installer and are examples of standard actions:</span></span>

[<span data-ttu-id="8c941-146">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="8c941-146">LaunchConditions</span></span>](launchconditions-action.md)

 

[<span data-ttu-id="8c941-147">AppSearch</span><span class="sxs-lookup"><span data-stu-id="8c941-147">AppSearch</span></span>](appsearch-action.md)

 

[<span data-ttu-id="8c941-148">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="8c941-148">CCPSearch</span></span>](ccpsearch-action.md)

 

[<span data-ttu-id="8c941-149">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="8c941-149">CostInitialize</span></span>](costinitialize-action.md)

 

[<span data-ttu-id="8c941-150">Custo de</span><span class="sxs-lookup"><span data-stu-id="8c941-150">FileCost</span></span>](filecost-action.md)

 

[<span data-ttu-id="8c941-151">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="8c941-151">CostFinalize</span></span>](costfinalize-action.md)

 

[<span data-ttu-id="8c941-152">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="8c941-152">RegisterProduct</span></span>](registerproduct-action.md)

 

[<span data-ttu-id="8c941-153">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="8c941-153">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="8c941-154">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="8c941-154">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="8c941-155">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="8c941-155">InstallValidate</span></span>](installvalidate-action.md)

<span data-ttu-id="8c941-156">As ações a seguir foram definidas pelo autor da tabela e são exemplos de [ações personalizadas](custom-actions.md) e devem ser listadas na [tabela CustomAction](customaction-table.md):</span><span class="sxs-lookup"><span data-stu-id="8c941-156">The following actions were defined by the table's author and are examples of [custom actions](custom-actions.md) and must be listed in the [CustomAction table](customaction-table.md):</span></span>

<span data-ttu-id="8c941-157">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="8c941-157">MyCustomConfig</span></span>

 

<span data-ttu-id="8c941-158">Mycustomizable</span><span class="sxs-lookup"><span data-stu-id="8c941-158">MyCustomAction</span></span>

<span data-ttu-id="8c941-159">As entradas restantes no campo de ação são chaves estrangeiras na [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c941-159">The remaining entries in the Action field are foreign keys into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="8c941-160">Eles especificam os nomes das caixas de diálogo que serão exibidas se o campo condição for avaliado como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="8c941-160">They specify the names of dialog boxes that will displayed if the condition field evaluates to True.</span></span>

<span data-ttu-id="8c941-161">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-161">CCPDialog</span></span>

 

<span data-ttu-id="8c941-162">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-162">InstallDialog</span></span>

 

<span data-ttu-id="8c941-163">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-163">MaintenanceDialog</span></span>

 

<span data-ttu-id="8c941-164">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="8c941-164">ActionDialog</span></span>

<span data-ttu-id="8c941-165">A coluna condição faz com que o instalador ignore a ação se a propriedade ou expressão nesse campo for false.</span><span class="sxs-lookup"><span data-stu-id="8c941-165">The Condition column causes the installer to skip the action if the property or expression in this field is False.</span></span> <span data-ttu-id="8c941-166">A propriedade [**installed**](installed.md) e a propriedade [**resume**](resume.md) são exemplos de propriedades que são definidas pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="8c941-166">The [**Installed**](installed.md) property and the [**RESUME**](resume.md) property are example of properties that are set by the installer.</span></span> <span data-ttu-id="8c941-167">A propriedade [**installed**](installed.md) será definida como true se o produto já estiver instalado e a propriedade [**resume**](resume.md) for definida se o retomar uma instalação suspensa.</span><span class="sxs-lookup"><span data-stu-id="8c941-167">The [**Installed**](installed.md) property is set to true if the product is already installed and the [**RESUME**](resume.md) property is set if resuming a suspended installation.</span></span> <span data-ttu-id="8c941-168">O teste do CCP \_ e as \_ Propriedades de êxito not CCP \_ são exemplos de propriedades que podem ser definidas na linha de comando pelo usuário que está instalando o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c941-168">The CCP\_TEST and the NOT\_CCP\_SUCCESS properties are examples of properties that can be set at the command line by the user installing the application.</span></span>

<span data-ttu-id="8c941-169">Todas as ações são executadas em sequência com as seguintes etapas condicionais:</span><span class="sxs-lookup"><span data-stu-id="8c941-169">All actions run in sequence with the following conditional steps:</span></span>

-   <span data-ttu-id="8c941-170">O CPPSearch será executado somente se o \_ teste do CCP estiver definido.</span><span class="sxs-lookup"><span data-stu-id="8c941-170">The CPPSearch is run only if CCP\_TEST is set.</span></span>
-   <span data-ttu-id="8c941-171">CCPDialog será executado somente se o \_ êxito de CCP não \_ for definido.</span><span class="sxs-lookup"><span data-stu-id="8c941-171">CCPDialog is run only if NOT\_CCP\_SUCCESS is set.</span></span>
-   <span data-ttu-id="8c941-172">MaintenanceDialog será executado somente se este produto já estiver instalado e se não for uma instalação que está sendo retomada após ser suspensa.</span><span class="sxs-lookup"><span data-stu-id="8c941-172">MaintenanceDialog is run only if this product is already installed and if this is not an installation that is being resume after being suspended.</span></span>
-   <span data-ttu-id="8c941-173">MyCustomAction será executado somente se a expressão na coluna Condition for true.</span><span class="sxs-lookup"><span data-stu-id="8c941-173">MyCustomAction is run only if the expression in the Condition column is True.</span></span> <span data-ttu-id="8c941-174">A expressão $MyComponent > 2 refere-se ao estado de ação do componente chamado myComponent.</span><span class="sxs-lookup"><span data-stu-id="8c941-174">The expression $MyComponent > 2 refers to the action state of the component called MyComponent.</span></span> <span data-ttu-id="8c941-175">Essa condição indica que mycustomizable deve ser executada somente se myComponent estiver definido para ser instalado.</span><span class="sxs-lookup"><span data-stu-id="8c941-175">This condition indicates that MyCustomAction should only be run if MyComponent is set to be installed.</span></span> <span data-ttu-id="8c941-176">Para obter mais informações sobre Estados de ação e Estados de seleção, consulte a propriedade [**FeatureRequestState**](session-featurerequeststate.md) , a [tabela de recursos](feature-table.md)e a [ação InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="8c941-176">For more information on Action states and Selection states, see the [**FeatureRequestState**](session-featurerequeststate.md) property, the [Feature table](feature-table.md), and the [InstallFiles action](installfiles-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c941-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c941-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c941-178">Usando propriedades</span><span class="sxs-lookup"><span data-stu-id="8c941-178">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="8c941-179">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="8c941-179">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 



