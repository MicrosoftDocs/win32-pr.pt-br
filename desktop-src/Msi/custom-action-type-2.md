---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 2 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Tipo de ação personalizada 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747777"
---
# <a name="custom-action-type-2"></a><span data-ttu-id="c1394-103">Tipo de ação personalizada 2</span><span class="sxs-lookup"><span data-stu-id="c1394-103">Custom Action Type 2</span></span>

<span data-ttu-id="c1394-104">Essa ação personalizada chama um executável iniciado com uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c1394-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="c1394-105">Fonte</span><span class="sxs-lookup"><span data-stu-id="c1394-105">Source</span></span>

<span data-ttu-id="c1394-106">O executável é gerado a partir de um fluxo binário temporário.</span><span class="sxs-lookup"><span data-stu-id="c1394-106">The executable is generated from a temporary binary stream.</span></span> <span data-ttu-id="c1394-107">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela binária](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="c1394-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="c1394-108">A coluna de dados na tabela binária contém os dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c1394-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="c1394-109">Um fluxo separado é alocado para cada linha.</span><span class="sxs-lookup"><span data-stu-id="c1394-109">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="c1394-110">Novos dados binários podem ser inseridos de um arquivo usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido por [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na tabela.</span><span class="sxs-lookup"><span data-stu-id="c1394-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="c1394-111">Quando a ação personalizada é invocada, os dados de fluxo são copiados em um arquivo temporário, que é processado dependendo do tipo de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="c1394-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="c1394-112">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="c1394-112">Type Value</span></span>

<span data-ttu-id="c1394-113">Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="c1394-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="c1394-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="c1394-114">Constants</span></span>                                                          | <span data-ttu-id="c1394-115">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c1394-115">Hexadecimal</span></span> | <span data-ttu-id="c1394-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="c1394-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="c1394-117">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="c1394-117">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="c1394-118">0x002</span><span class="sxs-lookup"><span data-stu-id="c1394-118">0x002</span></span>       | <span data-ttu-id="c1394-119">2</span><span class="sxs-lookup"><span data-stu-id="c1394-119">2</span></span>       |



 

## <a name="target"></a><span data-ttu-id="c1394-120">Destino</span><span class="sxs-lookup"><span data-stu-id="c1394-120">Target</span></span>

<span data-ttu-id="c1394-121">A coluna de destino da [tabela CustomAction](customaction-table.md) contém a cadeia de caracteres de linha de comando para o executável nomeado na coluna de origem.</span><span class="sxs-lookup"><span data-stu-id="c1394-121">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable named in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="c1394-122">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="c1394-122">Return Processing Options</span></span>

<span data-ttu-id="c1394-123">Inclua bits de sinalizador opcionais na coluna Type da tabela CustomAction para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="c1394-123">Include optional flag bits in the Type column of the CustomAction table to specify return processing options.</span></span> <span data-ttu-id="c1394-124">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c1394-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="c1394-125">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="c1394-125">Execution Scheduling Options</span></span>

<span data-ttu-id="c1394-126">Inclua bits de sinalizador opcionais na coluna Type da tabela CustomAction para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="c1394-126">Include optional flag bits in the Type column of the CustomAction table to specify execution scheduling options.</span></span> <span data-ttu-id="c1394-127">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c1394-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="c1394-128">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="c1394-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="c1394-129">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="c1394-129">In-Script Execution Options</span></span>

<span data-ttu-id="c1394-130">Inclua bits de sinalizador opcionais na coluna Type da tabela CustomAction para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="c1394-130">Include optional flag bits in the Type column of the CustomAction table to specify an in-script execution option.</span></span> <span data-ttu-id="c1394-131">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="c1394-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="c1394-132">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="c1394-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="c1394-133">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c1394-133">Return Values</span></span>

<span data-ttu-id="c1394-134">As ações personalizadas que são [arquivos executáveis](executable-files.md) devem retornar um valor de 0 para êxito.</span><span class="sxs-lookup"><span data-stu-id="c1394-134">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="c1394-135">O instalador interpreta qualquer outro valor de retorno como falha.</span><span class="sxs-lookup"><span data-stu-id="c1394-135">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="c1394-136">Para ignorar valores de retorno, defina o sinalizador de bit **msidbCustomActionTypeContinue** no campo Type da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="c1394-136">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1394-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1394-137">Remarks</span></span>

<span data-ttu-id="c1394-138">Uma ação personalizada que inicia um executável usa uma linha de comando, que normalmente contém propriedades que são designadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="c1394-138">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="c1394-139">Se essa for também uma [ação personalizada de execução adiada](deferred-execution-custom-actions.md), o instalador usará [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para criar o processo quando a ação personalizada for invocada a partir do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="c1394-139">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="c1394-140">Quando uma tabela de banco de dados é exportada, cada fluxo é gravado como um arquivo separado na subpasta nomeada após a tabela, usando a chave primária como o nome do arquivo (coluna de nome para a tabela binária), com uma extensão padrão de ". IBD".</span><span class="sxs-lookup"><span data-stu-id="c1394-140">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="c1394-141">O nome deve usar o formato 8,3 se o sistema de arquivos ou o sistema de controle de versão não oferecer suporte a nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="c1394-141">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="c1394-142">O arquivo morto persistente substitui os dados de fluxo pelo nome de arquivo usado, para que os dados possam ser localizados quando a tabela for importada.</span><span class="sxs-lookup"><span data-stu-id="c1394-142">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1394-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1394-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1394-144">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="c1394-144">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c1394-145">Arquivos executáveis</span><span class="sxs-lookup"><span data-stu-id="c1394-145">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
