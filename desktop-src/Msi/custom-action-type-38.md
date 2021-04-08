---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 38 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Tipo de ação personalizada 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922247"
---
# <a name="custom-action-type-38"></a><span data-ttu-id="75a30-103">Tipo de ação personalizada 38</span><span class="sxs-lookup"><span data-stu-id="75a30-103">Custom Action Type 38</span></span>

<span data-ttu-id="75a30-104">Essa ação personalizada é escrita em VBScript.</span><span class="sxs-lookup"><span data-stu-id="75a30-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="75a30-105">Consulte também [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="75a30-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="75a30-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="75a30-106">Source</span></span>

<span data-ttu-id="75a30-107">O campo de origem da [tabela CustomAction](customaction-table.md) contém o valor nulo.</span><span class="sxs-lookup"><span data-stu-id="75a30-107">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="75a30-108">O código de script para a ação personalizada é armazenado como uma cadeia de caracteres de texto de script literal no campo de destino.</span><span class="sxs-lookup"><span data-stu-id="75a30-108">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="75a30-109">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="75a30-109">Type Value</span></span>

<span data-ttu-id="75a30-110">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="75a30-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="75a30-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="75a30-111">Constants</span></span>                                                              | <span data-ttu-id="75a30-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="75a30-112">Hexadecimal</span></span> | <span data-ttu-id="75a30-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="75a30-113">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="75a30-114">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="75a30-114">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="75a30-115">0x026</span><span class="sxs-lookup"><span data-stu-id="75a30-115">0x026</span></span>       | <span data-ttu-id="75a30-116">38</span><span class="sxs-lookup"><span data-stu-id="75a30-116">38</span></span>      |



 

<span data-ttu-id="75a30-117">Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="75a30-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="75a30-118">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="75a30-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="75a30-119">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="75a30-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="75a30-120">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="75a30-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="75a30-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="75a30-121">Constants</span></span>                                                                                                     | <span data-ttu-id="75a30-122">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="75a30-122">Hexadecimal</span></span> | <span data-ttu-id="75a30-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="75a30-123">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="75a30-124">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="75a30-124">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="75a30-125">0x0001026</span><span class="sxs-lookup"><span data-stu-id="75a30-125">0x0001026</span></span>   | <span data-ttu-id="75a30-126">4134</span><span class="sxs-lookup"><span data-stu-id="75a30-126">4134</span></span>    |



 

## <a name="target"></a><span data-ttu-id="75a30-127">Destino</span><span class="sxs-lookup"><span data-stu-id="75a30-127">Target</span></span>

<span data-ttu-id="75a30-128">O campo de destino da [tabela CustomAction](customaction-table.md) contém o código de script para a ação personalizada como uma cadeia de caracteres de texto de script literal.</span><span class="sxs-lookup"><span data-stu-id="75a30-128">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="75a30-129">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="75a30-129">Return Processing Options</span></span>

<span data-ttu-id="75a30-130">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="75a30-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="75a30-131">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="75a30-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="75a30-132">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="75a30-132">Execution Scheduling Options</span></span>

<span data-ttu-id="75a30-133">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="75a30-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="75a30-134">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="75a30-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="75a30-135">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="75a30-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="75a30-136">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="75a30-136">In-Script Execution Options</span></span>

<span data-ttu-id="75a30-137">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="75a30-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="75a30-138">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="75a30-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="75a30-139">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="75a30-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="75a30-140">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="75a30-140">Return Values</span></span>

<span data-ttu-id="75a30-141">Esse tipo de ação personalizada sempre retorna êxito.</span><span class="sxs-lookup"><span data-stu-id="75a30-141">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a30-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="75a30-142">Remarks</span></span>

<span data-ttu-id="75a30-143">Uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação.</span><span class="sxs-lookup"><span data-stu-id="75a30-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="75a30-144">O instalador anexa o **objeto de sessão** ao script com o nome "Session".</span><span class="sxs-lookup"><span data-stu-id="75a30-144">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="75a30-145">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.</span><span class="sxs-lookup"><span data-stu-id="75a30-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75a30-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75a30-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75a30-147">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="75a30-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



