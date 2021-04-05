---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 53 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Tipo de ação personalizada 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a016d3b3f5a282567b909215d6ab7b32759417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922047"
---
# <a name="custom-action-type-53"></a><span data-ttu-id="9de1b-103">Tipo de ação personalizada 53</span><span class="sxs-lookup"><span data-stu-id="9de1b-103">Custom Action Type 53</span></span>

<span data-ttu-id="9de1b-104">Essa ação personalizada é escrita em JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="9de1b-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="9de1b-105">Windows Installer não dá suporte a JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="9de1b-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="9de1b-106">Para obter mais informações, consulte [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9de1b-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="9de1b-107">Fonte</span><span class="sxs-lookup"><span data-stu-id="9de1b-107">Source</span></span>

<span data-ttu-id="9de1b-108">O campo de origem da [tabela CustomAction](customaction-table.md) contém um nome de propriedade ou uma chave para a [tabela de propriedades](property-table.md) de uma propriedade que contém o texto do script.</span><span class="sxs-lookup"><span data-stu-id="9de1b-108">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="9de1b-109">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="9de1b-109">Type Value</span></span>

<span data-ttu-id="9de1b-110">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9de1b-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="9de1b-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="9de1b-111">Constants</span></span>                                                            | <span data-ttu-id="9de1b-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="9de1b-112">Hexadecimal</span></span> | <span data-ttu-id="9de1b-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="9de1b-113">Decimal</span></span> |
|----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9de1b-114">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="9de1b-114">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="9de1b-115">0x035</span><span class="sxs-lookup"><span data-stu-id="9de1b-115">0x035</span></span>       | <span data-ttu-id="9de1b-116">53</span><span class="sxs-lookup"><span data-stu-id="9de1b-116">53</span></span>      |



 

<span data-ttu-id="9de1b-117">Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9de1b-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="9de1b-118">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="9de1b-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="9de1b-119">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9de1b-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="9de1b-120">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9de1b-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="9de1b-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="9de1b-121">Constants</span></span>                                                                                                   | <span data-ttu-id="9de1b-122">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="9de1b-122">Hexadecimal</span></span> | <span data-ttu-id="9de1b-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="9de1b-123">Decimal</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9de1b-124">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="9de1b-124">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="9de1b-125">0x0001035</span><span class="sxs-lookup"><span data-stu-id="9de1b-125">0x0001035</span></span>   | <span data-ttu-id="9de1b-126">4149</span><span class="sxs-lookup"><span data-stu-id="9de1b-126">4149</span></span>    |



 

## <a name="target"></a><span data-ttu-id="9de1b-127">Destino</span><span class="sxs-lookup"><span data-stu-id="9de1b-127">Target</span></span>

<span data-ttu-id="9de1b-128">O campo de destino da [tabela CustomAction](customaction-table.md) contém uma função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="9de1b-128">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="9de1b-129">O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="9de1b-129">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9de1b-130">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="9de1b-130">Return Processing Options</span></span>

<span data-ttu-id="9de1b-131">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="9de1b-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9de1b-132">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="9de1b-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9de1b-133">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="9de1b-133">Execution Scheduling Options</span></span>

<span data-ttu-id="9de1b-134">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="9de1b-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9de1b-135">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9de1b-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9de1b-136">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="9de1b-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9de1b-137">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="9de1b-137">In-Script Execution Options</span></span>

<span data-ttu-id="9de1b-138">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="9de1b-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9de1b-139">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="9de1b-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9de1b-140">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="9de1b-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9de1b-141">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="9de1b-141">Return Values</span></span>

<span data-ttu-id="9de1b-142">Funções opcionais escritas em script devem retornar um dos valores descritos em [valores de retorno de ações personalizadas JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9de1b-142">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9de1b-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="9de1b-143">Remarks</span></span>

<span data-ttu-id="9de1b-144">Uma ação personalizada escrita em JScript requer o objeto de [**sessão**](session-object.md) de instalação.</span><span class="sxs-lookup"><span data-stu-id="9de1b-144">A custom action that is written in JScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="9de1b-145">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script usa um dos métodos descritos em [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9de1b-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script uses one of the methods described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9de1b-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9de1b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9de1b-147">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="9de1b-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



