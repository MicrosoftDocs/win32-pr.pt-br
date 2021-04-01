---
description: A tabela CustomAction fornece os meios de integrar código e dados personalizados à instalação. A origem do código que é executado pode ser um fluxo contido no banco de dados, um arquivo recentemente instalado ou um arquivo executável existente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabela CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647355"
---
# <a name="customaction-table"></a><span data-ttu-id="02f46-104">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="02f46-104">CustomAction Table</span></span>

<span data-ttu-id="02f46-105">A tabela CustomAction fornece os meios de integrar código e dados personalizados à instalação.</span><span class="sxs-lookup"><span data-stu-id="02f46-105">The CustomAction table provides the means of integrating custom code and data into the installation.</span></span> <span data-ttu-id="02f46-106">A origem do código que é executado pode ser um fluxo contido no banco de dados, um arquivo recentemente instalado ou um arquivo executável existente.</span><span class="sxs-lookup"><span data-stu-id="02f46-106">The source of the code that is executed can be a stream contained within the database, a recently installed file, or an existing executable file.</span></span>

<span data-ttu-id="02f46-107">A tabela CustomAction tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="02f46-107">The CustomAction table has the following columns.</span></span>



| <span data-ttu-id="02f46-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="02f46-108">Column</span></span>       | <span data-ttu-id="02f46-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="02f46-109">Type</span></span>                               | <span data-ttu-id="02f46-110">Chave</span><span class="sxs-lookup"><span data-stu-id="02f46-110">Key</span></span> | <span data-ttu-id="02f46-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="02f46-111">Nullable</span></span> |
|--------------|------------------------------------|-----|----------|
| <span data-ttu-id="02f46-112">Ação</span><span class="sxs-lookup"><span data-stu-id="02f46-112">Action</span></span>       | [<span data-ttu-id="02f46-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="02f46-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="02f46-114">S</span><span class="sxs-lookup"><span data-stu-id="02f46-114">Y</span></span>   | <span data-ttu-id="02f46-115">N</span><span class="sxs-lookup"><span data-stu-id="02f46-115">N</span></span>        |
| <span data-ttu-id="02f46-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="02f46-116">Type</span></span>         | [<span data-ttu-id="02f46-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="02f46-117">Integer</span></span>](integer.md)             | <span data-ttu-id="02f46-118">N</span><span class="sxs-lookup"><span data-stu-id="02f46-118">N</span></span>   | <span data-ttu-id="02f46-119">N</span><span class="sxs-lookup"><span data-stu-id="02f46-119">N</span></span>        |
| <span data-ttu-id="02f46-120">Fonte</span><span class="sxs-lookup"><span data-stu-id="02f46-120">Source</span></span>       | [<span data-ttu-id="02f46-121">CustomSource</span><span class="sxs-lookup"><span data-stu-id="02f46-121">CustomSource</span></span>](customsource.md)   | <span data-ttu-id="02f46-122">N</span><span class="sxs-lookup"><span data-stu-id="02f46-122">N</span></span>   | <span data-ttu-id="02f46-123">S</span><span class="sxs-lookup"><span data-stu-id="02f46-123">Y</span></span>        |
| <span data-ttu-id="02f46-124">Destino</span><span class="sxs-lookup"><span data-stu-id="02f46-124">Target</span></span>       | [<span data-ttu-id="02f46-125">Binário</span><span class="sxs-lookup"><span data-stu-id="02f46-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="02f46-126">N</span><span class="sxs-lookup"><span data-stu-id="02f46-126">N</span></span>   | <span data-ttu-id="02f46-127">S</span><span class="sxs-lookup"><span data-stu-id="02f46-127">Y</span></span>        |
| <span data-ttu-id="02f46-128">ExtendedType</span><span class="sxs-lookup"><span data-stu-id="02f46-128">ExtendedType</span></span> | [<span data-ttu-id="02f46-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="02f46-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="02f46-130">N</span><span class="sxs-lookup"><span data-stu-id="02f46-130">N</span></span>   | <span data-ttu-id="02f46-131">S</span><span class="sxs-lookup"><span data-stu-id="02f46-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02f46-132">Colunas</span><span class="sxs-lookup"><span data-stu-id="02f46-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02f46-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="02f46-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="02f46-134">Nome da ação.</span><span class="sxs-lookup"><span data-stu-id="02f46-134">Name of the action.</span></span> <span data-ttu-id="02f46-135">A ação normalmente aparece em uma tabela de sequência, a menos que seja chamada por outra ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="02f46-135">The action normally appears in a sequence table unless it is called by another custom action.</span></span> <span data-ttu-id="02f46-136">Se o nome corresponder a qualquer ação interna, a ação personalizada nunca será chamada.</span><span class="sxs-lookup"><span data-stu-id="02f46-136">If the name matches any built-in action, then the custom action is never called.</span></span>

<span data-ttu-id="02f46-137">Chave de tabela primária.</span><span class="sxs-lookup"><span data-stu-id="02f46-137">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="02f46-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva</span><span class="sxs-lookup"><span data-stu-id="02f46-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="02f46-139">Um campo de bits de sinalizador que especifica o tipo básico de ação e opções personalizadas.</span><span class="sxs-lookup"><span data-stu-id="02f46-139">A field of flag bits specifying the basic type of custom action and options.</span></span> <span data-ttu-id="02f46-140">Consulte [Resumo da lista de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md) para obter uma lista dos tipos básicos.</span><span class="sxs-lookup"><span data-stu-id="02f46-140">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a list of the basic types.</span></span> <span data-ttu-id="02f46-141">Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md), [Opções de agendamento de execução de ação](custom-action-execution-scheduling-options.md)personalizada, opção de [destino oculto de ação](custom-action-hidden-target-option.md)personalizada e opções de execução de In-Script de [ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="02f46-141">See [Custom Action Return Processing Options](custom-action-return-processing-options.md), [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md), [Custom Action Hidden Target Option](custom-action-hidden-target-option.md), and [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

</dd> <dt>

<span data-ttu-id="02f46-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Original</span><span class="sxs-lookup"><span data-stu-id="02f46-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="02f46-143">Um nome de propriedade ou uma chave externa em outra tabela.</span><span class="sxs-lookup"><span data-stu-id="02f46-143">A property name or external key into another table.</span></span> <span data-ttu-id="02f46-144">Para obter uma discussão sobre as possíveis fontes de ação personalizadas, consulte [fontes de ação personalizadas](custom-action-sources.md) e a [lista de Resumo de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="02f46-144">For a discussion of the possible custom action sources, see [Custom Action Sources](custom-action-sources.md) and the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span> <span data-ttu-id="02f46-145">Por exemplo, a coluna de origem pode conter uma chave externa na primeira coluna de uma das tabelas a seguir contendo a origem do código de ação personalizado.</span><span class="sxs-lookup"><span data-stu-id="02f46-145">For example, the Source column may contain an external key into the first column of one of the following tables containing the source of the custom action code.</span></span>

<span data-ttu-id="02f46-146">[Tabela de diretórios](directory-table.md) para chamar executáveis existentes.</span><span class="sxs-lookup"><span data-stu-id="02f46-146">[Directory table](directory-table.md) for calling existing executables.</span></span>

<span data-ttu-id="02f46-147">[Tabela de arquivos](file-table.md) para chamar executáveis e DLLs que acabou de ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="02f46-147">[File table](file-table.md) for calling executables and DLLs that have just been installed.</span></span>

<span data-ttu-id="02f46-148">[Tabela binária](binary-table.md) para chamar executáveis, DLLs e dados armazenados no banco de dado.</span><span class="sxs-lookup"><span data-stu-id="02f46-148">[Binary table](binary-table.md) for calling executables, DLLs, and data stored in the database.</span></span>

<span data-ttu-id="02f46-149">[Tabela de propriedades](property-table.md) para chamar executáveis cujos caminhos são mantidos por uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="02f46-149">[Property table](property-table.md) for calling executables whose paths are held by a property.</span></span>

</dd> <dt>

<span data-ttu-id="02f46-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo</span><span class="sxs-lookup"><span data-stu-id="02f46-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="02f46-151">Um parâmetro de execução que depende do tipo básico de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="02f46-151">An execution parameter that depends on the basic type of custom action.</span></span> <span data-ttu-id="02f46-152">Consulte a [lista de Resumo de todos os tipos de ação personalizada](summary-list-of-all-custom-action-types.md) para obter uma descrição do que deve ser inserido nesse campo para cada tipo de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="02f46-152">See the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a description of what should be entered in this field for each type of custom action.</span></span> <span data-ttu-id="02f46-153">Por exemplo, esse campo pode conter o seguinte, dependendo da ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="02f46-153">For example, this field may contain the following depending on the custom action.</span></span>



| <span data-ttu-id="02f46-154">Destino</span><span class="sxs-lookup"><span data-stu-id="02f46-154">Target</span></span>                                    | <span data-ttu-id="02f46-155">Ação personalizada</span><span class="sxs-lookup"><span data-stu-id="02f46-155">Custom action</span></span>                         |
|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="02f46-156">Ponto de entrada (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="02f46-156">Entry point (required)</span></span>                    | <span data-ttu-id="02f46-157">Chamando uma DLL.</span><span class="sxs-lookup"><span data-stu-id="02f46-157">Calling a DLL.</span></span>                        |
| <span data-ttu-id="02f46-158">Nome do executável com argumentos (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="02f46-158">Executable name with arguments (required)</span></span> | <span data-ttu-id="02f46-159">Chamando um executável existente.</span><span class="sxs-lookup"><span data-stu-id="02f46-159">Calling an existing executable.</span></span>       |
| <span data-ttu-id="02f46-160">Argumentos de linha de comando (opcional)</span><span class="sxs-lookup"><span data-stu-id="02f46-160">Command line arguments (optional)</span></span>         | <span data-ttu-id="02f46-161">Chamando um executável que acabou de ser instalado.</span><span class="sxs-lookup"><span data-stu-id="02f46-161">Calling an executable just installed.</span></span> |
| <span data-ttu-id="02f46-162">Nome do arquivo de destino (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="02f46-162">Target file name (required)</span></span>               | <span data-ttu-id="02f46-163">Criando um arquivo a partir de dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="02f46-163">Creating a file from custom data.</span></span>     |
| <span data-ttu-id="02f46-164">Nulo</span><span class="sxs-lookup"><span data-stu-id="02f46-164">Null</span></span>                                      | <span data-ttu-id="02f46-165">Executando código de script.</span><span class="sxs-lookup"><span data-stu-id="02f46-165">Executing script code.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="02f46-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span><span class="sxs-lookup"><span data-stu-id="02f46-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span></span>
</dt> <dd>

<span data-ttu-id="02f46-167">Insira o valor de **msidbCustomActionTypePatchUninstall** nesse campo para especificar uma ação personalizada com a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md).</span><span class="sxs-lookup"><span data-stu-id="02f46-167">Enter the **msidbCustomActionTypePatchUninstall** value in this field to specify a custom action with the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md).</span></span>

<span data-ttu-id="02f46-168">**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="02f46-168">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="02f46-169">Essa opção está disponível a partir do Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="02f46-169">This option is available beginning with Windows Installer 4.5.</span></span>

</dd> </dl>

<span data-ttu-id="02f46-170">Para obter mais informações, consulte todos os tópicos em [ações personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="02f46-170">For more information, see all the topics under [Custom Actions](custom-actions.md).</span></span>

## <a name="validation"></a><span data-ttu-id="02f46-171">Validação</span><span class="sxs-lookup"><span data-stu-id="02f46-171">Validation</span></span>

<dl>

[<span data-ttu-id="02f46-172">ICE03</span><span class="sxs-lookup"><span data-stu-id="02f46-172">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02f46-173">ICE06</span><span class="sxs-lookup"><span data-stu-id="02f46-173">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="02f46-174">ICE12</span><span class="sxs-lookup"><span data-stu-id="02f46-174">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="02f46-175">ICE27</span><span class="sxs-lookup"><span data-stu-id="02f46-175">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="02f46-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="02f46-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="02f46-177">ICE63</span><span class="sxs-lookup"><span data-stu-id="02f46-177">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="02f46-178">ICE68</span><span class="sxs-lookup"><span data-stu-id="02f46-178">ICE68</span></span>](ice68.md)  
[<span data-ttu-id="02f46-179">ICE72</span><span class="sxs-lookup"><span data-stu-id="02f46-179">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="02f46-180">ICE75</span><span class="sxs-lookup"><span data-stu-id="02f46-180">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="02f46-181">ICE77</span><span class="sxs-lookup"><span data-stu-id="02f46-181">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="02f46-182">ICE80</span><span class="sxs-lookup"><span data-stu-id="02f46-182">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="02f46-183">ICE88</span><span class="sxs-lookup"><span data-stu-id="02f46-183">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="02f46-184">ICE93</span><span class="sxs-lookup"><span data-stu-id="02f46-184">ICE93</span></span>](ice93.md)  
</dl>

 

 



