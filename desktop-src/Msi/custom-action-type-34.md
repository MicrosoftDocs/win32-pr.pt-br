---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 34 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Tipo de ação personalizada 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748598"
---
# <a name="custom-action-type-34"></a><span data-ttu-id="aed4c-103">Tipo de ação personalizada 34</span><span class="sxs-lookup"><span data-stu-id="aed4c-103">Custom Action Type 34</span></span>

<span data-ttu-id="aed4c-104">Essa ação personalizada chama um executável iniciado com uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="aed4c-104">This custom action calls an executable launched with a command line.</span></span> <span data-ttu-id="aed4c-105">Para obter mais informações, consulte [arquivos executáveis](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="aed4c-105">For more information, see [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="aed4c-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="aed4c-106">Source</span></span>

<span data-ttu-id="aed4c-107">O executável é gerado a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="aed4c-107">The executable is generated from a file.</span></span> <span data-ttu-id="aed4c-108">O campo de origem da tabela [CustomAction](customaction-table.md) contém uma chave para a tabela de [diretórios](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="aed4c-108">The Source field of the [CustomAction](customaction-table.md) table contains a key into the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="aed4c-109">A entrada da tabela de diretório referenciada é usada para resolver o caminho completo de um diretório de trabalho.</span><span class="sxs-lookup"><span data-stu-id="aed4c-109">The referenced Directory table entry is used to resolve the full path to a working directory.</span></span> <span data-ttu-id="aed4c-110">Isso não é necessário para ser o caminho para o diretório que contém o executável.</span><span class="sxs-lookup"><span data-stu-id="aed4c-110">This is not required to be the path to the directory containing the executable.</span></span>

## <a name="type-value"></a><span data-ttu-id="aed4c-111">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="aed4c-111">Type Value</span></span>

<span data-ttu-id="aed4c-112">Inclua o seguinte valor na coluna tipo da tabela [CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="aed4c-112">Include the following value in the Type column of the [CustomAction](customaction-table.md) table to specify the basic numeric type.</span></span>



| <span data-ttu-id="aed4c-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="aed4c-113">Constants</span></span>                                                         | <span data-ttu-id="aed4c-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="aed4c-114">Hexadecimal</span></span> | <span data-ttu-id="aed4c-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="aed4c-115">Decimal</span></span> |
|-------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="aed4c-116">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="aed4c-116">**msidbCustomActionTypeExe** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="aed4c-117">0x022</span><span class="sxs-lookup"><span data-stu-id="aed4c-117">0x022</span></span>       | <span data-ttu-id="aed4c-118">34</span><span class="sxs-lookup"><span data-stu-id="aed4c-118">34</span></span>      |



 

## <a name="target"></a><span data-ttu-id="aed4c-119">Destino</span><span class="sxs-lookup"><span data-stu-id="aed4c-119">Target</span></span>

<span data-ttu-id="aed4c-120">A coluna de destino da tabela [CustomAction](customaction-table.md) contém o caminho completo e o nome do arquivo executável seguido por argumentos opcionais para o executável.</span><span class="sxs-lookup"><span data-stu-id="aed4c-120">The Target column of the [CustomAction](customaction-table.md) table contains the full path and name of the executable file followed by optional arguments to the executable.</span></span> <span data-ttu-id="aed4c-121">O caminho completo e o nome do arquivo executável são necessários.</span><span class="sxs-lookup"><span data-stu-id="aed4c-121">The full path and name to the executable file is required.</span></span> <span data-ttu-id="aed4c-122">As aspas devem ser usadas ao longo de caminhos ou nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="aed4c-122">Quotation marks must be used around long file names or paths.</span></span> <span data-ttu-id="aed4c-123">O valor é tratado como texto [formatado](formatted.md) e pode conter referências a propriedades, arquivos, diretórios ou outros atributos de texto formatado.</span><span class="sxs-lookup"><span data-stu-id="aed4c-123">The value is treated as [formatted](formatted.md) text and may contain references to properties, files, directories, or other formatted text attributes.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="aed4c-124">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="aed4c-124">Return Processing Options</span></span>

<span data-ttu-id="aed4c-125">Inclua bits de sinalizador opcionais na coluna Type da tabela [CustomAction](customaction-table.md) para especificar opções de processamento de retorno.</span><span class="sxs-lookup"><span data-stu-id="aed4c-125">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify return processing options.</span></span> <span data-ttu-id="aed4c-126">Para obter uma descrição das opções e dos valores, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="aed4c-126">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="aed4c-127">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="aed4c-127">Execution Scheduling Options</span></span>

<span data-ttu-id="aed4c-128">Inclua bits de sinalizador opcionais na coluna Type da tabela [CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="aed4c-128">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify execution scheduling options.</span></span> <span data-ttu-id="aed4c-129">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="aed4c-129">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="aed4c-130">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="aed4c-130">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="aed4c-131">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="aed4c-131">In-Script Execution Options</span></span>

<span data-ttu-id="aed4c-132">Inclua bits de sinalizador opcionais na coluna Type da tabela [CustomAction](customaction-table.md) para especificar uma opção de execução em script.</span><span class="sxs-lookup"><span data-stu-id="aed4c-132">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify an in-script execution option.</span></span> <span data-ttu-id="aed4c-133">Essas opções copiam o código de ação para o script de execução, reversão ou confirmação.</span><span class="sxs-lookup"><span data-stu-id="aed4c-133">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="aed4c-134">Para obter uma descrição das opções, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="aed4c-134">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="aed4c-135">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="aed4c-135">Return Values</span></span>

<span data-ttu-id="aed4c-136">As ações personalizadas que são [arquivos executáveis](executable-files.md) devem retornar um valor de 0 para êxito.</span><span class="sxs-lookup"><span data-stu-id="aed4c-136">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="aed4c-137">O instalador interpreta qualquer outro valor de retorno como falha.</span><span class="sxs-lookup"><span data-stu-id="aed4c-137">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="aed4c-138">Para ignorar valores de retorno, defina o sinalizador de bit **msidbCustomActionTypeContinue** no campo Type da tabela [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="aed4c-138">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction](customaction-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="aed4c-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="aed4c-139">Remarks</span></span>

<span data-ttu-id="aed4c-140">Uma ação personalizada que inicia um executável usa uma linha de comando, que normalmente contém propriedades que são designadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="aed4c-140">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="aed4c-141">Se essa for também uma [ação personalizada de execução adiada](deferred-execution-custom-actions.md), o instalador usará [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para criar o processo quando a ação personalizada for invocada a partir do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="aed4c-141">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aed4c-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aed4c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aed4c-143">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="aed4c-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 
