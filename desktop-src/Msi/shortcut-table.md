---
description: A tabela de atalho contém as informações de que o aplicativo precisa para criar atalhos no computador do usuário.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabela de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828971"
---
# <a name="shortcut-table"></a><span data-ttu-id="cc178-103">Tabela de atalho</span><span class="sxs-lookup"><span data-stu-id="cc178-103">Shortcut Table</span></span>

<span data-ttu-id="cc178-104">A tabela de atalho contém as informações de que o aplicativo precisa para criar atalhos no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="cc178-104">The Shortcut table holds the information the application needs to create shortcuts on the user's computer.</span></span>

<span data-ttu-id="cc178-105">A tabela de atalho tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc178-105">The Shortcut table has the following columns.</span></span>



| <span data-ttu-id="cc178-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="cc178-106">Column</span></span>                 | <span data-ttu-id="cc178-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc178-107">Type</span></span>                         | <span data-ttu-id="cc178-108">Chave</span><span class="sxs-lookup"><span data-stu-id="cc178-108">Key</span></span> | <span data-ttu-id="cc178-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="cc178-109">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="cc178-110">Atalho</span><span class="sxs-lookup"><span data-stu-id="cc178-110">Shortcut</span></span>               | [<span data-ttu-id="cc178-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc178-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="cc178-112">S</span><span class="sxs-lookup"><span data-stu-id="cc178-112">Y</span></span>   | <span data-ttu-id="cc178-113">N</span><span class="sxs-lookup"><span data-stu-id="cc178-113">N</span></span>        |
| <span data-ttu-id="cc178-114">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="cc178-114">Directory\_</span></span>            | [<span data-ttu-id="cc178-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc178-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="cc178-116">N</span><span class="sxs-lookup"><span data-stu-id="cc178-116">N</span></span>   | <span data-ttu-id="cc178-117">N</span><span class="sxs-lookup"><span data-stu-id="cc178-117">N</span></span>        |
| <span data-ttu-id="cc178-118">Nome</span><span class="sxs-lookup"><span data-stu-id="cc178-118">Name</span></span>                   | [<span data-ttu-id="cc178-119">Filename</span><span class="sxs-lookup"><span data-stu-id="cc178-119">Filename</span></span>](filename.md)     | <span data-ttu-id="cc178-120">N</span><span class="sxs-lookup"><span data-stu-id="cc178-120">N</span></span>   | <span data-ttu-id="cc178-121">N</span><span class="sxs-lookup"><span data-stu-id="cc178-121">N</span></span>        |
| <span data-ttu-id="cc178-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="cc178-122">Component\_</span></span>            | [<span data-ttu-id="cc178-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc178-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="cc178-124">N</span><span class="sxs-lookup"><span data-stu-id="cc178-124">N</span></span>   | <span data-ttu-id="cc178-125">N</span><span class="sxs-lookup"><span data-stu-id="cc178-125">N</span></span>        |
| <span data-ttu-id="cc178-126">Destino</span><span class="sxs-lookup"><span data-stu-id="cc178-126">Target</span></span>                 | [<span data-ttu-id="cc178-127">Atalho</span><span class="sxs-lookup"><span data-stu-id="cc178-127">Shortcut</span></span>](shortcut.md)     | <span data-ttu-id="cc178-128">N</span><span class="sxs-lookup"><span data-stu-id="cc178-128">N</span></span>   | <span data-ttu-id="cc178-129">N</span><span class="sxs-lookup"><span data-stu-id="cc178-129">N</span></span>        |
| <span data-ttu-id="cc178-130">Argumentos</span><span class="sxs-lookup"><span data-stu-id="cc178-130">Arguments</span></span>              | [<span data-ttu-id="cc178-131">Binário</span><span class="sxs-lookup"><span data-stu-id="cc178-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="cc178-132">N</span><span class="sxs-lookup"><span data-stu-id="cc178-132">N</span></span>   | <span data-ttu-id="cc178-133">S</span><span class="sxs-lookup"><span data-stu-id="cc178-133">Y</span></span>        |
| <span data-ttu-id="cc178-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc178-134">Description</span></span>            | [<span data-ttu-id="cc178-135">Text</span><span class="sxs-lookup"><span data-stu-id="cc178-135">Text</span></span>](text.md)             | <span data-ttu-id="cc178-136">N</span><span class="sxs-lookup"><span data-stu-id="cc178-136">N</span></span>   | <span data-ttu-id="cc178-137">S</span><span class="sxs-lookup"><span data-stu-id="cc178-137">Y</span></span>        |
| <span data-ttu-id="cc178-138">Tecla de acesso</span><span class="sxs-lookup"><span data-stu-id="cc178-138">Hotkey</span></span>                 | [<span data-ttu-id="cc178-139">Inteiro</span><span class="sxs-lookup"><span data-stu-id="cc178-139">Integer</span></span>](integer.md)       | <span data-ttu-id="cc178-140">N</span><span class="sxs-lookup"><span data-stu-id="cc178-140">N</span></span>   | <span data-ttu-id="cc178-141">S</span><span class="sxs-lookup"><span data-stu-id="cc178-141">Y</span></span>        |
| <span data-ttu-id="cc178-142">ícone\_</span><span class="sxs-lookup"><span data-stu-id="cc178-142">Icon\_</span></span>                 | [<span data-ttu-id="cc178-143">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc178-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="cc178-144">N</span><span class="sxs-lookup"><span data-stu-id="cc178-144">N</span></span>   | <span data-ttu-id="cc178-145">S</span><span class="sxs-lookup"><span data-stu-id="cc178-145">Y</span></span>        |
| <span data-ttu-id="cc178-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="cc178-146">IconIndex</span></span>              | [<span data-ttu-id="cc178-147">Inteiro</span><span class="sxs-lookup"><span data-stu-id="cc178-147">Integer</span></span>](integer.md)       | <span data-ttu-id="cc178-148">N</span><span class="sxs-lookup"><span data-stu-id="cc178-148">N</span></span>   | <span data-ttu-id="cc178-149">S</span><span class="sxs-lookup"><span data-stu-id="cc178-149">Y</span></span>        |
| <span data-ttu-id="cc178-150">ShowCmd</span><span class="sxs-lookup"><span data-stu-id="cc178-150">ShowCmd</span></span>                | [<span data-ttu-id="cc178-151">Inteiro</span><span class="sxs-lookup"><span data-stu-id="cc178-151">Integer</span></span>](integer.md)       | <span data-ttu-id="cc178-152">N</span><span class="sxs-lookup"><span data-stu-id="cc178-152">N</span></span>   | <span data-ttu-id="cc178-153">S</span><span class="sxs-lookup"><span data-stu-id="cc178-153">Y</span></span>        |
| <span data-ttu-id="cc178-154">WkDir</span><span class="sxs-lookup"><span data-stu-id="cc178-154">WkDir</span></span>                  | [<span data-ttu-id="cc178-155">Identificador</span><span class="sxs-lookup"><span data-stu-id="cc178-155">Identifier</span></span>](identifier.md) | <span data-ttu-id="cc178-156">N</span><span class="sxs-lookup"><span data-stu-id="cc178-156">N</span></span>   | <span data-ttu-id="cc178-157">S</span><span class="sxs-lookup"><span data-stu-id="cc178-157">Y</span></span>        |
| <span data-ttu-id="cc178-158">DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="cc178-158">DisplayResourceDLL</span></span>     | [<span data-ttu-id="cc178-159">Binário</span><span class="sxs-lookup"><span data-stu-id="cc178-159">Formatted</span></span>](formatted.md)   | <span data-ttu-id="cc178-160">N</span><span class="sxs-lookup"><span data-stu-id="cc178-160">N</span></span>   | <span data-ttu-id="cc178-161">S</span><span class="sxs-lookup"><span data-stu-id="cc178-161">Y</span></span>        |
| <span data-ttu-id="cc178-162">DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="cc178-162">DisplayResourceId</span></span>      | [<span data-ttu-id="cc178-163">Inteiro</span><span class="sxs-lookup"><span data-stu-id="cc178-163">Integer</span></span>](integer.md)       | <span data-ttu-id="cc178-164">N</span><span class="sxs-lookup"><span data-stu-id="cc178-164">N</span></span>   | <span data-ttu-id="cc178-165">S</span><span class="sxs-lookup"><span data-stu-id="cc178-165">Y</span></span>        |
| <span data-ttu-id="cc178-166">DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="cc178-166">DescriptionResourceDLL</span></span> | [<span data-ttu-id="cc178-167">Binário</span><span class="sxs-lookup"><span data-stu-id="cc178-167">Formatted</span></span>](formatted.md)   | <span data-ttu-id="cc178-168">N</span><span class="sxs-lookup"><span data-stu-id="cc178-168">N</span></span>   | <span data-ttu-id="cc178-169">S</span><span class="sxs-lookup"><span data-stu-id="cc178-169">Y</span></span>        |
| <span data-ttu-id="cc178-170">DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="cc178-170">DescriptionResourceId</span></span>  | [<span data-ttu-id="cc178-171">Inteiro</span><span class="sxs-lookup"><span data-stu-id="cc178-171">Integer</span></span>](integer.md)       | <span data-ttu-id="cc178-172">N</span><span class="sxs-lookup"><span data-stu-id="cc178-172">N</span></span>   | <span data-ttu-id="cc178-173">S</span><span class="sxs-lookup"><span data-stu-id="cc178-173">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cc178-174">Colunas</span><span class="sxs-lookup"><span data-stu-id="cc178-174">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cc178-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Atalho</span><span class="sxs-lookup"><span data-stu-id="cc178-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Shortcut</span></span>
</dt> <dd>

<span data-ttu-id="cc178-176">O valor da chave para esta tabela.</span><span class="sxs-lookup"><span data-stu-id="cc178-176">The key value for this table.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_</span><span class="sxs-lookup"><span data-stu-id="cc178-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="cc178-178">A chave externa na primeira coluna da tabela de [diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-178">The external key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="cc178-179">Esta coluna especifica o diretório no qual o arquivo de atalho é criado.</span><span class="sxs-lookup"><span data-stu-id="cc178-179">This column specifies the directory in which the Shortcut file is created.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="cc178-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="cc178-181">O nome localizável do atalho a ser criado.</span><span class="sxs-lookup"><span data-stu-id="cc178-181">The localizable name of the shortcut to be created.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="cc178-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="cc178-183">A chave externa na primeira coluna da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-183">The external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="cc178-184">O instalador usa o estado de instalação do componente especificado nesta coluna para determinar se o atalho foi criado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="cc178-184">The installer uses the installation state of the component specified in this column to determine whether the shortcut is created or deleted.</span></span> <span data-ttu-id="cc178-185">Esse componente deve ter um caminho de chave válido para que o atalho seja instalado.</span><span class="sxs-lookup"><span data-stu-id="cc178-185">This component must have a valid key path for the shortcut to be installed.</span></span> <span data-ttu-id="cc178-186">Se a coluna de destino contiver o nome de um recurso, o arquivo iniciado pelo atalho será o arquivo de chave do componente listado nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="cc178-186">If the Target column contains the name of a feature, the file launched by the shortcut is the key file of the component listed in this column.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo</span><span class="sxs-lookup"><span data-stu-id="cc178-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="cc178-188">O destino do atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-188">The shortcut target.</span></span>

<span data-ttu-id="cc178-189">Para um atalho anunciado, essa coluna deve ser uma chave externa na primeira coluna da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-189">For an advertised shortcut, this column must be an external key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="cc178-190">O instalador avalia a entrada no campo de destino como um [identificador](identifier.md) e a entrada deve ser uma chave estrangeira válida na tabela de [recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-190">The installer evaluates the entry in the Target field as an [Identifier](identifier.md) and the entry must be a valid foreign key into the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="cc178-191">O arquivo iniciado pelo atalho, nesse caso, é o arquivo de chave do componente listado na coluna componente \_ .</span><span class="sxs-lookup"><span data-stu-id="cc178-191">The file launched by the shortcut in this case is the key file of the component listed in the Component\_ column.</span></span> <span data-ttu-id="cc178-192">Quando o atalho é ativado, o instalador verifica se todos os componentes do recurso estão instalados antes de iniciar este arquivo.</span><span class="sxs-lookup"><span data-stu-id="cc178-192">When the shortcut is activated, the installer verifies that all the components in the feature are installed before launching this file.</span></span>

<span data-ttu-id="cc178-193">Para um atalho não anunciado, o instalador avalia esse campo como uma cadeia de caracteres [formatada](formatted.md) .</span><span class="sxs-lookup"><span data-stu-id="cc178-193">For a non-advertised shortcut, the installer evaluates this field as a [Formatted](formatted.md) string.</span></span> <span data-ttu-id="cc178-194">O campo deve conter um identificador de propriedade entre colchetes ( \[ \] ), que é expandido no arquivo ou uma pasta apontada pelo atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-194">The field should contains a property identifier enclosed by square brackets (\[ \]), that is expanded into the file or a folder pointed to by the shortcut.</span></span> <span data-ttu-id="cc178-195">Para obter mais informações, consulte a [ação Createshortcuts](createshortcuts-action.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-195">For more information, see the [CreateShortcuts action](createshortcuts-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc178-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos</span><span class="sxs-lookup"><span data-stu-id="cc178-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="cc178-197">Os argumentos de linha de comando para o atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-197">The command-line arguments for the shortcut.</span></span>

<span data-ttu-id="cc178-198">Observe que a resolução das propriedades no campo argumentos é limitada.</span><span class="sxs-lookup"><span data-stu-id="cc178-198">Note that the resolution of properties in the Arguments field is limited.</span></span> <span data-ttu-id="cc178-199">Uma propriedade formatada como \[ *Propriedade* \] nesse campo só poderá ser resolvida se a propriedade já tiver o valor pretendido quando o componente proprietário do atalho for instalado.</span><span class="sxs-lookup"><span data-stu-id="cc178-199">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component that owns the shortcut is installed.</span></span> <span data-ttu-id="cc178-200">Por exemplo, para resolver o valor correto para o argumento " \[ \#MyDoc.doc\] ", o mesmo processo deve estar instalando o arquivo MyDoc.doc e o componente que possui o atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-200">For example, to resolve to the correct value for the argument "\[\#MyDoc.doc\]", the same process must be installing the file MyDoc.doc and the component that owns the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="cc178-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="cc178-202">A descrição localizável do atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-202">The localizable description of the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Tecla</span><span class="sxs-lookup"><span data-stu-id="cc178-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span></span>
</dt> <dd>

<span data-ttu-id="cc178-204">A tecla de atalhos do atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-204">The hotkey for the shortcut.</span></span> <span data-ttu-id="cc178-205">O byte de ordem inferior contém o código de chave virtual para a chave e o byte de ordem superior contém sinalizadores de modificador.</span><span class="sxs-lookup"><span data-stu-id="cc178-205">The low-order byte contains the virtual-key code for the key, and the high-order byte contains modifier flags.</span></span> <span data-ttu-id="cc178-206">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="cc178-206">This must be a non-negative number.</span></span> <span data-ttu-id="cc178-207">Os autores de pacotes de instalação geralmente são recomendados para não definir essa opção, pois a configuração dessa opção pode adicionar teclas de a-opções duplicadas à área de trabalho de um usuário.</span><span class="sxs-lookup"><span data-stu-id="cc178-207">Authors of installation packages are generally recommended not to set this option, because the setting of this option can add duplicate hotkeys to a user's desktop.</span></span> <span data-ttu-id="cc178-208">Além disso, a prática de atribuir teclas de atalho a atalhos pode ser problemática para os usuários que usam teclas de [acesso para acessibilidade](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-208">In addition, the practice of assigning hotkeys to shortcuts can be problematic for users using hotkeys for [accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc178-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Cone\_</span><span class="sxs-lookup"><span data-stu-id="cc178-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="cc178-210">A chave externa para a coluna um da [tabela de ícones](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-210">The external key to column one of the [Icon table](icon-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc178-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="cc178-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="cc178-212">O índice de ícone do atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-212">The icon index for the shortcut.</span></span> <span data-ttu-id="cc178-213">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="cc178-213">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span><span class="sxs-lookup"><span data-stu-id="cc178-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span></span>
</dt> <dd>

<span data-ttu-id="cc178-215">O comando show para a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cc178-215">The Show command for the application window.</span></span>

<span data-ttu-id="cc178-216">Os valores a seguir podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="cc178-216">The following values may be used.</span></span> <span data-ttu-id="cc178-217">Os valores são os definidos para a função de API do Windows.</span><span class="sxs-lookup"><span data-stu-id="cc178-217">The values are as defined for the Windows API function ShowWindow.</span></span>



| <span data-ttu-id="cc178-218">Valor</span><span class="sxs-lookup"><span data-stu-id="cc178-218">Value</span></span> | <span data-ttu-id="cc178-219">Significado</span><span class="sxs-lookup"><span data-stu-id="cc178-219">Meaning</span></span>             |
|-------|---------------------|
| <span data-ttu-id="cc178-220">1</span><span class="sxs-lookup"><span data-stu-id="cc178-220">1</span></span>     | <span data-ttu-id="cc178-221">SW \_ normal</span><span class="sxs-lookup"><span data-stu-id="cc178-221">SW\_SHOWNORMAL</span></span>      |
| <span data-ttu-id="cc178-222">3</span><span class="sxs-lookup"><span data-stu-id="cc178-222">3</span></span>     | <span data-ttu-id="cc178-223">SW não \_ maximizado</span><span class="sxs-lookup"><span data-stu-id="cc178-223">SW\_SHOWMAXIMIZED</span></span>   |
| <span data-ttu-id="cc178-224">7</span><span class="sxs-lookup"><span data-stu-id="cc178-224">7</span></span>     | <span data-ttu-id="cc178-225">\_SHOWMINNOACTIVE SW</span><span class="sxs-lookup"><span data-stu-id="cc178-225">SW\_SHOWMINNOACTIVE</span></span> |



 

</dd> <dt>

<span data-ttu-id="cc178-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span><span class="sxs-lookup"><span data-stu-id="cc178-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span></span>
</dt> <dd>

<span data-ttu-id="cc178-227">O nome da propriedade que tem o caminho do diretório de trabalho para o atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-227">The name of the property that has the path of the working directory for the shortcut.</span></span> <span data-ttu-id="cc178-228">O valor pode usar o formato do Windows para referenciar variáveis de ambiente, por exemplo% USERPROFILE%.</span><span class="sxs-lookup"><span data-stu-id="cc178-228">The value can use the Windows format to reference environment variables, for example %USERPROFILE%.</span></span> <span data-ttu-id="cc178-229">As referências são resolvidas para um caminho real quando o instalador resolve o diretório de trabalho para criar o atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-229">The references are resolved to an actual path when the installer resolves the working directory to create the shortcut.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="cc178-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="cc178-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="cc178-231">Esse campo contém um valor de cadeia de caracteres [formatado](formatted.md) para o caminho completo para o executável portátil neutro de idioma (arquivo ln) que contém os dados de configuração de recurso (RC config).</span><span class="sxs-lookup"><span data-stu-id="cc178-231">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="cc178-232">A cadeia de caracteres formatada pode usar a \[ \# \] Convenção FileKey.</span><span class="sxs-lookup"><span data-stu-id="cc178-232">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="cc178-233">Se esse campo contiver um valor, a coluna nome será ignorada.</span><span class="sxs-lookup"><span data-stu-id="cc178-233">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="cc178-234">Se esse campo estiver vazio, o instalador usará o valor na coluna nome.</span><span class="sxs-lookup"><span data-stu-id="cc178-234">If this field is empty, the installer uses the value in the Name column.</span></span> <span data-ttu-id="cc178-235">Quando esse campo contiver um valor, o campo **DisplayResourceId** também será necessário para conter um valor ou a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="cc178-235">When this field contains a value, the **DisplayResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="cc178-236">Esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada.</span><span class="sxs-lookup"><span data-stu-id="cc178-236">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="cc178-237">Esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="cc178-237">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="cc178-238">Para obter informações sobre como adicionar atalhos à tabela de atalho para uso com recursos de MUI, consulte [um exemplo de atalho do MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-238">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc178-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="cc178-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span></span>
</dt> <dd>

<span data-ttu-id="cc178-240">O índice do nome de exibição do atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-240">The display name index for the shortcut.</span></span> <span data-ttu-id="cc178-241">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="cc178-241">This must be a non-negative number.</span></span> <span data-ttu-id="cc178-242">Quando esse campo contém um valor, o campo **DisplayResourceDLL** também deve conter um valor ou a instalação falha.</span><span class="sxs-lookup"><span data-stu-id="cc178-242">When this field contains a value, the **DisplayResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="cc178-243">Esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada.</span><span class="sxs-lookup"><span data-stu-id="cc178-243">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="cc178-244">Esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="cc178-244">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> <dt>

<span data-ttu-id="cc178-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="cc178-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="cc178-246">Esse campo contém um valor de cadeia de caracteres [formatado](formatted.md) para o caminho completo para o executável portátil neutro de idioma (arquivo ln) que contém os dados de configuração de recurso (RC config).</span><span class="sxs-lookup"><span data-stu-id="cc178-246">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="cc178-247">A cadeia de caracteres formatada pode usar a \[ \# \] Convenção FileKey.</span><span class="sxs-lookup"><span data-stu-id="cc178-247">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="cc178-248">Se esse campo contiver um valor, a coluna nome será ignorada.</span><span class="sxs-lookup"><span data-stu-id="cc178-248">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="cc178-249">Se esse campo estiver vazio, o instalador usará o valor na coluna Descrição.</span><span class="sxs-lookup"><span data-stu-id="cc178-249">If this field is empty, the installer uses the value in the Description column.</span></span> <span data-ttu-id="cc178-250">Quando esse campo contiver um valor, o campo **DescriptionResourceId** também será necessário para conter um valor ou a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="cc178-250">When this field contains a value, the **DescriptionResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="cc178-251">Esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada.</span><span class="sxs-lookup"><span data-stu-id="cc178-251">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="cc178-252">Esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="cc178-252">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="cc178-253">Para obter informações sobre como adicionar atalhos à tabela de atalho para uso com recursos de MUI, consulte [um exemplo de atalho do MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="cc178-253">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc178-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="cc178-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span></span>
</dt> <dd>

<span data-ttu-id="cc178-255">O índice de nome de descrição do atalho.</span><span class="sxs-lookup"><span data-stu-id="cc178-255">The description name index for the shortcut.</span></span> <span data-ttu-id="cc178-256">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="cc178-256">This must be a non-negative number.</span></span> <span data-ttu-id="cc178-257">Quando esse campo contém um valor, o campo **DescriptionResourceDLL** também deve conter um valor ou a instalação falha.</span><span class="sxs-lookup"><span data-stu-id="cc178-257">When this field contains a value, the **DescriptionResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="cc178-258">Esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada.</span><span class="sxs-lookup"><span data-stu-id="cc178-258">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="cc178-259">Esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="cc178-259">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc178-260">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc178-260">Remarks</span></span>

<span data-ttu-id="cc178-261">A habilitação de um recurso criará um atalho anunciado somente se a interface IShellLink do sistema der suporte à resolução do descritor de instalador.</span><span class="sxs-lookup"><span data-stu-id="cc178-261">The enabling of a feature creates an advertised shortcut only if the system's IShellLink interface supports installer descriptor resolution.</span></span> <span data-ttu-id="cc178-262">Isso é suportado pelo Microsoft Windows 2000 e sistemas que executam o Microsoft Internet Explorer 4, 1.</span><span class="sxs-lookup"><span data-stu-id="cc178-262">This is supported by Microsoft Windows 2000 and systems running Microsoft Internet Explorer 4.01.</span></span> <span data-ttu-id="cc178-263">Se não houver suporte, o instalador criará um atalho não anunciado na instalação do componente do recurso, seja localmente ou executado a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="cc178-263">If unsupported, the installer creates a non-advertised shortcut upon the installation of the feature's component, either locally or run from source.</span></span>

<span data-ttu-id="cc178-264">Observe que os atalhos anunciados sempre apontam para um aplicativo específico, identificados por um [**ProductCode**](productcode.md)e não devem ser compartilhados entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="cc178-264">Note that advertised shortcuts always point at a particular application, identified by a [**ProductCode**](productcode.md), and should not be shared between applications.</span></span> <span data-ttu-id="cc178-265">Os atalhos anunciados só funcionam para o aplicativo instalado mais recentemente e são removidos quando esse aplicativo é removido.</span><span class="sxs-lookup"><span data-stu-id="cc178-265">Advertised shortcuts only work for the most recently installed application, and are removed when that application is removed.</span></span>

<span data-ttu-id="cc178-266">Essa tabela é referida quando a [ação Createshortcuts](createshortcuts-action.md) e a [ação RemoveShortcuts](removeshortcuts-action.md) são executadas.</span><span class="sxs-lookup"><span data-stu-id="cc178-266">This table is referred to when the [CreateShortcuts action](createshortcuts-action.md) and the [RemoveShortcuts action](removeshortcuts-action.md) is executed.</span></span>

<span data-ttu-id="cc178-267">Consulte também a propriedade [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .</span><span class="sxs-lookup"><span data-stu-id="cc178-267">See also the [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="cc178-268">Validação</span><span class="sxs-lookup"><span data-stu-id="cc178-268">Validation</span></span>

<dl>

[<span data-ttu-id="cc178-269">ICE03</span><span class="sxs-lookup"><span data-stu-id="cc178-269">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cc178-270">ICE06</span><span class="sxs-lookup"><span data-stu-id="cc178-270">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cc178-271">ICE19</span><span class="sxs-lookup"><span data-stu-id="cc178-271">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="cc178-272">ICE32</span><span class="sxs-lookup"><span data-stu-id="cc178-272">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="cc178-273">ICE36</span><span class="sxs-lookup"><span data-stu-id="cc178-273">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="cc178-274">ICE46</span><span class="sxs-lookup"><span data-stu-id="cc178-274">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="cc178-275">ICE50</span><span class="sxs-lookup"><span data-stu-id="cc178-275">ICE50</span></span>](ice50.md)  
[<span data-ttu-id="cc178-276">ICE57</span><span class="sxs-lookup"><span data-stu-id="cc178-276">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="cc178-277">ICE59</span><span class="sxs-lookup"><span data-stu-id="cc178-277">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="cc178-278">ICE67</span><span class="sxs-lookup"><span data-stu-id="cc178-278">ICE67</span></span>](ice67.md)  
[<span data-ttu-id="cc178-279">ICE69</span><span class="sxs-lookup"><span data-stu-id="cc178-279">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="cc178-280">ICE80</span><span class="sxs-lookup"><span data-stu-id="cc178-280">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="cc178-281">ICE90</span><span class="sxs-lookup"><span data-stu-id="cc178-281">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="cc178-282">ICE91</span><span class="sxs-lookup"><span data-stu-id="cc178-282">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="cc178-283">ICE94</span><span class="sxs-lookup"><span data-stu-id="cc178-283">ICE94</span></span>](ice94.md)  
</dl>

 

 



