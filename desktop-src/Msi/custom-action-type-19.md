---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 19 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo de ação personalizada 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787504"
---
# <a name="custom-action-type-19"></a><span data-ttu-id="87da1-103">Tipo de ação personalizada 19</span><span class="sxs-lookup"><span data-stu-id="87da1-103">Custom Action Type 19</span></span>

<span data-ttu-id="87da1-104">Essa ação personalizada exibe uma mensagem de erro especificada, retorna falha e, em seguida, encerra a instalação.</span><span class="sxs-lookup"><span data-stu-id="87da1-104">This custom action displays a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="87da1-105">A mensagem de erro exibida pode ser fornecida como uma cadeia de caracteres ou como um índice na [tabela de erros](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="87da1-105">The error message displayed can be supplied as a string or as an index into the [Error table](error-table.md).</span></span>

## <a name="source"></a><span data-ttu-id="87da1-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="87da1-106">Source</span></span>

<span data-ttu-id="87da1-107">Deixe a coluna de origem da [tabela CustomAction](customaction-table.md) em branco.</span><span class="sxs-lookup"><span data-stu-id="87da1-107">Leave the Source column of the [CustomAction table](customaction-table.md) blank.</span></span>

## <a name="type-value"></a><span data-ttu-id="87da1-108">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="87da1-108">Type Value</span></span>

<span data-ttu-id="87da1-109">Inclua o seguinte valor na coluna tipo da tabela CustomAction para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="87da1-109">Include the following value in the Type column of the CustomAction table to specify the basic numeric type.</span></span>



| <span data-ttu-id="87da1-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="87da1-110">Constants</span></span>                                                               | <span data-ttu-id="87da1-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="87da1-111">Hexadecimal</span></span> | <span data-ttu-id="87da1-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="87da1-112">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="87da1-113">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="87da1-113">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="87da1-114">0x013</span><span class="sxs-lookup"><span data-stu-id="87da1-114">0x013</span></span>       | <span data-ttu-id="87da1-115">19</span><span class="sxs-lookup"><span data-stu-id="87da1-115">19</span></span>      |



 

## <a name="target"></a><span data-ttu-id="87da1-116">Destino</span><span class="sxs-lookup"><span data-stu-id="87da1-116">Target</span></span>

<span data-ttu-id="87da1-117">A coluna Target da [tabela CustomAction](customaction-table.md) contém uma cadeia de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico).</span><span class="sxs-lookup"><span data-stu-id="87da1-117">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="87da1-118">Os parâmetros a serem substituídos são colocados entre colchetes, \[ ... \] e podem ser Propriedades, variáveis de ambiente (% Prefix), caminhos de arquivo ( \# prefixo) ou caminhos de diretório de componente ($ Prefix).</span><span class="sxs-lookup"><span data-stu-id="87da1-118">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="87da1-119">Se depois de Formatar a cadeia de caracteres for avaliada como um inteiro, esse inteiro será usado como um índice na [tabela de erros](error-table.md) para recuperar a mensagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="87da1-119">If after formatting the string evaluates to an integer, that integer is used as an index into the [Error table](error-table.md) to retrieve the message to display.</span></span> <span data-ttu-id="87da1-120">Se, depois de Formatar, a cadeia de caracteres contiver caracteres não numéricos, a cadeia de caracteres será exibida como a mensagem.</span><span class="sxs-lookup"><span data-stu-id="87da1-120">If after formatting the string contains non-numeric characters, the string itself is displayed as the message.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="87da1-121">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="87da1-121">Return Processing Options</span></span>

<span data-ttu-id="87da1-122">A ação personalizada não usa nenhuma opção.</span><span class="sxs-lookup"><span data-stu-id="87da1-122">The custom action does not use any options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="87da1-123">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="87da1-123">Execution Scheduling Options</span></span>

<span data-ttu-id="87da1-124">A ação personalizada não usa nenhuma opção.</span><span class="sxs-lookup"><span data-stu-id="87da1-124">The custom action does not use any options.</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="87da1-125">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="87da1-125">In-Script Execution Options</span></span>

<span data-ttu-id="87da1-126">A ação personalizada não usa nenhuma opção.</span><span class="sxs-lookup"><span data-stu-id="87da1-126">The custom action does not use any options.</span></span>

## <a name="return-values"></a><span data-ttu-id="87da1-127">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="87da1-127">Return Values</span></span>

<span data-ttu-id="87da1-128">Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="87da1-128">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87da1-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="87da1-129">Remarks</span></span>

<span data-ttu-id="87da1-130">Por exemplo, as ações personalizadas CAError1, CAError2, CAError3 e CAError4 retornam essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="87da1-130">For example, the custom actions CAError1, CAError2, CAError3, and CAError4 return these messages.</span></span>

[<span data-ttu-id="87da1-131">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="87da1-131">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="87da1-132">Ação</span><span class="sxs-lookup"><span data-stu-id="87da1-132">Action</span></span>   | <span data-ttu-id="87da1-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="87da1-133">Type</span></span> | <span data-ttu-id="87da1-134">Fonte</span><span class="sxs-lookup"><span data-stu-id="87da1-134">Source</span></span> | <span data-ttu-id="87da1-135">Destino</span><span class="sxs-lookup"><span data-stu-id="87da1-135">Target</span></span>                              |
|----------|------|--------|-------------------------------------|
| <span data-ttu-id="87da1-136">CAError1</span><span class="sxs-lookup"><span data-stu-id="87da1-136">CAError1</span></span> | <span data-ttu-id="87da1-137">19</span><span class="sxs-lookup"><span data-stu-id="87da1-137">19</span></span>   |        | <span data-ttu-id="87da1-138">\[Prop1\]</span><span class="sxs-lookup"><span data-stu-id="87da1-138">\[Prop1\]</span></span>                           |
| <span data-ttu-id="87da1-139">CAError2</span><span class="sxs-lookup"><span data-stu-id="87da1-139">CAError2</span></span> | <span data-ttu-id="87da1-140">19</span><span class="sxs-lookup"><span data-stu-id="87da1-140">19</span></span>   |        | <span data-ttu-id="87da1-141">Falha na instalação devido a Error2.</span><span class="sxs-lookup"><span data-stu-id="87da1-141">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="87da1-142">CAError3</span><span class="sxs-lookup"><span data-stu-id="87da1-142">CAError3</span></span> | <span data-ttu-id="87da1-143">19</span><span class="sxs-lookup"><span data-stu-id="87da1-143">19</span></span>   |        | <span data-ttu-id="87da1-144">25000</span><span class="sxs-lookup"><span data-stu-id="87da1-144">25000</span></span>                               |
| <span data-ttu-id="87da1-145">CAError4</span><span class="sxs-lookup"><span data-stu-id="87da1-145">CAError4</span></span> | <span data-ttu-id="87da1-146">19</span><span class="sxs-lookup"><span data-stu-id="87da1-146">19</span></span>   |        | <span data-ttu-id="87da1-147">\[Prop2\]</span><span class="sxs-lookup"><span data-stu-id="87da1-147">\[Prop2\]</span></span>                           |



 

[<span data-ttu-id="87da1-148">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="87da1-148">Property Table</span></span>](property-table.md)



| <span data-ttu-id="87da1-149">Propriedade</span><span class="sxs-lookup"><span data-stu-id="87da1-149">Property</span></span> | <span data-ttu-id="87da1-150">Valor</span><span class="sxs-lookup"><span data-stu-id="87da1-150">Value</span></span>                                 |
|----------|---------------------------------------|
| <span data-ttu-id="87da1-151">Prop1</span><span class="sxs-lookup"><span data-stu-id="87da1-151">Prop1</span></span>    | <span data-ttu-id="87da1-152">"Falha na instalação devido a Error1."</span><span class="sxs-lookup"><span data-stu-id="87da1-152">"Installation failure due to Error1."</span></span> |
| <span data-ttu-id="87da1-153">Prop2</span><span class="sxs-lookup"><span data-stu-id="87da1-153">Prop2</span></span>    | <span data-ttu-id="87da1-154">"25100"</span><span class="sxs-lookup"><span data-stu-id="87da1-154">"25100"</span></span>                               |



 

[<span data-ttu-id="87da1-155">Tabela de erros</span><span class="sxs-lookup"><span data-stu-id="87da1-155">Error Table</span></span>](error-table.md)



| <span data-ttu-id="87da1-156">Código</span><span class="sxs-lookup"><span data-stu-id="87da1-156">Code</span></span>  | <span data-ttu-id="87da1-157">Mensagem</span><span class="sxs-lookup"><span data-stu-id="87da1-157">Message</span></span>                             |
|-------|-------------------------------------|
| <span data-ttu-id="87da1-158">25000</span><span class="sxs-lookup"><span data-stu-id="87da1-158">25000</span></span> | <span data-ttu-id="87da1-159">Falha na instalação devido a Error3.</span><span class="sxs-lookup"><span data-stu-id="87da1-159">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="87da1-160">25100</span><span class="sxs-lookup"><span data-stu-id="87da1-160">25100</span></span> | <span data-ttu-id="87da1-161">Falha na instalação devido a Error4.</span><span class="sxs-lookup"><span data-stu-id="87da1-161">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="87da1-162">Essas ações personalizadas retornam as seguintes mensagens de erro:</span><span class="sxs-lookup"><span data-stu-id="87da1-162">These custom actions return the following error messages:</span></span>



| <span data-ttu-id="87da1-163">Ação personalizada</span><span class="sxs-lookup"><span data-stu-id="87da1-163">Custom action</span></span> | <span data-ttu-id="87da1-164">Cadeia de caracteres de mensagem retornada</span><span class="sxs-lookup"><span data-stu-id="87da1-164">Returned message string</span></span>             |
|---------------|-------------------------------------|
| <span data-ttu-id="87da1-165">CAError1</span><span class="sxs-lookup"><span data-stu-id="87da1-165">CAError1</span></span>      | <span data-ttu-id="87da1-166">Falha na instalação devido a Error1.</span><span class="sxs-lookup"><span data-stu-id="87da1-166">Installation failure due to Error1.</span></span> |
| <span data-ttu-id="87da1-167">CAError2</span><span class="sxs-lookup"><span data-stu-id="87da1-167">CAError2</span></span>      | <span data-ttu-id="87da1-168">Falha na instalação devido a Error2.</span><span class="sxs-lookup"><span data-stu-id="87da1-168">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="87da1-169">CAError3</span><span class="sxs-lookup"><span data-stu-id="87da1-169">CAError3</span></span>      | <span data-ttu-id="87da1-170">Falha na instalação devido a Error3.</span><span class="sxs-lookup"><span data-stu-id="87da1-170">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="87da1-171">CAError4</span><span class="sxs-lookup"><span data-stu-id="87da1-171">CAError4</span></span>      | <span data-ttu-id="87da1-172">Falha na instalação devido a Error4.</span><span class="sxs-lookup"><span data-stu-id="87da1-172">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="87da1-173">Observe que, como a ordem de avaliação das condições de inicialização não pode ser garantida ao criar a [tabela LaunchCondition](launchcondition-table.md), você deve usar as ações personalizadas do tipo de ação personalizada 19 em sua instalação para avaliar as condições em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="87da1-173">Note that because the order of evaluation of launch conditions cannot be guaranteed by authoring the [LaunchCondition table](launchcondition-table.md), you should use Custom Action Type 19 custom actions in your installation to evaluate conditions in a specific order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87da1-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87da1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87da1-175">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="87da1-175">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



