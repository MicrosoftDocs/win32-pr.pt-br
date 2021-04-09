---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 1 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo de ação personalizada 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011725"
---
# <a name="custom-action-type-1"></a><span data-ttu-id="b0dea-103">Tipo de ação personalizada 1</span><span class="sxs-lookup"><span data-stu-id="b0dea-103">Custom Action Type 1</span></span>

<span data-ttu-id="b0dea-104">Essa ação personalizada chama uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.</span><span class="sxs-lookup"><span data-stu-id="b0dea-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="b0dea-105">Fonte</span><span class="sxs-lookup"><span data-stu-id="b0dea-105">Source</span></span>

<span data-ttu-id="b0dea-106">A DLL é gerada a partir de um fluxo binário temporário.</span><span class="sxs-lookup"><span data-stu-id="b0dea-106">The DLL is generated from a temporary binary stream.</span></span> <span data-ttu-id="b0dea-107">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela binária](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="b0dea-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="b0dea-108">A coluna de dados na tabela binária contém os dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b0dea-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="b0dea-109">Um fluxo separado é alocado para cada linha.</span><span class="sxs-lookup"><span data-stu-id="b0dea-109">A separate stream is allocated for each row.</span></span> <span data-ttu-id="b0dea-110">Novos dados binários podem ser inseridos de um arquivo usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido por [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na tabela.</span><span class="sxs-lookup"><span data-stu-id="b0dea-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="b0dea-111">Quando a ação personalizada é invocada, os dados de fluxo são copiados em um arquivo temporário, que é processado dependendo do tipo de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="b0dea-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="b0dea-112">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="b0dea-112">Type Value</span></span>

<span data-ttu-id="b0dea-113">Inclua os seguintes bits de sinalizador na coluna Type da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="b0dea-113">Include the following flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="b0dea-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="b0dea-114">Constants</span></span>                                                          | <span data-ttu-id="b0dea-115">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="b0dea-115">Hexadecimal</span></span> | <span data-ttu-id="b0dea-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="b0dea-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="b0dea-117">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="b0dea-117">**msidbCustomActionTypeDll** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="b0dea-118">0x001</span><span class="sxs-lookup"><span data-stu-id="b0dea-118">0x001</span></span>       | <span data-ttu-id="b0dea-119">1</span><span class="sxs-lookup"><span data-stu-id="b0dea-119">1</span></span>       |



 

## <a name="target"></a><span data-ttu-id="b0dea-120">Destino</span><span class="sxs-lookup"><span data-stu-id="b0dea-120">Target</span></span>

<span data-ttu-id="b0dea-121">A DLL é chamada por meio do ponto de entrada nomeado no campo de destino da [tabela CustomAction](customaction-table.md), passando um único argumento que é o identificador para a sessão de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="b0dea-121">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="b0dea-122">O nome do ponto de entrada especificado na tabela deve corresponder ao exportado da DLL.</span><span class="sxs-lookup"><span data-stu-id="b0dea-122">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="b0dea-123">Observe que, se a função de entrada não for especificada por um. Arquivo DEF ou por uma especificação/EXPORT: linker, o nome pode ter um sublinhado à esquerda e um @4 sufixo "".</span><span class="sxs-lookup"><span data-stu-id="b0dea-123">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="b0dea-124">A função chamada deve especificar a \_ \_ Convenção de chamada stdcall.</span><span class="sxs-lookup"><span data-stu-id="b0dea-124">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="b0dea-125">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="b0dea-125">Return Processing Options</span></span>

<span data-ttu-id="b0dea-126">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="b0dea-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="b0dea-127">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="b0dea-127">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="b0dea-128">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="b0dea-128">Execution Scheduling Options</span></span>

<span data-ttu-id="b0dea-129">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="b0dea-129">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="b0dea-130">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b0dea-130">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="b0dea-131">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="b0dea-131">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="b0dea-132">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="b0dea-132">In-Script Execution Options</span></span>

<span data-ttu-id="b0dea-133">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="b0dea-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="b0dea-134">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="b0dea-134">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="b0dea-135">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="b0dea-135">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="b0dea-136">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b0dea-136">Return Values</span></span>

<span data-ttu-id="b0dea-137">Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b0dea-137">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0dea-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0dea-138">Remarks</span></span>

<span data-ttu-id="b0dea-139">Uma ação personalizada que chama uma DLL (biblioteca de vínculo dinâmico) requer um identificador para a sessão de instalação.</span><span class="sxs-lookup"><span data-stu-id="b0dea-139">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="b0dea-140">Se essa for também uma ação personalizada de execução adiada, a sessão poderá não existir mais durante a execução do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="b0dea-140">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="b0dea-141">Para obter informações sobre como uma ação personalizada desse tipo pode obter informações de contexto, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="b0dea-141">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="b0dea-142">Quando uma tabela de banco de dados é exportada, cada fluxo é gravado como um arquivo separado na subpasta nomeada após a tabela, usando a chave primária como o nome do arquivo (coluna de nome para a tabela binária), com uma extensão padrão de ". IBD".</span><span class="sxs-lookup"><span data-stu-id="b0dea-142">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="b0dea-143">O nome deve usar o formato 8,3 se o sistema de arquivos ou o sistema de controle de versão não oferecer suporte a nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="b0dea-143">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="b0dea-144">O arquivo morto persistente substitui os dados de fluxo pelo nome de arquivo usado, para que os dados possam ser localizados quando a tabela for importada.</span><span class="sxs-lookup"><span data-stu-id="b0dea-144">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0dea-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0dea-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0dea-146">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="b0dea-146">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="b0dea-147">Bibliotecas de vínculo dinâmico</span><span class="sxs-lookup"><span data-stu-id="b0dea-147">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> <dt>

[<span data-ttu-id="b0dea-148">Obtendo informações de contexto para ações personalizadas de execução adiada</span><span class="sxs-lookup"><span data-stu-id="b0dea-148">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



