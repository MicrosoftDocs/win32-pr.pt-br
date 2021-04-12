---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 17 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo de ação personalizada 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297449"
---
# <a name="custom-action-type-17"></a><span data-ttu-id="c22b6-103">Tipo de ação personalizada 17</span><span class="sxs-lookup"><span data-stu-id="c22b6-103">Custom Action Type 17</span></span>

<span data-ttu-id="c22b6-104">Essa ação personalizada chama uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.</span><span class="sxs-lookup"><span data-stu-id="c22b6-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="c22b6-105">Fonte</span><span class="sxs-lookup"><span data-stu-id="c22b6-105">Source</span></span>

<span data-ttu-id="c22b6-106">A DLL é instalada com o aplicativo durante a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="c22b6-106">The DLL is installed with the application during the current session.</span></span> <span data-ttu-id="c22b6-107">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="c22b6-108">O local do código de ação personalizado é determinado pela resolução do caminho de destino para esse arquivo; Portanto, essa ação personalizada deve ser chamada depois que o arquivo tiver sido instalado e antes de ser removido.</span><span class="sxs-lookup"><span data-stu-id="c22b6-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after that file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="c22b6-109">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="c22b6-109">Type Value</span></span>

<span data-ttu-id="c22b6-110">Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="c22b6-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="c22b6-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="c22b6-111">Constants</span></span>                                                          | <span data-ttu-id="c22b6-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c22b6-112">Hexadecimal</span></span> | <span data-ttu-id="c22b6-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="c22b6-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="c22b6-114">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="c22b6-114">**msidbCustomActionTypeDll** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="c22b6-115">0x011</span><span class="sxs-lookup"><span data-stu-id="c22b6-115">0x011</span></span>       | <span data-ttu-id="c22b6-116">17</span><span class="sxs-lookup"><span data-stu-id="c22b6-116">17</span></span>      |



 

## <a name="target"></a><span data-ttu-id="c22b6-117">Destino</span><span class="sxs-lookup"><span data-stu-id="c22b6-117">Target</span></span>

<span data-ttu-id="c22b6-118">A DLL é chamada por meio do ponto de entrada nomeado no campo de destino da [tabela CustomAction](customaction-table.md), passando um único argumento que é o identificador para a sessão de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="c22b6-118">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="c22b6-119">O nome do ponto de entrada especificado na tabela deve corresponder ao exportado da DLL.</span><span class="sxs-lookup"><span data-stu-id="c22b6-119">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="c22b6-120">Observe que, se a função de entrada não for especificada por um. Arquivo DEF ou por uma especificação/EXPORT: linker, o nome pode ter um sublinhado à esquerda e um @4 sufixo "".</span><span class="sxs-lookup"><span data-stu-id="c22b6-120">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="c22b6-121">A função chamada deve especificar a \_ \_ Convenção de chamada stdcall.</span><span class="sxs-lookup"><span data-stu-id="c22b6-121">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="c22b6-122">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="c22b6-122">Return Processing Options</span></span>

<span data-ttu-id="c22b6-123">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="c22b6-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="c22b6-124">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="c22b6-125">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="c22b6-125">Execution Scheduling Options</span></span>

<span data-ttu-id="c22b6-126">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="c22b6-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="c22b6-127">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c22b6-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="c22b6-128">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="c22b6-129">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="c22b6-129">In-Script Execution Options</span></span>

<span data-ttu-id="c22b6-130">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="c22b6-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="c22b6-131">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="c22b6-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="c22b6-132">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="c22b6-133">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c22b6-133">Return Values</span></span>

<span data-ttu-id="c22b6-134">Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-134">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c22b6-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="c22b6-135">Remarks</span></span>

<span data-ttu-id="c22b6-136">Uma ação personalizada que chama uma DLL (biblioteca de vínculo dinâmico) requer um identificador para a sessão de instalação.</span><span class="sxs-lookup"><span data-stu-id="c22b6-136">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="c22b6-137">Se essa for também uma ação personalizada de execução adiada, a sessão poderá não existir mais durante a execução do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="c22b6-137">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="c22b6-138">Para obter informações sobre como uma ação personalizada desse tipo pode obter informações de contexto, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-138">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="c22b6-139">As ações personalizadas são executadas em um thread separado e podem ter acesso limitado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="c22b6-139">Custom actions execute in a separate thread, and may have limited access to the system.</span></span> <span data-ttu-id="c22b6-140">As ações personalizadas que são executadas de modo assíncrono bloqueiam o thread principal no término da sequência atual ou da sessão de instalação até que eles sejam retornados.</span><span class="sxs-lookup"><span data-stu-id="c22b6-140">Custom actions that run asynchronously block the main thread at the termination of either the current sequence or the install session until they return.</span></span>

<span data-ttu-id="c22b6-141">As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 17 (DLL), devem aderir às seguintes restrições de sequenciamento:</span><span class="sxs-lookup"><span data-stu-id="c22b6-141">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="c22b6-142">A ação personalizada deve ser sequenciada após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-142">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="c22b6-143">Isso é para que a ação personalizada possa resolver o caminho necessário para localizar a DLL.</span><span class="sxs-lookup"><span data-stu-id="c22b6-143">This is so that the custom action can resolve the path needed to locate the DLL.</span></span>
-   <span data-ttu-id="c22b6-144">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) desse tipo deverão ser sequenciadas após a [ação InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-144">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="c22b6-145">Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas não adiadas desse tipo deverão ser sequenciadas após a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="c22b6-145">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c22b6-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c22b6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c22b6-147">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="c22b6-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c22b6-148">Ações personalizadas de execução adiada</span><span class="sxs-lookup"><span data-stu-id="c22b6-148">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c22b6-149">Bibliotecas de vínculo dinâmico</span><span class="sxs-lookup"><span data-stu-id="c22b6-149">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> </dl>

 

 



