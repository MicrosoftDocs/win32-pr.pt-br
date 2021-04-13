---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 22 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Tipo de ação personalizada 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00b4772b1d2532c0291223cc5c4b6a63ead9324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297775"
---
# <a name="custom-action-type-22"></a><span data-ttu-id="0417d-103">Tipo de ação personalizada 22</span><span class="sxs-lookup"><span data-stu-id="0417d-103">Custom Action Type 22</span></span>

<span data-ttu-id="0417d-104">Essa ação personalizada é escrita em VBScript.</span><span class="sxs-lookup"><span data-stu-id="0417d-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="0417d-105">Consulte também [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="0417d-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="0417d-106">Source</span></span>

<span data-ttu-id="0417d-107">O script é instalado com o aplicativo durante a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="0417d-107">The script is installed with the application during the current session.</span></span> <span data-ttu-id="0417d-108">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="0417d-109">O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; Portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.</span><span class="sxs-lookup"><span data-stu-id="0417d-109">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="0417d-110">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="0417d-110">Type Value</span></span>

<span data-ttu-id="0417d-111">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0417d-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="0417d-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="0417d-112">Constants</span></span>                                                               | <span data-ttu-id="0417d-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="0417d-113">Hexadecimal</span></span> | <span data-ttu-id="0417d-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="0417d-114">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="0417d-115">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="0417d-115">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="0417d-116">0x016</span><span class="sxs-lookup"><span data-stu-id="0417d-116">0x016</span></span>       | <span data-ttu-id="0417d-117">22</span><span class="sxs-lookup"><span data-stu-id="0417d-117">22</span></span>      |



 

<span data-ttu-id="0417d-118">Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0417d-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="0417d-119">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="0417d-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="0417d-120">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="0417d-121">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0417d-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="0417d-122">Constantes</span><span class="sxs-lookup"><span data-stu-id="0417d-122">Constants</span></span>                                                                                                      | <span data-ttu-id="0417d-123">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="0417d-123">Hexadecimal</span></span> | <span data-ttu-id="0417d-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="0417d-124">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="0417d-125">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="0417d-125">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="0417d-126">0x0001016</span><span class="sxs-lookup"><span data-stu-id="0417d-126">0x0001016</span></span>   | <span data-ttu-id="0417d-127">4118</span><span class="sxs-lookup"><span data-stu-id="0417d-127">4118</span></span>    |



 

## <a name="target"></a><span data-ttu-id="0417d-128">Destino</span><span class="sxs-lookup"><span data-stu-id="0417d-128">Target</span></span>

<span data-ttu-id="0417d-129">O campo de destino da [tabela CustomAction](customaction-table.md) contém uma função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="0417d-129">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="0417d-130">O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="0417d-130">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="0417d-131">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="0417d-131">Return Processing Options</span></span>

<span data-ttu-id="0417d-132">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="0417d-132">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="0417d-133">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-133">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="0417d-134">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="0417d-134">Execution Scheduling Options</span></span>

<span data-ttu-id="0417d-135">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="0417d-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="0417d-136">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="0417d-136">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="0417d-137">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-137">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="0417d-138">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="0417d-138">In-Script Execution Options</span></span>

<span data-ttu-id="0417d-139">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="0417d-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="0417d-140">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="0417d-140">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="0417d-141">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-141">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="0417d-142">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="0417d-142">Return Values</span></span>

<span data-ttu-id="0417d-143">Funções opcionais escritas em script devem retornar um dos valores descritos em [valores de retorno de ações personalizadas JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-143">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0417d-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="0417d-144">Remarks</span></span>

<span data-ttu-id="0417d-145">Uma ação personalizada escrita em JScript ou VBScript requer o [**objeto de sessão**](session-object.md)de instalação.</span><span class="sxs-lookup"><span data-stu-id="0417d-145">A custom action that is written in JScript or VBScript requires the install [**Session Object**](session-object.md).</span></span> <span data-ttu-id="0417d-146">Esse é o objeto de **sessão** de tipo e o instalador o anexa ao script com o nome "Session".</span><span class="sxs-lookup"><span data-stu-id="0417d-146">This is of the type **Session Object** and the installer attaches it to the script with the name "Session".</span></span> <span data-ttu-id="0417d-147">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.</span><span class="sxs-lookup"><span data-stu-id="0417d-147">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="0417d-148">As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 22 (VBcript), devem aderir às seguintes restrições de sequenciamento:</span><span class="sxs-lookup"><span data-stu-id="0417d-148">Custom actions that reference an installed file as their source, such as Custom Action Type 22 (VBcript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="0417d-149">A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-149">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="0417d-150">Isso é para que a ação personalizada possa resolver o caminho necessário para localizar o arquivo de origem que contém o VBScript.</span><span class="sxs-lookup"><span data-stu-id="0417d-150">This is so that the custom action can resolve the path needed to locate the source file containing the VBScript.</span></span>
-   <span data-ttu-id="0417d-151">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-151">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="0417d-152">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0417d-152">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0417d-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0417d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0417d-154">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="0417d-154">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



