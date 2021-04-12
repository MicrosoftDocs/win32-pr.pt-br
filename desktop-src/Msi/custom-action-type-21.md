---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 21 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Tipo de ação personalizada 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297448"
---
# <a name="custom-action-type-21"></a><span data-ttu-id="3940a-103">Tipo de ação personalizada 21</span><span class="sxs-lookup"><span data-stu-id="3940a-103">Custom Action Type 21</span></span>

<span data-ttu-id="3940a-104">Essa ação personalizada é escrita em JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="3940a-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="3940a-105">Windows Installer não dá suporte a JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="3940a-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="3940a-106">Para obter mais informações, consulte [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="3940a-107">Fonte</span><span class="sxs-lookup"><span data-stu-id="3940a-107">Source</span></span>

<span data-ttu-id="3940a-108">O script é instalado com o aplicativo durante a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="3940a-108">The script is installed with the application during the current session.</span></span> <span data-ttu-id="3940a-109">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="3940a-110">O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; Portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.</span><span class="sxs-lookup"><span data-stu-id="3940a-110">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="3940a-111">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="3940a-111">Type Value</span></span>

<span data-ttu-id="3940a-112">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3940a-112">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="3940a-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="3940a-113">Constants</span></span>                                                              | <span data-ttu-id="3940a-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3940a-114">Hexadecimal</span></span> | <span data-ttu-id="3940a-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="3940a-115">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3940a-116">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="3940a-116">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="3940a-117">0x015</span><span class="sxs-lookup"><span data-stu-id="3940a-117">0x015</span></span>       | <span data-ttu-id="3940a-118">21</span><span class="sxs-lookup"><span data-stu-id="3940a-118">21</span></span>      |



 

<span data-ttu-id="3940a-119">Windows Installer pode usar [ações personalizadas de 64 bits](64-bit-custom-actions.md) em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3940a-119">Windows Installer may use [64-bit Custom Actions](64-bit-custom-actions.md) on 64-bit operating systems.</span></span> <span data-ttu-id="3940a-120">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="3940a-120">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="3940a-121">Para obter informações, consulte ações personalizadas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3940a-121">For information see 64-bit Custom Actions.</span></span> <span data-ttu-id="3940a-122">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3940a-122">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="3940a-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="3940a-123">Constants</span></span>                                                                                                     | <span data-ttu-id="3940a-124">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3940a-124">Hexadecimal</span></span> | <span data-ttu-id="3940a-125">Decimal</span><span class="sxs-lookup"><span data-stu-id="3940a-125">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3940a-126">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="3940a-126">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="3940a-127">0x0001015</span><span class="sxs-lookup"><span data-stu-id="3940a-127">0x0001015</span></span>   | <span data-ttu-id="3940a-128">4117</span><span class="sxs-lookup"><span data-stu-id="3940a-128">4117</span></span>    |



 

## <a name="target"></a><span data-ttu-id="3940a-129">Destino</span><span class="sxs-lookup"><span data-stu-id="3940a-129">Target</span></span>

<span data-ttu-id="3940a-130">O campo de destino da [tabela CustomAction](customaction-table.md) contém uma função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="3940a-130">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="3940a-131">O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="3940a-131">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="3940a-132">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="3940a-132">Return Processing Options</span></span>

<span data-ttu-id="3940a-133">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="3940a-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="3940a-134">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-134">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="3940a-135">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="3940a-135">Execution Scheduling Options</span></span>

<span data-ttu-id="3940a-136">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="3940a-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="3940a-137">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3940a-137">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="3940a-138">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-138">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="3940a-139">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="3940a-139">In-Script Execution Options</span></span>

<span data-ttu-id="3940a-140">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="3940a-140">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="3940a-141">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="3940a-141">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="3940a-142">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-142">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="3940a-143">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3940a-143">Return Values</span></span>

<span data-ttu-id="3940a-144">Funções opcionais escritas em script devem retornar um dos valores descritos em [valores de retorno de ações personalizadas JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-144">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3940a-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="3940a-145">Remarks</span></span>

<span data-ttu-id="3940a-146">Uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação.</span><span class="sxs-lookup"><span data-stu-id="3940a-146">A custom action that is written in JScript or VBScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="3940a-147">O instalador anexa o **objeto de sessão** ao script com o nome "Session".</span><span class="sxs-lookup"><span data-stu-id="3940a-147">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="3940a-148">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.</span><span class="sxs-lookup"><span data-stu-id="3940a-148">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="3940a-149">As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 21 (JScript), devem aderir às seguintes restrições de sequenciamento:</span><span class="sxs-lookup"><span data-stu-id="3940a-149">Custom actions that reference an installed file as their source, such as Custom Action Type 21 (JScript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="3940a-150">A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-150">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="3940a-151">Isso é para que a ação personalizada possa resolver o caminho necessário para localizar o arquivo de origem que contém o JScript.</span><span class="sxs-lookup"><span data-stu-id="3940a-151">This is so that the custom action can resolve the path needed to locate the source file containing the JScript.</span></span>
-   <span data-ttu-id="3940a-152">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-152">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="3940a-153">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3940a-153">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3940a-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3940a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3940a-155">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="3940a-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



