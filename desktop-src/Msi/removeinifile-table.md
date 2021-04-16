---
description: A tabela RemoveIniFile contém as informações que um aplicativo precisa excluir de um arquivo. ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabela RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757509"
---
# <a name="removeinifile-table"></a><span data-ttu-id="8e1da-103">Tabela RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="8e1da-103">RemoveIniFile Table</span></span>

<span data-ttu-id="8e1da-104">A tabela RemoveIniFile contém as informações que um aplicativo precisa excluir de um arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="8e1da-104">The RemoveIniFile table contains the information an application needs to delete from a .ini file.</span></span>

<span data-ttu-id="8e1da-105">A tabela RemoveIniFile tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e1da-105">The RemoveIniFile table has the following columns.</span></span>



| <span data-ttu-id="8e1da-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="8e1da-106">Column</span></span>        | <span data-ttu-id="8e1da-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e1da-107">Type</span></span>                         | <span data-ttu-id="8e1da-108">Chave</span><span class="sxs-lookup"><span data-stu-id="8e1da-108">Key</span></span> | <span data-ttu-id="8e1da-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="8e1da-109">Nullable</span></span> |
|---------------|------------------------------|-----|----------|
| <span data-ttu-id="8e1da-110">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="8e1da-110">RemoveIniFile</span></span> | [<span data-ttu-id="8e1da-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="8e1da-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="8e1da-112">S</span><span class="sxs-lookup"><span data-stu-id="8e1da-112">Y</span></span>   | <span data-ttu-id="8e1da-113">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-113">N</span></span>        |
| <span data-ttu-id="8e1da-114">FileName</span><span class="sxs-lookup"><span data-stu-id="8e1da-114">FileName</span></span>      | [<span data-ttu-id="8e1da-115">FileName</span><span class="sxs-lookup"><span data-stu-id="8e1da-115">FileName</span></span>](text.md)         | <span data-ttu-id="8e1da-116">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-116">N</span></span>   | <span data-ttu-id="8e1da-117">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-117">N</span></span>        |
| <span data-ttu-id="8e1da-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="8e1da-118">DirProperty</span></span>   | [<span data-ttu-id="8e1da-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="8e1da-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="8e1da-120">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-120">N</span></span>   | <span data-ttu-id="8e1da-121">S</span><span class="sxs-lookup"><span data-stu-id="8e1da-121">Y</span></span>        |
| <span data-ttu-id="8e1da-122">Seção</span><span class="sxs-lookup"><span data-stu-id="8e1da-122">Section</span></span>       | [<span data-ttu-id="8e1da-123">Binário</span><span class="sxs-lookup"><span data-stu-id="8e1da-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8e1da-124">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-124">N</span></span>   | <span data-ttu-id="8e1da-125">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-125">N</span></span>        |
| <span data-ttu-id="8e1da-126">Chave</span><span class="sxs-lookup"><span data-stu-id="8e1da-126">Key</span></span>           | [<span data-ttu-id="8e1da-127">Binário</span><span class="sxs-lookup"><span data-stu-id="8e1da-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8e1da-128">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-128">N</span></span>   | <span data-ttu-id="8e1da-129">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-129">N</span></span>        |
| <span data-ttu-id="8e1da-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8e1da-130">Value</span></span>         | [<span data-ttu-id="8e1da-131">Binário</span><span class="sxs-lookup"><span data-stu-id="8e1da-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8e1da-132">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-132">N</span></span>   | <span data-ttu-id="8e1da-133">S</span><span class="sxs-lookup"><span data-stu-id="8e1da-133">Y</span></span>        |
| <span data-ttu-id="8e1da-134">Ação</span><span class="sxs-lookup"><span data-stu-id="8e1da-134">Action</span></span>        | [<span data-ttu-id="8e1da-135">Inteiro</span><span class="sxs-lookup"><span data-stu-id="8e1da-135">Integer</span></span>](integer.md)       | <span data-ttu-id="8e1da-136">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-136">N</span></span>   | <span data-ttu-id="8e1da-137">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-137">N</span></span>        |
| <span data-ttu-id="8e1da-138">Componente\_</span><span class="sxs-lookup"><span data-stu-id="8e1da-138">Component\_</span></span>   | [<span data-ttu-id="8e1da-139">Identificador</span><span class="sxs-lookup"><span data-stu-id="8e1da-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="8e1da-140">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-140">N</span></span>   | <span data-ttu-id="8e1da-141">N</span><span class="sxs-lookup"><span data-stu-id="8e1da-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8e1da-142">Colunas</span><span class="sxs-lookup"><span data-stu-id="8e1da-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8e1da-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="8e1da-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-144">A chave para esta tabela.</span><span class="sxs-lookup"><span data-stu-id="8e1da-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="8e1da-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="8e1da-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-146">O nome do arquivo. ini no qual as informações são excluídas.</span><span class="sxs-lookup"><span data-stu-id="8e1da-146">The .ini file name in which to delete the information.</span></span>

</dd> <dt>

<span data-ttu-id="8e1da-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="8e1da-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-148">Nome de uma propriedade cujo valor é considerado para ser resolvido para o caminho completo da pasta do arquivo. ini a ser removido.</span><span class="sxs-lookup"><span data-stu-id="8e1da-148">Name of a property whose value is assumed to resolve to the full path to the folder of the .ini file to be removed.</span></span> <span data-ttu-id="8e1da-149">A propriedade pode ser o nome de um diretório na [tabela de diretórios](directory-table.md), uma propriedade definida pela [tabela AppSearch](appsearch-table.md)ou qualquer outra propriedade que represente um caminho completo.</span><span class="sxs-lookup"><span data-stu-id="8e1da-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="8e1da-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span><span class="sxs-lookup"><span data-stu-id="8e1da-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-151">A seção do arquivo localizável. ini.</span><span class="sxs-lookup"><span data-stu-id="8e1da-151">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="8e1da-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves</span><span class="sxs-lookup"><span data-stu-id="8e1da-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-153">A chave do arquivo localizável. ini abaixo da seção.</span><span class="sxs-lookup"><span data-stu-id="8e1da-153">The localizable .ini file key below the section.</span></span>

</dd> <dt>

<span data-ttu-id="8e1da-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="8e1da-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-155">O valor localizável a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8e1da-155">The localizable value to be deleted.</span></span> <span data-ttu-id="8e1da-156">O valor é necessário quando a ação é 4.</span><span class="sxs-lookup"><span data-stu-id="8e1da-156">The value is required when Action is 4.</span></span>

</dd> <dt>

<span data-ttu-id="8e1da-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="8e1da-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-158">O tipo de modificação a ser feita.</span><span class="sxs-lookup"><span data-stu-id="8e1da-158">The type of modification to be made.</span></span>



| <span data-ttu-id="8e1da-159">Constante</span><span class="sxs-lookup"><span data-stu-id="8e1da-159">Constant</span></span>                         | <span data-ttu-id="8e1da-160">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8e1da-160">Hexadecimal</span></span> | <span data-ttu-id="8e1da-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="8e1da-161">Decimal</span></span> | <span data-ttu-id="8e1da-162">Significado</span><span class="sxs-lookup"><span data-stu-id="8e1da-162">Meaning</span></span>                          |
|----------------------------------|-------------|---------|----------------------------------|
| <span data-ttu-id="8e1da-163">**msidbIniFileActionRemoveLine**</span><span class="sxs-lookup"><span data-stu-id="8e1da-163">**msidbIniFileActionRemoveLine**</span></span> | <span data-ttu-id="8e1da-164">0x002</span><span class="sxs-lookup"><span data-stu-id="8e1da-164">0x002</span></span>       | <span data-ttu-id="8e1da-165">2</span><span class="sxs-lookup"><span data-stu-id="8e1da-165">2</span></span>       | <span data-ttu-id="8e1da-166">Exclui a entrada. ini.</span><span class="sxs-lookup"><span data-stu-id="8e1da-166">Deletes .ini entry.</span></span>              |
| <span data-ttu-id="8e1da-167">**msidbIniFileActionRemoveTag**</span><span class="sxs-lookup"><span data-stu-id="8e1da-167">**msidbIniFileActionRemoveTag**</span></span>  | <span data-ttu-id="8e1da-168">0x004</span><span class="sxs-lookup"><span data-stu-id="8e1da-168">0x004</span></span>       | <span data-ttu-id="8e1da-169">4</span><span class="sxs-lookup"><span data-stu-id="8e1da-169">4</span></span>       | <span data-ttu-id="8e1da-170">Exclui uma marca de uma entrada. ini.</span><span class="sxs-lookup"><span data-stu-id="8e1da-170">Deletes a tag from a .ini entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8e1da-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="8e1da-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="8e1da-172">Chave externa na primeira coluna da [tabela de componentes](component-table.md) que faz referência ao componente que controla a exclusão do valor. ini.</span><span class="sxs-lookup"><span data-stu-id="8e1da-172">External key into first column of the [Component table](component-table.md) referencing the component that controls the deletion of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e1da-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e1da-173">Remarks</span></span>

<span data-ttu-id="8e1da-174">As informações do arquivo. ini são excluídas quando o componente correspondente foi selecionado para ser instalado, seja localmente ou executado da origem.</span><span class="sxs-lookup"><span data-stu-id="8e1da-174">The .ini file information is deleted when the corresponding Component has been selected to be installed, either locally or run from source.</span></span>

<span data-ttu-id="8e1da-175">Essa tabela é referida quando a [ação RemoveIniValues](removeinivalues-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="8e1da-175">This table is referred to when the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

<span data-ttu-id="8e1da-176">Se a coluna de diretório \_ for especificada como nula, o local do arquivo ini será o local padrão do Windows ini, que é o diretório do Windows por padrão.</span><span class="sxs-lookup"><span data-stu-id="8e1da-176">If the Directory\_ column is specified as null, the ini file location is the standard Windows ini location which is the Windows directory by default.</span></span>

<span data-ttu-id="8e1da-177">A remoção do último valor de uma seção exclui essa seção.</span><span class="sxs-lookup"><span data-stu-id="8e1da-177">Removing the last value from a section deletes that section.</span></span> <span data-ttu-id="8e1da-178">Não há nenhuma outra maneira de excluir uma seção inteira que não seja remover todos os seus valores.</span><span class="sxs-lookup"><span data-stu-id="8e1da-178">There is no other way to delete an entire section other than removing all its values.</span></span>

## <a name="validation"></a><span data-ttu-id="8e1da-179">Validação</span><span class="sxs-lookup"><span data-stu-id="8e1da-179">Validation</span></span>

<dl>

[<span data-ttu-id="8e1da-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="8e1da-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8e1da-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="8e1da-181">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8e1da-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="8e1da-182">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8e1da-183">ICE40</span><span class="sxs-lookup"><span data-stu-id="8e1da-183">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="8e1da-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="8e1da-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="8e1da-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="8e1da-185">ICE69</span></span>](ice69.md)  
</dl>

 

 



