---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 6 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Tipo de ação personalizada 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747556"
---
# <a name="custom-action-type-6"></a><span data-ttu-id="48255-103">Tipo de ação personalizada 6</span><span class="sxs-lookup"><span data-stu-id="48255-103">Custom Action Type 6</span></span>

<span data-ttu-id="48255-104">Essa ação personalizada é escrita em VBScript.</span><span class="sxs-lookup"><span data-stu-id="48255-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="48255-105">Para obter mais informações, consulte [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="48255-105">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="48255-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="48255-106">Source</span></span>

<span data-ttu-id="48255-107">O script é gerado a partir de um fluxo binário temporário.</span><span class="sxs-lookup"><span data-stu-id="48255-107">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="48255-108">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela binária](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="48255-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="48255-109">A coluna de dados na tabela binária contém os dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="48255-109">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="48255-110">Um fluxo separado é alocado para cada linha.</span><span class="sxs-lookup"><span data-stu-id="48255-110">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="48255-111">Novos dados binários podem ser inseridos de um arquivo usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido por [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na tabela.</span><span class="sxs-lookup"><span data-stu-id="48255-111">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="48255-112">Quando a ação personalizada é invocada, os dados de fluxo são copiados em um arquivo temporário, que é processado dependendo do tipo de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="48255-112">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="48255-113">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="48255-113">Type Value</span></span>

<span data-ttu-id="48255-114">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48255-114">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="48255-115">Constantes</span><span class="sxs-lookup"><span data-stu-id="48255-115">Constants</span></span>                                                               | <span data-ttu-id="48255-116">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="48255-116">Hexadecimal</span></span> | <span data-ttu-id="48255-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="48255-117">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="48255-118">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="48255-118">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="48255-119">0x006</span><span class="sxs-lookup"><span data-stu-id="48255-119">0x006</span></span>       | <span data-ttu-id="48255-120">6</span><span class="sxs-lookup"><span data-stu-id="48255-120">6</span></span>       |



 

<span data-ttu-id="48255-121">Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="48255-121">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="48255-122">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="48255-122">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="48255-123">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="48255-123">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="48255-124">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="48255-124">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="48255-125">Constantes</span><span class="sxs-lookup"><span data-stu-id="48255-125">Constants</span></span>                                                                                                      | <span data-ttu-id="48255-126">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="48255-126">Hexadecimal</span></span> | <span data-ttu-id="48255-127">Decimal</span><span class="sxs-lookup"><span data-stu-id="48255-127">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="48255-128">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="48255-128">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="48255-129">0x0001006</span><span class="sxs-lookup"><span data-stu-id="48255-129">0x0001006</span></span>   | <span data-ttu-id="48255-130">4102</span><span class="sxs-lookup"><span data-stu-id="48255-130">4102</span></span>    |



 

## <a name="target"></a><span data-ttu-id="48255-131">Destino</span><span class="sxs-lookup"><span data-stu-id="48255-131">Target</span></span>

<span data-ttu-id="48255-132">O campo de destino da [tabela CustomAction](customaction-table.md) contém uma função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="48255-132">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="48255-133">O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="48255-133">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="48255-134">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="48255-134">Return Processing Options</span></span>

<span data-ttu-id="48255-135">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="48255-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="48255-136">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="48255-136">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="48255-137">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="48255-137">Execution Scheduling Options</span></span>

<span data-ttu-id="48255-138">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="48255-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="48255-139">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="48255-139">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="48255-140">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="48255-140">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="48255-141">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="48255-141">In-Script Execution Options</span></span>

<span data-ttu-id="48255-142">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="48255-142">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="48255-143">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="48255-143">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="48255-144">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="48255-144">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="48255-145">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="48255-145">Return Values</span></span>

<span data-ttu-id="48255-146">Funções opcionais escritas em script devem retornar um dos valores descritos em [valores de retorno de ações personalizadas JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="48255-146">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="48255-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="48255-147">Remarks</span></span>

<span data-ttu-id="48255-148">Uma ação personalizada escrita em JScript ou VBScript requer a instalação do [**objeto de sessão**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="48255-148">A custom action that is written in JScript or VBScript requires the installation of the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="48255-149">O instalador anexa o objeto de **sessão** ao script com a *sessão* de nome.</span><span class="sxs-lookup"><span data-stu-id="48255-149">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="48255-150">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.</span><span class="sxs-lookup"><span data-stu-id="48255-150">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="48255-151">Quando uma tabela de banco de dados é exportada, cada fluxo é gravado como um arquivo separado na subpasta nomeada após a tabela, usando a chave primária como o nome do arquivo (coluna de nome para a tabela binária), com uma extensão padrão de ". IBD".</span><span class="sxs-lookup"><span data-stu-id="48255-151">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="48255-152">O nome deve usar o formato de nome de arquivo 8,3 se o sistema de arquivos ou o sistema de controle de versão não oferecer suporte a nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="48255-152">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="48255-153">O arquivo morto persistente substitui os dados de fluxo pelo nome de arquivo usado, para que os dados possam ser localizados quando a tabela for importada.</span><span class="sxs-lookup"><span data-stu-id="48255-153">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48255-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48255-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48255-155">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="48255-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



