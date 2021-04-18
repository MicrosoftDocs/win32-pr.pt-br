---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 5 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Tipo de ação personalizada 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85460c9a41dca060ca2634c013999c2c340ddfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770379"
---
# <a name="custom-action-type-5"></a><span data-ttu-id="c9949-103">Tipo de ação personalizada 5</span><span class="sxs-lookup"><span data-stu-id="c9949-103">Custom Action Type 5</span></span>

<span data-ttu-id="c9949-104">Essa ação personalizada é escrita em JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="c9949-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="c9949-105">Windows Installer não dá suporte a JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="c9949-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="c9949-106">Para obter mais informações, consulte [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="c9949-107">Fonte</span><span class="sxs-lookup"><span data-stu-id="c9949-107">Source</span></span>

<span data-ttu-id="c9949-108">O script é gerado a partir de um fluxo binário temporário.</span><span class="sxs-lookup"><span data-stu-id="c9949-108">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="c9949-109">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela binária](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="c9949-110">A coluna de dados na tabela binária contém os dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c9949-110">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="c9949-111">Um fluxo separado é alocado para cada linha.</span><span class="sxs-lookup"><span data-stu-id="c9949-111">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="c9949-112">Novos dados binários podem ser inseridos de um arquivo usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido por [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na tabela.</span><span class="sxs-lookup"><span data-stu-id="c9949-112">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="c9949-113">Quando a ação personalizada é invocada, os dados de fluxo são copiados em um arquivo temporário, que é processado de acordo com o tipo de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="c9949-113">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed according to the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="c9949-114">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="c9949-114">Type Value</span></span>

<span data-ttu-id="c9949-115">Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de ação personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c9949-115">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of 32-bit custom action.</span></span>



| <span data-ttu-id="c9949-116">Constantes</span><span class="sxs-lookup"><span data-stu-id="c9949-116">Constants</span></span>                                                              | <span data-ttu-id="c9949-117">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c9949-117">Hexadecimal</span></span> | <span data-ttu-id="c9949-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="c9949-118">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="c9949-119">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="c9949-119">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="c9949-120">0x05</span><span class="sxs-lookup"><span data-stu-id="c9949-120">0x05</span></span>        | <span data-ttu-id="c9949-121">5</span><span class="sxs-lookup"><span data-stu-id="c9949-121">5</span></span>       |



 

<span data-ttu-id="c9949-122">Windows Installer pode usar ações personalizadas de 64 bits em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c9949-122">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="c9949-123">Uma ação personalizada de 64 bits baseada em scripts deve incluir o bit **msidbCustomActionType64BitScript** em seu tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="c9949-123">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="c9949-124">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-124">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="c9949-125">Inclua o seguinte valor na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico de uma ação personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c9949-125">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="c9949-126">Constantes</span><span class="sxs-lookup"><span data-stu-id="c9949-126">Constants</span></span>                                                                                                     | <span data-ttu-id="c9949-127">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c9949-127">Hexadecimal</span></span> | <span data-ttu-id="c9949-128">Decimal</span><span class="sxs-lookup"><span data-stu-id="c9949-128">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="c9949-129">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="c9949-129">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="c9949-130">0x0001005</span><span class="sxs-lookup"><span data-stu-id="c9949-130">0x0001005</span></span>   | <span data-ttu-id="c9949-131">4101</span><span class="sxs-lookup"><span data-stu-id="c9949-131">4101</span></span>    |



 

## <a name="target"></a><span data-ttu-id="c9949-132">Destino</span><span class="sxs-lookup"><span data-stu-id="c9949-132">Target</span></span>

<span data-ttu-id="c9949-133">O campo de destino da [tabela CustomAction](customaction-table.md) contém uma função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="c9949-133">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="c9949-134">O processamento primeiro envia o script para análise e, em seguida, chama a função de script opcional.</span><span class="sxs-lookup"><span data-stu-id="c9949-134">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="c9949-135">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="c9949-135">Return Processing Options</span></span>

<span data-ttu-id="c9949-136">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="c9949-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="c9949-137">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-137">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="c9949-138">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="c9949-138">Execution Scheduling Options</span></span>

<span data-ttu-id="c9949-139">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="c9949-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="c9949-140">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c9949-140">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="c9949-141">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-141">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="c9949-142">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="c9949-142">In-Script Execution Options</span></span>

<span data-ttu-id="c9949-143">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="c9949-143">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="c9949-144">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="c9949-144">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="c9949-145">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-145">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="c9949-146">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c9949-146">Return Values</span></span>

<span data-ttu-id="c9949-147">Funções opcionais escritas em script devem retornar um dos valores descritos em [valores de retorno de ações personalizadas JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-147">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9949-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9949-148">Remarks</span></span>

<span data-ttu-id="c9949-149">Uma ação personalizada escrita em JScript ou VBScript requer a instalação do objeto de [**sessão**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="c9949-149">A custom action that is written in JScript or VBScript requires the installation of [**Session Object**](session-object.md).</span></span> <span data-ttu-id="c9949-150">O instalador anexa o objeto de **sessão** ao script com a *sessão* de nome.</span><span class="sxs-lookup"><span data-stu-id="c9949-150">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="c9949-151">Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades do objeto de **sessão** descrito na seção [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar seu contexto.</span><span class="sxs-lookup"><span data-stu-id="c9949-151">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="c9949-152">Quando uma tabela de banco de dados é exportada, cada fluxo é gravado como um arquivo separado na subpasta nomeada após a tabela, usando a chave primária como o nome do arquivo (coluna de nome para a tabela binária), com uma extensão padrão de ". IBD".</span><span class="sxs-lookup"><span data-stu-id="c9949-152">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="c9949-153">O nome deve usar o formato de nome de arquivo 8,3 se o sistema de arquivos ou o sistema de controle de versão não oferecer suporte a nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="c9949-153">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="c9949-154">O arquivo morto persistente substitui os dados de fluxo pelo nome de arquivo usado, para que os dados possam ser localizados quando a tabela for importada.</span><span class="sxs-lookup"><span data-stu-id="c9949-154">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9949-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9949-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9949-156">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="c9949-156">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



