---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 54 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Tipo de ação personalizada 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461252"
---
# <a name="custom-action-type-54"></a><span data-ttu-id="c5850-103">Tipo de ação personalizada 54</span><span class="sxs-lookup"><span data-stu-id="c5850-103">Custom Action Type 54</span></span>

<span data-ttu-id="c5850-104">Essa ação personalizada é escrita em VBScript.</span><span class="sxs-lookup"><span data-stu-id="c5850-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="c5850-105">Consulte também [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c5850-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="c5850-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="c5850-106">Source</span></span>

<span data-ttu-id="c5850-107">O campo de origem da [tabela CustomAction](customaction-table.md) contém um nome de propriedade ou uma chave para a [tabela de propriedades](property-table.md) de uma propriedade que contém o texto do script.</span><span class="sxs-lookup"><span data-stu-id="c5850-107">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="c5850-108">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="c5850-108">Type Value</span></span>

<span data-ttu-id="c5850-109">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c5850-109">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="c5850-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="c5850-110">Constants</span></span>                                                             | <span data-ttu-id="c5850-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c5850-111">Hexadecimal</span></span> | <span data-ttu-id="c5850-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="c5850-112">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="c5850-113">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="c5850-113">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="c5850-114">0x036</span><span class="sxs-lookup"><span data-stu-id="c5850-114">0x036</span></span>       | <span data-ttu-id="c5850-115">54</span><span class="sxs-lookup"><span data-stu-id="c5850-115">54</span></span>      |



 

<span data-ttu-id="c5850-116">Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c5850-116">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="c5850-117">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="c5850-117">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="c5850-118">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c5850-118">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="c5850-119">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c5850-119">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="c5850-120">Constantes</span><span class="sxs-lookup"><span data-stu-id="c5850-120">Constants</span></span>                                                                                                    | <span data-ttu-id="c5850-121">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c5850-121">Hexadecimal</span></span> | <span data-ttu-id="c5850-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="c5850-122">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="c5850-123">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="c5850-123">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="c5850-124">0x0001036</span><span class="sxs-lookup"><span data-stu-id="c5850-124">0x0001036</span></span>   | <span data-ttu-id="c5850-125">4150</span><span class="sxs-lookup"><span data-stu-id="c5850-125">4150</span></span>    |



 

## <a name="target"></a><span data-ttu-id="c5850-126">Destino</span><span class="sxs-lookup"><span data-stu-id="c5850-126">Target</span></span>

<span data-ttu-id="c5850-127">O campo de destino da [tabela CustomAction](customaction-table.md) contém uma função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="c5850-127">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="c5850-128">O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="c5850-128">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="c5850-129">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="c5850-129">Return Processing Options</span></span>

<span data-ttu-id="c5850-130">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="c5850-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="c5850-131">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c5850-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="c5850-132">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="c5850-132">Execution Scheduling Options</span></span>

<span data-ttu-id="c5850-133">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="c5850-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="c5850-134">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c5850-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="c5850-135">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="c5850-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="c5850-136">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="c5850-136">In-Script Execution Options</span></span>

<span data-ttu-id="c5850-137">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="c5850-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="c5850-138">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5850-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="c5850-139">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="c5850-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="c5850-140">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c5850-140">Return Values</span></span>

<span data-ttu-id="c5850-141">Funções opcionais escritas em script devem retornar um dos valores descritos em [valores de retorno de ações personalizadas JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c5850-141">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5850-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5850-142">Remarks</span></span>

<span data-ttu-id="c5850-143">Uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação.</span><span class="sxs-lookup"><span data-stu-id="c5850-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="c5850-144">O instalador anexa o **objeto de sessão** ao script com a *sessão* de nome.</span><span class="sxs-lookup"><span data-stu-id="c5850-144">The installer attaches the **Session Object** to the script with the name *Session*.</span></span> <span data-ttu-id="c5850-145">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.</span><span class="sxs-lookup"><span data-stu-id="c5850-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5850-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5850-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5850-147">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="c5850-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



