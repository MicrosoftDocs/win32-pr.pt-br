---
description: O ICE34 valida que cada botão de opção em cada controle do grupo de botões tem uma propriedade na coluna propriedade da tabela RadioButton que especifica seu grupo de botões de opção.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755083"
---
# <a name="ice34"></a><span data-ttu-id="de2a6-103">ICE34</span><span class="sxs-lookup"><span data-stu-id="de2a6-103">ICE34</span></span>

<span data-ttu-id="de2a6-104">O ICE34 valida que cada botão de opção em cada controle do grupo de [botões](radiobuttongroup-control.md) tem uma propriedade na coluna propriedade da [tabela RadioButton](radiobutton-table.md) que especifica seu grupo de botões de opção.</span><span class="sxs-lookup"><span data-stu-id="de2a6-104">ICE34 validates that each radio button on every [RadioButtonGroup Control](radiobuttongroup-control.md) has a property in the Property column of the [RadioButton table](radiobutton-table.md) that specifies its radio button group.</span></span> <span data-ttu-id="de2a6-105">ICE34 valida que essa propriedade existe e é definida como um valor padrão na tabela de [Propriedades](property-table.md) , que é igual a um dos valores de botão de opção do grupo na coluna valor da tabela RadioButton.</span><span class="sxs-lookup"><span data-stu-id="de2a6-105">ICE34 validates that this property exists and is set to a default value in the [Property table](property-table.md) which is equal to one of the group's radio button values in the Value column of the RadioButton table.</span></span>

<span data-ttu-id="de2a6-106">Um grupo de botões de opção deve ter um padrão para que os usuários possam selecionar uma opção usando a tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="de2a6-106">A radio button group must have a default for users to be able to select a choice using the TAB key.</span></span> <span data-ttu-id="de2a6-107">Isso é necessário para a acessibilidade adequada do usuário.</span><span class="sxs-lookup"><span data-stu-id="de2a6-107">This is required for proper user accessibility.</span></span>

<span data-ttu-id="de2a6-108">ICE34 relata tabelas ausentes.</span><span class="sxs-lookup"><span data-stu-id="de2a6-108">ICE34 reports missing tables.</span></span>

## <a name="result"></a><span data-ttu-id="de2a6-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="de2a6-109">Result</span></span>

<span data-ttu-id="de2a6-110">ICE34 postar uma mensagem de erro se houver um botão de opção que especifique uma propriedade inválida.</span><span class="sxs-lookup"><span data-stu-id="de2a6-110">ICE34 post an error message if there is a radio button that specifies an invalid property.</span></span>

## <a name="example"></a><span data-ttu-id="de2a6-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="de2a6-111">Example</span></span>

<span data-ttu-id="de2a6-112">ICE34 relata os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="de2a6-112">ICE34 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="de2a6-113">Erro de ICE34</span><span class="sxs-lookup"><span data-stu-id="de2a6-113">ICE34 error</span></span>                                                                                                                                                                | <span data-ttu-id="de2a6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="de2a6-114">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de2a6-115">Control caixa de diálogo. Control2 deve ter uma propriedade porque é do tipo RadioButton.</span><span class="sxs-lookup"><span data-stu-id="de2a6-115">Control DialogA.Control2 must have a property because it is of type RadioButtonGroup.</span></span>                                                                                      | <span data-ttu-id="de2a6-116">Há um controle de grupo de [botões](radiobuttongroup-control.md), sem o bit de [controle indireto](indirect-control-attribute.md) definido na coluna atributos da [tabela de controle](control-table.md), que não tem uma propriedade listada na coluna propriedade.</span><span class="sxs-lookup"><span data-stu-id="de2a6-116">There is a [RadioButtonGroup control](radiobuttongroup-control.md), without the [Indirect control](indirect-control-attribute.md) bit set in the Attributes column of the [Control table](control-table.md), that does not have a property listed in the Property column.</span></span> |
| <span data-ttu-id="de2a6-117">Talvez não seja um valor padrão válido para o messagebutton usando a propriedade Property3.</span><span class="sxs-lookup"><span data-stu-id="de2a6-117">Maybe is not a valid default value for the RadioButtonGroup using property Property3.</span></span> <span data-ttu-id="de2a6-118">O valor deve ser listado como uma opção na tabela de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="de2a6-118">The value must be listed as an option in the RadioButtonGroup table.</span></span>                 | <span data-ttu-id="de2a6-119">Há um valor padrão para uma propriedade especificada na coluna valor da [tabela de propriedades](property-table.md) que não é um dos valores para o grupo de botões de opção especificado na coluna valor da [tabela RadioButton](radiobutton-table.md).</span><span class="sxs-lookup"><span data-stu-id="de2a6-119">There is a default value for a property specified in the Value column of the [Property table](property-table.md) that is not one of the values for the radio button group specified in the Value column of the [RadioButton table](radiobutton-table.md).</span></span>                  |
| <span data-ttu-id="de2a6-120">A propriedade PropertyB deve ser definida porque é uma propriedade indireta de um controle de botão de caixa de diálogo. Control4</span><span class="sxs-lookup"><span data-stu-id="de2a6-120">Property PropertyB must be defined because it is an indirect property of a RadioButtonGroup control DialogA.Control4</span></span>                                                       | <span data-ttu-id="de2a6-121">A propriedade referenciada por este grupo de botões de opção é uma propriedade indireta e o valor da propriedade indireta não é uma das opções para o grupo de botões de opção.</span><span class="sxs-lookup"><span data-stu-id="de2a6-121">The property referenced by this RadioButton group is an indirect property, and the value of the indirect property is not one of the choices for the RadioButton group.</span></span>                                                                                                       |
| <span data-ttu-id="de2a6-122">Talvez não seja um valor padrão válido para a propriedade propertya.</span><span class="sxs-lookup"><span data-stu-id="de2a6-122">Maybe is not a valid default value for the property PropertyA.</span></span> <span data-ttu-id="de2a6-123">A propriedade é uma propriedade do botão de opção indireto do controle dialogo. Control5 (via Propriedade Property5).</span><span class="sxs-lookup"><span data-stu-id="de2a6-123">The property is an indirect RadioButtonGroup property of control DialogA.Control5 (via property Property5).</span></span> | <span data-ttu-id="de2a6-124">O valor da propriedade indireta referenciada por meio do controle não é um dos valores padrão para esse botão de opção.</span><span class="sxs-lookup"><span data-stu-id="de2a6-124">The value of the indirect property referenced via the control is not one of the default values for that RadioButtonGroup.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="de2a6-125">[Tabela de controle](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="de2a6-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="de2a6-126">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="de2a6-126">Dialog</span></span>  | <span data-ttu-id="de2a6-127">Control</span><span class="sxs-lookup"><span data-stu-id="de2a6-127">Control</span></span>  | <span data-ttu-id="de2a6-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="de2a6-128">Type</span></span>             | <span data-ttu-id="de2a6-129">Atributos</span><span class="sxs-lookup"><span data-stu-id="de2a6-129">Attributes</span></span> | <span data-ttu-id="de2a6-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2a6-130">Property</span></span>  |
|---------|----------|------------------|------------|-----------|
| <span data-ttu-id="de2a6-131">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="de2a6-131">DialogA</span></span> | <span data-ttu-id="de2a6-132">Control1</span><span class="sxs-lookup"><span data-stu-id="de2a6-132">Control1</span></span> | <span data-ttu-id="de2a6-133">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="de2a6-133">RadioButtonGroup</span></span> | <span data-ttu-id="de2a6-134">0</span><span class="sxs-lookup"><span data-stu-id="de2a6-134">0</span></span>          | <span data-ttu-id="de2a6-135">Property1</span><span class="sxs-lookup"><span data-stu-id="de2a6-135">Property1</span></span> |
| <span data-ttu-id="de2a6-136">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="de2a6-136">DialogA</span></span> | <span data-ttu-id="de2a6-137">Control2</span><span class="sxs-lookup"><span data-stu-id="de2a6-137">Control2</span></span> | <span data-ttu-id="de2a6-138">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="de2a6-138">RadioButtonGroup</span></span> | <span data-ttu-id="de2a6-139">0</span><span class="sxs-lookup"><span data-stu-id="de2a6-139">0</span></span>          |           |
| <span data-ttu-id="de2a6-140">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="de2a6-140">DialogA</span></span> | <span data-ttu-id="de2a6-141">Control3</span><span class="sxs-lookup"><span data-stu-id="de2a6-141">Control3</span></span> | <span data-ttu-id="de2a6-142">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="de2a6-142">RadioButtonGroup</span></span> | <span data-ttu-id="de2a6-143">0</span><span class="sxs-lookup"><span data-stu-id="de2a6-143">0</span></span>          | <span data-ttu-id="de2a6-144">Property3</span><span class="sxs-lookup"><span data-stu-id="de2a6-144">Property3</span></span> |
| <span data-ttu-id="de2a6-145">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="de2a6-145">DialogA</span></span> | <span data-ttu-id="de2a6-146">Control4</span><span class="sxs-lookup"><span data-stu-id="de2a6-146">Control4</span></span> | <span data-ttu-id="de2a6-147">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="de2a6-147">RadioButtonGroup</span></span> | <span data-ttu-id="de2a6-148">8</span><span class="sxs-lookup"><span data-stu-id="de2a6-148">8</span></span>          | <span data-ttu-id="de2a6-149">Property4</span><span class="sxs-lookup"><span data-stu-id="de2a6-149">Property4</span></span> |
| <span data-ttu-id="de2a6-150">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="de2a6-150">DialogA</span></span> | <span data-ttu-id="de2a6-151">Control5</span><span class="sxs-lookup"><span data-stu-id="de2a6-151">Control5</span></span> | <span data-ttu-id="de2a6-152">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="de2a6-152">RadioButtonGroup</span></span> | <span data-ttu-id="de2a6-153">8</span><span class="sxs-lookup"><span data-stu-id="de2a6-153">8</span></span>          | <span data-ttu-id="de2a6-154">Property5</span><span class="sxs-lookup"><span data-stu-id="de2a6-154">Property5</span></span> |



 

<span data-ttu-id="de2a6-155">[Tabela de propriedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="de2a6-155">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="de2a6-156">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2a6-156">Property</span></span>  | <span data-ttu-id="de2a6-157">Valor</span><span class="sxs-lookup"><span data-stu-id="de2a6-157">Value</span></span>     |
|-----------|-----------|
| <span data-ttu-id="de2a6-158">Property1</span><span class="sxs-lookup"><span data-stu-id="de2a6-158">Property1</span></span> | <span data-ttu-id="de2a6-159">Yes</span><span class="sxs-lookup"><span data-stu-id="de2a6-159">Yes</span></span>       |
| <span data-ttu-id="de2a6-160">Property3</span><span class="sxs-lookup"><span data-stu-id="de2a6-160">Property3</span></span> | <span data-ttu-id="de2a6-161">Talvez</span><span class="sxs-lookup"><span data-stu-id="de2a6-161">Maybe</span></span>     |
| <span data-ttu-id="de2a6-162">Property4</span><span class="sxs-lookup"><span data-stu-id="de2a6-162">Property4</span></span> | <span data-ttu-id="de2a6-163">PropertyB</span><span class="sxs-lookup"><span data-stu-id="de2a6-163">PropertyB</span></span> |
| <span data-ttu-id="de2a6-164">Property5</span><span class="sxs-lookup"><span data-stu-id="de2a6-164">Property5</span></span> | <span data-ttu-id="de2a6-165">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2a6-165">PropertyA</span></span> |
| <span data-ttu-id="de2a6-166">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2a6-166">PropertyA</span></span> | <span data-ttu-id="de2a6-167">Talvez</span><span class="sxs-lookup"><span data-stu-id="de2a6-167">Maybe</span></span>     |



 

<span data-ttu-id="de2a6-168">[Tabela RadioButton](radiobutton-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="de2a6-168">[RadioButton Table](radiobutton-table.md) (partial)</span></span>



| <span data-ttu-id="de2a6-169">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2a6-169">Property</span></span>  | <span data-ttu-id="de2a6-170">Ordem</span><span class="sxs-lookup"><span data-stu-id="de2a6-170">Order</span></span> | <span data-ttu-id="de2a6-171">Valor</span><span class="sxs-lookup"><span data-stu-id="de2a6-171">Value</span></span> |
|-----------|-------|-------|
| <span data-ttu-id="de2a6-172">Property1</span><span class="sxs-lookup"><span data-stu-id="de2a6-172">Property1</span></span> | <span data-ttu-id="de2a6-173">1</span><span class="sxs-lookup"><span data-stu-id="de2a6-173">1</span></span>     | <span data-ttu-id="de2a6-174">Sim</span><span class="sxs-lookup"><span data-stu-id="de2a6-174">Yes</span></span>   |
| <span data-ttu-id="de2a6-175">Property1</span><span class="sxs-lookup"><span data-stu-id="de2a6-175">Property1</span></span> | <span data-ttu-id="de2a6-176">2</span><span class="sxs-lookup"><span data-stu-id="de2a6-176">2</span></span>     | <span data-ttu-id="de2a6-177">Agora</span><span class="sxs-lookup"><span data-stu-id="de2a6-177">Now</span></span>   |
| <span data-ttu-id="de2a6-178">Property2</span><span class="sxs-lookup"><span data-stu-id="de2a6-178">Property2</span></span> | <span data-ttu-id="de2a6-179">1</span><span class="sxs-lookup"><span data-stu-id="de2a6-179">1</span></span>     | <span data-ttu-id="de2a6-180">Sim</span><span class="sxs-lookup"><span data-stu-id="de2a6-180">Yes</span></span>   |
| <span data-ttu-id="de2a6-181">Property2</span><span class="sxs-lookup"><span data-stu-id="de2a6-181">Property2</span></span> | <span data-ttu-id="de2a6-182">2</span><span class="sxs-lookup"><span data-stu-id="de2a6-182">2</span></span>     | <span data-ttu-id="de2a6-183">Não</span><span class="sxs-lookup"><span data-stu-id="de2a6-183">No</span></span>    |
| <span data-ttu-id="de2a6-184">Property3</span><span class="sxs-lookup"><span data-stu-id="de2a6-184">Property3</span></span> | <span data-ttu-id="de2a6-185">1</span><span class="sxs-lookup"><span data-stu-id="de2a6-185">1</span></span>     | <span data-ttu-id="de2a6-186">Sim</span><span class="sxs-lookup"><span data-stu-id="de2a6-186">Yes</span></span>   |
| <span data-ttu-id="de2a6-187">Property3</span><span class="sxs-lookup"><span data-stu-id="de2a6-187">Property3</span></span> | <span data-ttu-id="de2a6-188">2</span><span class="sxs-lookup"><span data-stu-id="de2a6-188">2</span></span>     | <span data-ttu-id="de2a6-189">Não</span><span class="sxs-lookup"><span data-stu-id="de2a6-189">No</span></span>    |
| <span data-ttu-id="de2a6-190">Property4</span><span class="sxs-lookup"><span data-stu-id="de2a6-190">Property4</span></span> | <span data-ttu-id="de2a6-191">1</span><span class="sxs-lookup"><span data-stu-id="de2a6-191">1</span></span>     | <span data-ttu-id="de2a6-192">Sim</span><span class="sxs-lookup"><span data-stu-id="de2a6-192">Yes</span></span>   |
| <span data-ttu-id="de2a6-193">Property4</span><span class="sxs-lookup"><span data-stu-id="de2a6-193">Property4</span></span> | <span data-ttu-id="de2a6-194">2</span><span class="sxs-lookup"><span data-stu-id="de2a6-194">2</span></span>     | <span data-ttu-id="de2a6-195">Não</span><span class="sxs-lookup"><span data-stu-id="de2a6-195">No</span></span>    |
| <span data-ttu-id="de2a6-196">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2a6-196">PropertyA</span></span> | <span data-ttu-id="de2a6-197">1</span><span class="sxs-lookup"><span data-stu-id="de2a6-197">1</span></span>     | <span data-ttu-id="de2a6-198">Sim</span><span class="sxs-lookup"><span data-stu-id="de2a6-198">Yes</span></span>   |
| <span data-ttu-id="de2a6-199">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2a6-199">PropertyA</span></span> | <span data-ttu-id="de2a6-200">2</span><span class="sxs-lookup"><span data-stu-id="de2a6-200">2</span></span>     | <span data-ttu-id="de2a6-201">Não</span><span class="sxs-lookup"><span data-stu-id="de2a6-201">No</span></span>    |
| <span data-ttu-id="de2a6-202">PropertyB</span><span class="sxs-lookup"><span data-stu-id="de2a6-202">PropertyB</span></span> | <span data-ttu-id="de2a6-203">1</span><span class="sxs-lookup"><span data-stu-id="de2a6-203">1</span></span>     | <span data-ttu-id="de2a6-204">Sim</span><span class="sxs-lookup"><span data-stu-id="de2a6-204">Yes</span></span>   |
| <span data-ttu-id="de2a6-205">PropertyB</span><span class="sxs-lookup"><span data-stu-id="de2a6-205">PropertyB</span></span> | <span data-ttu-id="de2a6-206">2</span><span class="sxs-lookup"><span data-stu-id="de2a6-206">2</span></span>     | <span data-ttu-id="de2a6-207">Não</span><span class="sxs-lookup"><span data-stu-id="de2a6-207">No</span></span>    |



 

<span data-ttu-id="de2a6-208">Para corrigir os erros relatados por este ICE, verifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="de2a6-208">To fix the errors reported by this ICE, check the following:</span></span>

-   <span data-ttu-id="de2a6-209">Que cada entrada de controle RadioButton sem o conjunto de atributos indiretos tem uma propriedade listada na coluna Propriedade:</span><span class="sxs-lookup"><span data-stu-id="de2a6-209">That every RadioButton control entry without the indirect attribute set has a property listed in the Property column:</span></span>
-   <span data-ttu-id="de2a6-210">Cada propriedade desse tipo tem pelo menos uma entrada correspondente na tabela RadioButton.</span><span class="sxs-lookup"><span data-stu-id="de2a6-210">That every such property has at least one corresponding entry in the RadioButton table.</span></span>
-   <span data-ttu-id="de2a6-211">Que cada propriedade desse tipo é definida na tabela de propriedades, com um valor que é uma das opções da tabela RadioButton.</span><span class="sxs-lookup"><span data-stu-id="de2a6-211">That every such property is defined in the Property table, with a value that is one of the choices from the RadioButton table.</span></span>
-   <span data-ttu-id="de2a6-212">Que cada propriedade referenciada na coluna Property de um controle RadioButton com o conjunto de atributos indiretos é definida na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="de2a6-212">That every property referenced in the Property column of a RadioButton control with the indirect attribute set is defined in the Property table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de2a6-213">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de2a6-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de2a6-214">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="de2a6-214">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



