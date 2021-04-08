---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 51 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Tipo de ação personalizada 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922332"
---
# <a name="custom-action-type-51"></a><span data-ttu-id="fe042-103">Tipo de ação personalizada 51</span><span class="sxs-lookup"><span data-stu-id="fe042-103">Custom Action Type 51</span></span>

<span data-ttu-id="fe042-104">Essa ação personalizada define uma propriedade de uma cadeia de caracteres de texto formatado.</span><span class="sxs-lookup"><span data-stu-id="fe042-104">This custom action sets a property from a formatted text string.</span></span>

<span data-ttu-id="fe042-105">Para afetar uma propriedade usada em uma condição em um componente ou recurso, a ação personalizada deve vir antes da [ação CostFinalize](costfinalize-action.md) na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="fe042-105">To affect a property used in a condition on a component or feature, the custom action must come before the [CostFinalize action](costfinalize-action.md) in the action sequence.</span></span>

## <a name="source"></a><span data-ttu-id="fe042-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="fe042-106">Source</span></span>

<span data-ttu-id="fe042-107">O campo de origem da [tabela CustomAction](customaction-table.md) pode conter o nome de uma propriedade ou uma chave para a [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="fe042-107">The Source field of the [CustomAction table](customaction-table.md) can contain either the name of a property or a key to the [Property table](property-table.md).</span></span> <span data-ttu-id="fe042-108">Essa propriedade é definida pela cadeia de caracteres formatada no campo de destino usando [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span><span class="sxs-lookup"><span data-stu-id="fe042-108">This property is set by the formatted string in the Target field using [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span></span>

## <a name="type-value"></a><span data-ttu-id="fe042-109">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="fe042-109">Type Value</span></span>

<span data-ttu-id="fe042-110">Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="fe042-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="fe042-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="fe042-111">Constants</span></span>                                                             | <span data-ttu-id="fe042-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="fe042-112">Hexadecimal</span></span> | <span data-ttu-id="fe042-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="fe042-113">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="fe042-114">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="fe042-114">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="fe042-115">0x033</span><span class="sxs-lookup"><span data-stu-id="fe042-115">0x033</span></span>       | <span data-ttu-id="fe042-116">51</span><span class="sxs-lookup"><span data-stu-id="fe042-116">51</span></span>      |



 

## <a name="target"></a><span data-ttu-id="fe042-117">Destino</span><span class="sxs-lookup"><span data-stu-id="fe042-117">Target</span></span>

<span data-ttu-id="fe042-118">A coluna Target da [tabela CustomAction](customaction-table.md) contém uma cadeia de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico).</span><span class="sxs-lookup"><span data-stu-id="fe042-118">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="fe042-119">Os parâmetros a serem substituídos são colocados entre colchetes, \[ ... \] e podem ser Propriedades, variáveis de ambiente (% Prefix), caminhos de arquivo ( \# prefixo) ou caminhos de diretório de componente ($ Prefix).</span><span class="sxs-lookup"><span data-stu-id="fe042-119">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="fe042-120">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="fe042-120">Return Processing Options</span></span>

<span data-ttu-id="fe042-121">A ação personalizada não usa essas opções.</span><span class="sxs-lookup"><span data-stu-id="fe042-121">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="fe042-122">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="fe042-122">Execution Scheduling Options</span></span>

<span data-ttu-id="fe042-123">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="fe042-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="fe042-124">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fe042-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="fe042-125">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="fe042-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="fe042-126">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="fe042-126">In-Script Execution Options</span></span>

<span data-ttu-id="fe042-127">A ação personalizada não usa essas opções.</span><span class="sxs-lookup"><span data-stu-id="fe042-127">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="fe042-128">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="fe042-128">Return Values</span></span>

<span data-ttu-id="fe042-129">Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fe042-129">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe042-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe042-130">Remarks</span></span>

<span data-ttu-id="fe042-131">Se você definir uma [propriedade privada](private-properties.md) na sequência da interface do usuário criando uma ação personalizada em uma das tabelas de sequência da interface do usuário, essa propriedade não será definida na sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="fe042-131">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="fe042-132">Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="fe042-132">To set the property in the execution sequence, you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="fe042-133">Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na [**Propriedade SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="fe042-133">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe042-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe042-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe042-135">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="fe042-135">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="fe042-136">Ações personalizadas de texto formatado</span><span class="sxs-lookup"><span data-stu-id="fe042-136">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



