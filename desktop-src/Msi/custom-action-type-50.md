---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 50 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Tipo de ação personalizada 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747341"
---
# <a name="custom-action-type-50"></a><span data-ttu-id="8b133-103">Tipo de ação personalizada 50</span><span class="sxs-lookup"><span data-stu-id="8b133-103">Custom Action Type 50</span></span>

<span data-ttu-id="8b133-104">Essa ação personalizada chama um executável iniciado com uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="8b133-104">This custom action calls an executable launched with a command line.</span></span>

<span data-ttu-id="8b133-105">Consulte também [arquivos executáveis](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="8b133-105">See also [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="8b133-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="8b133-106">Source</span></span>

<span data-ttu-id="8b133-107">O executável é gerado a partir de um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="8b133-107">The executable is generated from an existing file.</span></span> <span data-ttu-id="8b133-108">O campo Source da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de propriedades](property-table.md) de uma propriedade que contém o caminho completo para o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="8b133-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Property table](property-table.md) for a property that contains the full path to the executable file.</span></span>

## <a name="type-value"></a><span data-ttu-id="8b133-109">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="8b133-109">Type Value</span></span>

<span data-ttu-id="8b133-110">Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="8b133-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="8b133-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="8b133-111">Constants</span></span>                                                        | <span data-ttu-id="8b133-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8b133-112">Hexadecimal</span></span> | <span data-ttu-id="8b133-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="8b133-113">Decimal</span></span> |
|------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="8b133-114">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="8b133-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="8b133-115">0x032</span><span class="sxs-lookup"><span data-stu-id="8b133-115">0x032</span></span>       | <span data-ttu-id="8b133-116">50</span><span class="sxs-lookup"><span data-stu-id="8b133-116">50</span></span>      |



 

## <a name="target"></a><span data-ttu-id="8b133-117">Destino</span><span class="sxs-lookup"><span data-stu-id="8b133-117">Target</span></span>

<span data-ttu-id="8b133-118">A coluna de destino da [tabela CustomAction](customaction-table.md) contém a cadeia de caracteres de linha de comando para o executável identificado na coluna de origem.</span><span class="sxs-lookup"><span data-stu-id="8b133-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="8b133-119">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="8b133-119">Return Processing Options</span></span>

<span data-ttu-id="8b133-120">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="8b133-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="8b133-121">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="8b133-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="8b133-122">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="8b133-122">Execution Scheduling Options</span></span>

<span data-ttu-id="8b133-123">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="8b133-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="8b133-124">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8b133-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="8b133-125">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="8b133-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="8b133-126">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="8b133-126">In-Script Execution Options</span></span>

<span data-ttu-id="8b133-127">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="8b133-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="8b133-128">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="8b133-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="8b133-129">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="8b133-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="8b133-130">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8b133-130">Return Values</span></span>

<span data-ttu-id="8b133-131">As ações personalizadas que são [arquivos executáveis](executable-files.md) devem retornar um valor de 0 para êxito.</span><span class="sxs-lookup"><span data-stu-id="8b133-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="8b133-132">O instalador interpreta qualquer outro valor de retorno como falha.</span><span class="sxs-lookup"><span data-stu-id="8b133-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="8b133-133">Para ignorar valores de retorno, defina o sinalizador de bit **msidbCustomActionTypeContinue** no campo Type da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="8b133-133">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b133-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b133-134">Remarks</span></span>

<span data-ttu-id="8b133-135">Uma ação personalizada que inicia um executável usa uma linha de comando, que normalmente contém propriedades que são designadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8b133-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="8b133-136">Se essa for também uma [ação personalizada de execução adiada](deferred-execution-custom-actions.md), o instalador usará CreateProcessAsUser ou CreateProcess para criar o processo quando a ação personalizada for invocada a partir do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="8b133-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses CreateProcessAsUser or CreateProcess to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b133-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b133-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b133-138">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="8b133-138">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



