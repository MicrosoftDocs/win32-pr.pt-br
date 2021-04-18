---
description: A tabela IniLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando um arquivo. ini ou para procurar uma própria entrada. ini em particular. O arquivo. ini deve estar presente no diretório padrão do Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabela IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747977"
---
# <a name="inilocator-table"></a><span data-ttu-id="6ff58-104">Tabela IniLocator</span><span class="sxs-lookup"><span data-stu-id="6ff58-104">IniLocator Table</span></span>

<span data-ttu-id="6ff58-105">A tabela IniLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando um arquivo. ini ou para procurar uma própria entrada. ini em particular.</span><span class="sxs-lookup"><span data-stu-id="6ff58-105">The IniLocator table holds the information needed to search for a file or directory using an .ini file or to search for a particular .ini entry itself.</span></span> <span data-ttu-id="6ff58-106">O arquivo. ini deve estar presente no diretório padrão do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6ff58-106">The .ini file must be present in the default Microsoft Windows directory.</span></span>

<span data-ttu-id="6ff58-107">A tabela IniLocator tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ff58-107">The IniLocator table has the following columns.</span></span>



| <span data-ttu-id="6ff58-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="6ff58-108">Column</span></span>      | <span data-ttu-id="6ff58-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ff58-109">Type</span></span>                         | <span data-ttu-id="6ff58-110">Chave</span><span class="sxs-lookup"><span data-stu-id="6ff58-110">Key</span></span> | <span data-ttu-id="6ff58-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="6ff58-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="6ff58-112">Signature\_</span><span class="sxs-lookup"><span data-stu-id="6ff58-112">Signature\_</span></span> | [<span data-ttu-id="6ff58-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="6ff58-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="6ff58-114">S</span><span class="sxs-lookup"><span data-stu-id="6ff58-114">Y</span></span>   | <span data-ttu-id="6ff58-115">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-115">N</span></span>        |
| <span data-ttu-id="6ff58-116">FileName</span><span class="sxs-lookup"><span data-stu-id="6ff58-116">FileName</span></span>    | [<span data-ttu-id="6ff58-117">FileName</span><span class="sxs-lookup"><span data-stu-id="6ff58-117">FileName</span></span>](text.md)         | <span data-ttu-id="6ff58-118">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-118">N</span></span>   | <span data-ttu-id="6ff58-119">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-119">N</span></span>        |
| <span data-ttu-id="6ff58-120">Seção</span><span class="sxs-lookup"><span data-stu-id="6ff58-120">Section</span></span>     | [<span data-ttu-id="6ff58-121">Text</span><span class="sxs-lookup"><span data-stu-id="6ff58-121">Text</span></span>](text.md)             | <span data-ttu-id="6ff58-122">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-122">N</span></span>   | <span data-ttu-id="6ff58-123">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-123">N</span></span>        |
| <span data-ttu-id="6ff58-124">Chave</span><span class="sxs-lookup"><span data-stu-id="6ff58-124">Key</span></span>         | [<span data-ttu-id="6ff58-125">Text</span><span class="sxs-lookup"><span data-stu-id="6ff58-125">Text</span></span>](text.md)             | <span data-ttu-id="6ff58-126">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-126">N</span></span>   | <span data-ttu-id="6ff58-127">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-127">N</span></span>        |
| <span data-ttu-id="6ff58-128">Campo</span><span class="sxs-lookup"><span data-stu-id="6ff58-128">Field</span></span>       | [<span data-ttu-id="6ff58-129">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6ff58-129">Integer</span></span>](integer.md)       | <span data-ttu-id="6ff58-130">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-130">N</span></span>   | <span data-ttu-id="6ff58-131">Y</span><span class="sxs-lookup"><span data-stu-id="6ff58-131">Y</span></span>        |
| <span data-ttu-id="6ff58-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ff58-132">Type</span></span>        | [<span data-ttu-id="6ff58-133">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6ff58-133">Integer</span></span>](integer.md)       | <span data-ttu-id="6ff58-134">N</span><span class="sxs-lookup"><span data-stu-id="6ff58-134">N</span></span>   | <span data-ttu-id="6ff58-135">S</span><span class="sxs-lookup"><span data-stu-id="6ff58-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6ff58-136">Colunas</span><span class="sxs-lookup"><span data-stu-id="6ff58-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6ff58-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="6ff58-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="6ff58-138">Uma chave externa na primeira coluna da tabela de [assinatura](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ff58-138">An external key into the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="6ff58-139">A assinatura \_ representa uma assinatura exclusiva e também é a chave externa na coluna um da tabela de assinatura.</span><span class="sxs-lookup"><span data-stu-id="6ff58-139">The Signature\_ represents a unique signature and is also the external key into column one of the Signature table.</span></span> <span data-ttu-id="6ff58-140">Se essa assinatura estiver presente na tabela de assinatura, a pesquisa será para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ff58-140">If this signature is present in the Signature table, then the search is for a file.</span></span> <span data-ttu-id="6ff58-141">Se essa chave estiver ausente da tabela de assinatura e o valor da coluna de tipo for **msidbLocatorTypeRawValue**, a pesquisa será para a entrada. ini especificada pela tabela IniLocator.</span><span class="sxs-lookup"><span data-stu-id="6ff58-141">If this key is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the .ini entry specified by the IniLocator table.</span></span> <span data-ttu-id="6ff58-142">Caso contrário, a pesquisa será para um diretório especificado pela tabela IniLocator.</span><span class="sxs-lookup"><span data-stu-id="6ff58-142">Otherwise the search is for a directory specified by the IniLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="6ff58-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="6ff58-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="6ff58-144">O nome do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="6ff58-144">The .ini file name.</span></span>

</dd> <dt>

<span data-ttu-id="6ff58-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span><span class="sxs-lookup"><span data-stu-id="6ff58-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="6ff58-146">Nome da seção dentro do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="6ff58-146">Section name within the .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="6ff58-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves</span><span class="sxs-lookup"><span data-stu-id="6ff58-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="6ff58-148">Valor da chave na seção.</span><span class="sxs-lookup"><span data-stu-id="6ff58-148">Key value within the section.</span></span>

</dd> <dt>

<span data-ttu-id="6ff58-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo</span><span class="sxs-lookup"><span data-stu-id="6ff58-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Field</span></span>
</dt> <dd>

<span data-ttu-id="6ff58-150">O campo na linha. ini.</span><span class="sxs-lookup"><span data-stu-id="6ff58-150">The field in the .ini line.</span></span> <span data-ttu-id="6ff58-151">Se o campo for nulo ou 0, a linha inteira será lida.</span><span class="sxs-lookup"><span data-stu-id="6ff58-151">If Field is Null or 0, then the entire line is read.</span></span> <span data-ttu-id="6ff58-152">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="6ff58-152">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="6ff58-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva</span><span class="sxs-lookup"><span data-stu-id="6ff58-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="6ff58-154">Um valor que determina se o valor de. ini é um local de arquivo, um local de diretório ou um valor RAW. ini.</span><span class="sxs-lookup"><span data-stu-id="6ff58-154">A value that determines whether the .ini value is a file location, a directory location, or raw .ini value.</span></span>

<span data-ttu-id="6ff58-155">A tabela a seguir lista os valores válidos.</span><span class="sxs-lookup"><span data-stu-id="6ff58-155">The following table lists valid values.</span></span> <span data-ttu-id="6ff58-156">Se estiver ausente, o tipo será definido como 1.</span><span class="sxs-lookup"><span data-stu-id="6ff58-156">If absent, Type is set to be 1.</span></span>



| <span data-ttu-id="6ff58-157">Constante</span><span class="sxs-lookup"><span data-stu-id="6ff58-157">Constant</span></span>                      | <span data-ttu-id="6ff58-158">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="6ff58-158">Hexadecimal</span></span> | <span data-ttu-id="6ff58-159">Decimal</span><span class="sxs-lookup"><span data-stu-id="6ff58-159">Decimal</span></span> | <span data-ttu-id="6ff58-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ff58-160">Description</span></span>           |
|-------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="6ff58-161">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="6ff58-161">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="6ff58-162">0x000</span><span class="sxs-lookup"><span data-stu-id="6ff58-162">0x000</span></span>       | <span data-ttu-id="6ff58-163">0</span><span class="sxs-lookup"><span data-stu-id="6ff58-163">0</span></span>       | <span data-ttu-id="6ff58-164">Um local do diretório.</span><span class="sxs-lookup"><span data-stu-id="6ff58-164">A directory location.</span></span> |
| <span data-ttu-id="6ff58-165">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="6ff58-165">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="6ff58-166">0x001</span><span class="sxs-lookup"><span data-stu-id="6ff58-166">0x001</span></span>       | <span data-ttu-id="6ff58-167">1</span><span class="sxs-lookup"><span data-stu-id="6ff58-167">1</span></span>       | <span data-ttu-id="6ff58-168">Um local de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ff58-168">A file location.</span></span>      |
| <span data-ttu-id="6ff58-169">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="6ff58-169">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="6ff58-170">0x002</span><span class="sxs-lookup"><span data-stu-id="6ff58-170">0x002</span></span>       | <span data-ttu-id="6ff58-171">2</span><span class="sxs-lookup"><span data-stu-id="6ff58-171">2</span></span>       | <span data-ttu-id="6ff58-172">Um valor RAW. ini.</span><span class="sxs-lookup"><span data-stu-id="6ff58-172">A raw .ini value.</span></span>     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ff58-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ff58-173">Remarks</span></span>

<span data-ttu-id="6ff58-174">Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ff58-174">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="6ff58-175">As colunas desta tabela geralmente não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="6ff58-175">This table's columns are generally not localized.</span></span> <span data-ttu-id="6ff58-176">Se um autor decidir procurar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="6ff58-176">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="6ff58-177">O texto localizado associado para exibição de progresso ou registro em log está especificado na [tabela ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ff58-177">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="6ff58-178">Consulte [pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="6ff58-178">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="6ff58-179">Validação</span><span class="sxs-lookup"><span data-stu-id="6ff58-179">Validation</span></span>

<dl>

[<span data-ttu-id="6ff58-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="6ff58-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6ff58-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="6ff58-181">ICE06</span></span>](ice06.md)  
</dl>

 

 



