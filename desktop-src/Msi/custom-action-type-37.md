---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 37 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Tipo de ação personalizada 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a42d4837af6fe2878f33624251d9c06550855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011466"
---
# <a name="custom-action-type-37"></a><span data-ttu-id="61746-103">Tipo de ação personalizada 37</span><span class="sxs-lookup"><span data-stu-id="61746-103">Custom Action Type 37</span></span>

<span data-ttu-id="61746-104">Essa ação personalizada é escrita em JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="61746-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="61746-105">Windows Installer não dá suporte a JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="61746-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="61746-106">Para obter mais informações, consulte [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="61746-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="61746-107">Fonte</span><span class="sxs-lookup"><span data-stu-id="61746-107">Source</span></span>

<span data-ttu-id="61746-108">O campo de origem da [tabela CustomAction](customaction-table.md) contém o valor nulo.</span><span class="sxs-lookup"><span data-stu-id="61746-108">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="61746-109">O código de script para a ação personalizada é armazenado como uma cadeia de caracteres de texto de script literal no campo de destino.</span><span class="sxs-lookup"><span data-stu-id="61746-109">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="61746-110">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="61746-110">Type Value</span></span>

<span data-ttu-id="61746-111">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="61746-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="61746-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="61746-112">Constants</span></span>                                                             | <span data-ttu-id="61746-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="61746-113">Hexadecimal</span></span> | <span data-ttu-id="61746-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="61746-114">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="61746-115">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="61746-115">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="61746-116">0x025</span><span class="sxs-lookup"><span data-stu-id="61746-116">0x025</span></span>       | <span data-ttu-id="61746-117">37</span><span class="sxs-lookup"><span data-stu-id="61746-117">37</span></span>      |



 

<span data-ttu-id="61746-118">Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="61746-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="61746-119">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="61746-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="61746-120">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="61746-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="61746-121">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="61746-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="61746-122">Constantes</span><span class="sxs-lookup"><span data-stu-id="61746-122">Constants</span></span>                                                                                                    | <span data-ttu-id="61746-123">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="61746-123">Hexadecimal</span></span> | <span data-ttu-id="61746-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="61746-124">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="61746-125">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="61746-125">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="61746-126">0x0001025</span><span class="sxs-lookup"><span data-stu-id="61746-126">0x0001025</span></span>   | <span data-ttu-id="61746-127">4133</span><span class="sxs-lookup"><span data-stu-id="61746-127">4133</span></span>    |



 

## <a name="target"></a><span data-ttu-id="61746-128">Destino</span><span class="sxs-lookup"><span data-stu-id="61746-128">Target</span></span>

<span data-ttu-id="61746-129">O campo de destino da [tabela CustomAction](customaction-table.md) contém o código de script para a ação personalizada como uma cadeia de caracteres de texto de script literal.</span><span class="sxs-lookup"><span data-stu-id="61746-129">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="61746-130">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="61746-130">Return Processing Options</span></span>

<span data-ttu-id="61746-131">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="61746-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="61746-132">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="61746-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="61746-133">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="61746-133">Execution Scheduling Options</span></span>

<span data-ttu-id="61746-134">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="61746-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="61746-135">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="61746-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="61746-136">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="61746-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="61746-137">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="61746-137">In-Script Execution Options</span></span>

<span data-ttu-id="61746-138">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="61746-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="61746-139">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="61746-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="61746-140">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="61746-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="61746-141">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="61746-141">Return Values</span></span>

<span data-ttu-id="61746-142">Esse tipo de ação personalizada sempre retorna êxito.</span><span class="sxs-lookup"><span data-stu-id="61746-142">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="61746-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="61746-143">Remarks</span></span>

<span data-ttu-id="61746-144">Uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação.</span><span class="sxs-lookup"><span data-stu-id="61746-144">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="61746-145">O instalador anexa o **objeto de sessão** ao script com o nome "Session".</span><span class="sxs-lookup"><span data-stu-id="61746-145">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="61746-146">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.</span><span class="sxs-lookup"><span data-stu-id="61746-146">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61746-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61746-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61746-148">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="61746-148">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



