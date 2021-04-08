---
description: A tabela IniFile contém as informações de. ini que o aplicativo precisa definir em um arquivo. ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabela IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010904"
---
# <a name="inifile-table"></a><span data-ttu-id="2a1ce-103">Tabela IniFile</span><span class="sxs-lookup"><span data-stu-id="2a1ce-103">IniFile Table</span></span>

<span data-ttu-id="2a1ce-104">A tabela IniFile contém as informações de. ini que o aplicativo precisa definir em um arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-104">The IniFile table contains the .ini information that the application needs to set in an .ini file.</span></span>

<span data-ttu-id="2a1ce-105">A tabela IniFile tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-105">The IniFile table has the following columns.</span></span>



| <span data-ttu-id="2a1ce-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="2a1ce-106">Column</span></span>      | <span data-ttu-id="2a1ce-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a1ce-107">Type</span></span>                         | <span data-ttu-id="2a1ce-108">Chave</span><span class="sxs-lookup"><span data-stu-id="2a1ce-108">Key</span></span> | <span data-ttu-id="2a1ce-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2a1ce-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="2a1ce-110">IniFile</span><span class="sxs-lookup"><span data-stu-id="2a1ce-110">IniFile</span></span>     | [<span data-ttu-id="2a1ce-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="2a1ce-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2a1ce-112">S</span><span class="sxs-lookup"><span data-stu-id="2a1ce-112">Y</span></span>   | <span data-ttu-id="2a1ce-113">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-113">N</span></span>        |
| <span data-ttu-id="2a1ce-114">FileName</span><span class="sxs-lookup"><span data-stu-id="2a1ce-114">FileName</span></span>    | [<span data-ttu-id="2a1ce-115">FileName</span><span class="sxs-lookup"><span data-stu-id="2a1ce-115">FileName</span></span>](text.md)         | <span data-ttu-id="2a1ce-116">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-116">N</span></span>   | <span data-ttu-id="2a1ce-117">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-117">N</span></span>        |
| <span data-ttu-id="2a1ce-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="2a1ce-118">DirProperty</span></span> | [<span data-ttu-id="2a1ce-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="2a1ce-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="2a1ce-120">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-120">N</span></span>   | <span data-ttu-id="2a1ce-121">S</span><span class="sxs-lookup"><span data-stu-id="2a1ce-121">Y</span></span>        |
| <span data-ttu-id="2a1ce-122">Seção</span><span class="sxs-lookup"><span data-stu-id="2a1ce-122">Section</span></span>     | [<span data-ttu-id="2a1ce-123">Binário</span><span class="sxs-lookup"><span data-stu-id="2a1ce-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2a1ce-124">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-124">N</span></span>   | <span data-ttu-id="2a1ce-125">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-125">N</span></span>        |
| <span data-ttu-id="2a1ce-126">Chave</span><span class="sxs-lookup"><span data-stu-id="2a1ce-126">Key</span></span>         | [<span data-ttu-id="2a1ce-127">Binário</span><span class="sxs-lookup"><span data-stu-id="2a1ce-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2a1ce-128">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-128">N</span></span>   | <span data-ttu-id="2a1ce-129">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-129">N</span></span>        |
| <span data-ttu-id="2a1ce-130">Valor</span><span class="sxs-lookup"><span data-stu-id="2a1ce-130">Value</span></span>       | [<span data-ttu-id="2a1ce-131">Binário</span><span class="sxs-lookup"><span data-stu-id="2a1ce-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2a1ce-132">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-132">N</span></span>   | <span data-ttu-id="2a1ce-133">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-133">N</span></span>        |
| <span data-ttu-id="2a1ce-134">Ação</span><span class="sxs-lookup"><span data-stu-id="2a1ce-134">Action</span></span>      | [<span data-ttu-id="2a1ce-135">Inteiro</span><span class="sxs-lookup"><span data-stu-id="2a1ce-135">Integer</span></span>](integer.md)       | <span data-ttu-id="2a1ce-136">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-136">N</span></span>   | <span data-ttu-id="2a1ce-137">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-137">N</span></span>        |
| <span data-ttu-id="2a1ce-138">Componente\_</span><span class="sxs-lookup"><span data-stu-id="2a1ce-138">Component\_</span></span> | [<span data-ttu-id="2a1ce-139">Identificador</span><span class="sxs-lookup"><span data-stu-id="2a1ce-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="2a1ce-140">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-140">N</span></span>   | <span data-ttu-id="2a1ce-141">N</span><span class="sxs-lookup"><span data-stu-id="2a1ce-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2a1ce-142">Colunas</span><span class="sxs-lookup"><span data-stu-id="2a1ce-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2a1ce-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span><span class="sxs-lookup"><span data-stu-id="2a1ce-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-144">A chave para esta tabela.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="2a1ce-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="2a1ce-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-146">O nome localizável do arquivo. ini no qual gravar as informações.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-146">The localizable name of the .ini file in which to write the information.</span></span>

</dd> <dt>

<span data-ttu-id="2a1ce-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="2a1ce-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-148">Nome de uma propriedade que tem um valor que resolve para o caminho completo da pasta que contém o arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-148">Name of a property having a value that resolves to the full path of the folder containing the .ini file.</span></span> <span data-ttu-id="2a1ce-149">A propriedade pode ser o nome de um diretório na [tabela de diretórios](directory-table.md), uma propriedade definida pela [tabela AppSearch](appsearch-table.md)ou qualquer outra propriedade que represente um caminho completo.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span> <span data-ttu-id="2a1ce-150">Se esse campo for deixado em branco, o arquivo. ini será criado na pasta com o caminho completo especificado pela propriedade [**WindowsFolder**](windowsfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="2a1ce-150">If this field is left blank, the .ini file is created in the folder having the full path specified by the [**WindowsFolder**](windowsfolder.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="2a1ce-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span><span class="sxs-lookup"><span data-stu-id="2a1ce-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-152">A seção do arquivo localizável. ini.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-152">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="2a1ce-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves</span><span class="sxs-lookup"><span data-stu-id="2a1ce-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-154">A chave do arquivo localizável. ini na seção.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-154">The localizable .ini file key within the section.</span></span>

</dd> <dt>

<span data-ttu-id="2a1ce-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="2a1ce-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-156">O valor localizável a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-156">The localizable value to be written.</span></span>

</dd> <dt>

<span data-ttu-id="2a1ce-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="2a1ce-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-158">O tipo de modificação a ser feita.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-158">The type of modification to be made.</span></span>



| <span data-ttu-id="2a1ce-159">Constante</span><span class="sxs-lookup"><span data-stu-id="2a1ce-159">Constant</span></span>                         | <span data-ttu-id="2a1ce-160">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="2a1ce-160">Hexadecimal</span></span> | <span data-ttu-id="2a1ce-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="2a1ce-161">Decimal</span></span> | <span data-ttu-id="2a1ce-162">Modification</span><span class="sxs-lookup"><span data-stu-id="2a1ce-162">Modification</span></span>                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a1ce-163">**msidbIniFileActionAddLine**</span><span class="sxs-lookup"><span data-stu-id="2a1ce-163">**msidbIniFileActionAddLine**</span></span>    | <span data-ttu-id="2a1ce-164">0x000</span><span class="sxs-lookup"><span data-stu-id="2a1ce-164">0x000</span></span>       | <span data-ttu-id="2a1ce-165">0</span><span class="sxs-lookup"><span data-stu-id="2a1ce-165">0</span></span>       | <span data-ttu-id="2a1ce-166">Cria ou atualiza uma entrada. ini.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-166">Creates or updates a .ini entry.</span></span>                                                 |
| <span data-ttu-id="2a1ce-167">**msidbIniFileActionCreateLine**</span><span class="sxs-lookup"><span data-stu-id="2a1ce-167">**msidbIniFileActionCreateLine**</span></span> | <span data-ttu-id="2a1ce-168">0x001</span><span class="sxs-lookup"><span data-stu-id="2a1ce-168">0x001</span></span>       | <span data-ttu-id="2a1ce-169">1</span><span class="sxs-lookup"><span data-stu-id="2a1ce-169">1</span></span>       | <span data-ttu-id="2a1ce-170">Cria uma entrada. ini somente se a entrada ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-170">Creates a .ini entry only if the entry does not already exist.</span></span>                   |
| <span data-ttu-id="2a1ce-171">**msidbIniFileActionAddTag**</span><span class="sxs-lookup"><span data-stu-id="2a1ce-171">**msidbIniFileActionAddTag**</span></span>     | <span data-ttu-id="2a1ce-172">0x003</span><span class="sxs-lookup"><span data-stu-id="2a1ce-172">0x003</span></span>       | <span data-ttu-id="2a1ce-173">3</span><span class="sxs-lookup"><span data-stu-id="2a1ce-173">3</span></span>       | <span data-ttu-id="2a1ce-174">Cria uma nova entrada ou acrescenta um novo valor separado por vírgula a uma entrada existente.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-174">Creates a new entry or appends a new comma-separated value to an existing entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2a1ce-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="2a1ce-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="2a1ce-176">Chave externa na primeira coluna da tabela de [componentes](component-table.md) que faz referência ao componente que controla a instalação do valor. ini.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-176">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a1ce-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a1ce-177">Remarks</span></span>

<span data-ttu-id="2a1ce-178">As informações do arquivo. ini são gravadas quando o componente correspondente foi selecionado para ser instalado como local ou executado da origem.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-178">The .ini file information is written out when the corresponding component has been selected to be installed as local or run from source.</span></span>

<span data-ttu-id="2a1ce-179">Essa tabela é referida quando a ação [WriteIniValues](writeinivalues-action.md) ou a [ação RemoveIniValues](removeinivalues-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-179">This table is referred to when the [WriteIniValues action](writeinivalues-action.md) or the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="2a1ce-180">Validação</span><span class="sxs-lookup"><span data-stu-id="2a1ce-180">Validation</span></span>

<dl>

[<span data-ttu-id="2a1ce-181">ICE03</span><span class="sxs-lookup"><span data-stu-id="2a1ce-181">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2a1ce-182">ICE06</span><span class="sxs-lookup"><span data-stu-id="2a1ce-182">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2a1ce-183">ICE32</span><span class="sxs-lookup"><span data-stu-id="2a1ce-183">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2a1ce-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="2a1ce-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="2a1ce-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="2a1ce-185">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="2a1ce-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="2a1ce-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="2a1ce-187">ICE91</span><span class="sxs-lookup"><span data-stu-id="2a1ce-187">ICE91</span></span>](ice91.md)  
</dl>

 

 



