---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 18 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Tipo de ação personalizada 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922693"
---
# <a name="custom-action-type-18"></a><span data-ttu-id="fa10f-103">Tipo de ação personalizada 18</span><span class="sxs-lookup"><span data-stu-id="fa10f-103">Custom Action Type 18</span></span>

<span data-ttu-id="fa10f-104">Essa ação personalizada chama um executável iniciado com uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="fa10f-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="fa10f-105">Fonte</span><span class="sxs-lookup"><span data-stu-id="fa10f-105">Source</span></span>

<span data-ttu-id="fa10f-106">O executável é gerado a partir de um arquivo instalado com o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa10f-106">The executable is generated from a file installed with the application.</span></span> <span data-ttu-id="fa10f-107">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="fa10f-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="fa10f-108">O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; Portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.</span><span class="sxs-lookup"><span data-stu-id="fa10f-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="fa10f-109">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="fa10f-109">Type Value</span></span>

<span data-ttu-id="fa10f-110">Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="fa10f-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="fa10f-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="fa10f-111">Constants</span></span>                                                          | <span data-ttu-id="fa10f-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="fa10f-112">Hexadecimal</span></span> | <span data-ttu-id="fa10f-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="fa10f-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="fa10f-114">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="fa10f-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="fa10f-115">0x012</span><span class="sxs-lookup"><span data-stu-id="fa10f-115">0x012</span></span>       | <span data-ttu-id="fa10f-116">18</span><span class="sxs-lookup"><span data-stu-id="fa10f-116">18</span></span>      |



 

## <a name="target"></a><span data-ttu-id="fa10f-117">Destino</span><span class="sxs-lookup"><span data-stu-id="fa10f-117">Target</span></span>

<span data-ttu-id="fa10f-118">A coluna de destino da [tabela CustomAction](customaction-table.md) contém a cadeia de caracteres de linha de comando para o executável identificado na coluna de origem.</span><span class="sxs-lookup"><span data-stu-id="fa10f-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="fa10f-119">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="fa10f-119">Return Processing Options</span></span>

<span data-ttu-id="fa10f-120">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="fa10f-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="fa10f-121">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="fa10f-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="fa10f-122">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="fa10f-122">Execution Scheduling Options</span></span>

<span data-ttu-id="fa10f-123">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="fa10f-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="fa10f-124">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fa10f-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="fa10f-125">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="fa10f-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="fa10f-126">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="fa10f-126">In-Script Execution Options</span></span>

<span data-ttu-id="fa10f-127">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="fa10f-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="fa10f-128">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="fa10f-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="fa10f-129">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="fa10f-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="fa10f-130">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="fa10f-130">Return Values</span></span>

<span data-ttu-id="fa10f-131">As ações personalizadas que são [arquivos executáveis](executable-files.md) devem retornar um valor de 0 para êxito.</span><span class="sxs-lookup"><span data-stu-id="fa10f-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="fa10f-132">O instalador interpreta qualquer outro valor de retorno como falha.</span><span class="sxs-lookup"><span data-stu-id="fa10f-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="fa10f-133">Para ignorar valores de retorno, defina o sinalizador de bit **msidbCustomActionTypeContinue** no campo Type da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="fa10f-133">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa10f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa10f-134">Remarks</span></span>

<span data-ttu-id="fa10f-135">Uma ação personalizada que inicia um executável usa uma linha de comando, que normalmente contém propriedades que são designadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fa10f-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="fa10f-136">Se essa for também uma [ação personalizada de execução adiada](deferred-execution-custom-actions.md), o instalador usará [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para criar o processo quando a ação personalizada for invocada a partir do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="fa10f-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="fa10f-137">As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 18 (EXE), devem aderir às seguintes restrições de sequenciamento:</span><span class="sxs-lookup"><span data-stu-id="fa10f-137">Custom actions that reference an installed file as their source, such as Custom Action Type 18 (EXE), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="fa10f-138">A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="fa10f-138">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="fa10f-139">Isso é para que a ação personalizada possa resolver o caminho necessário para localizar o EXE.</span><span class="sxs-lookup"><span data-stu-id="fa10f-139">This is so that the custom action can resolve the path needed to locate the EXE.</span></span>
-   <span data-ttu-id="fa10f-140">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="fa10f-140">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="fa10f-141">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="fa10f-141">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa10f-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa10f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa10f-143">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="fa10f-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="fa10f-144">Arquivos executáveis</span><span class="sxs-lookup"><span data-stu-id="fa10f-144">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
