---
description: A tabela de assinatura contém as informações que identificam exclusivamente uma assinatura de arquivo. Para obter mais informações sobre assinaturas, consulte assinaturas digitais e Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabela de assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759206"
---
# <a name="signature-table"></a><span data-ttu-id="25cc9-104">Tabela de assinatura</span><span class="sxs-lookup"><span data-stu-id="25cc9-104">Signature Table</span></span>

<span data-ttu-id="25cc9-105">A tabela de assinatura contém as informações que identificam exclusivamente uma assinatura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-105">The Signature table holds the information that uniquely identifies a file signature.</span></span> <span data-ttu-id="25cc9-106">Para obter mais informações sobre assinaturas [, consulte assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="25cc9-106">For more information regarding signatures see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="25cc9-107">A tabela de assinatura tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="25cc9-107">The Signature table has the following columns.</span></span>



| <span data-ttu-id="25cc9-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="25cc9-108">Column</span></span>     | <span data-ttu-id="25cc9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="25cc9-109">Type</span></span>                               | <span data-ttu-id="25cc9-110">Chave</span><span class="sxs-lookup"><span data-stu-id="25cc9-110">Key</span></span> | <span data-ttu-id="25cc9-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="25cc9-111">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="25cc9-112">Assinatura</span><span class="sxs-lookup"><span data-stu-id="25cc9-112">Signature</span></span>  | [<span data-ttu-id="25cc9-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="25cc9-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="25cc9-114">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-114">Y</span></span>   | <span data-ttu-id="25cc9-115">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-115">N</span></span>        |
| <span data-ttu-id="25cc9-116">FileName</span><span class="sxs-lookup"><span data-stu-id="25cc9-116">FileName</span></span>   | [<span data-ttu-id="25cc9-117">Text</span><span class="sxs-lookup"><span data-stu-id="25cc9-117">Text</span></span>](text.md)                   | <span data-ttu-id="25cc9-118">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-118">N</span></span>   | <span data-ttu-id="25cc9-119">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-119">N</span></span>        |
| <span data-ttu-id="25cc9-120">MinVersion</span><span class="sxs-lookup"><span data-stu-id="25cc9-120">MinVersion</span></span> | [<span data-ttu-id="25cc9-121">Text</span><span class="sxs-lookup"><span data-stu-id="25cc9-121">Text</span></span>](text.md)                   | <span data-ttu-id="25cc9-122">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-122">N</span></span>   | <span data-ttu-id="25cc9-123">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-123">Y</span></span>        |
| <span data-ttu-id="25cc9-124">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="25cc9-124">MaxVersion</span></span> | [<span data-ttu-id="25cc9-125">Text</span><span class="sxs-lookup"><span data-stu-id="25cc9-125">Text</span></span>](text.md)                   | <span data-ttu-id="25cc9-126">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-126">N</span></span>   | <span data-ttu-id="25cc9-127">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-127">Y</span></span>        |
| <span data-ttu-id="25cc9-128">MinSize</span><span class="sxs-lookup"><span data-stu-id="25cc9-128">MinSize</span></span>    | [<span data-ttu-id="25cc9-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="25cc9-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="25cc9-130">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-130">N</span></span>   | <span data-ttu-id="25cc9-131">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-131">Y</span></span>        |
| <span data-ttu-id="25cc9-132">MaxSize</span><span class="sxs-lookup"><span data-stu-id="25cc9-132">MaxSize</span></span>    | [<span data-ttu-id="25cc9-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="25cc9-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="25cc9-134">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-134">N</span></span>   | <span data-ttu-id="25cc9-135">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-135">Y</span></span>        |
| <span data-ttu-id="25cc9-136">Lembre-se</span><span class="sxs-lookup"><span data-stu-id="25cc9-136">MinDate</span></span>    | [<span data-ttu-id="25cc9-137">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="25cc9-137">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="25cc9-138">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-138">N</span></span>   | <span data-ttu-id="25cc9-139">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-139">Y</span></span>        |
| <span data-ttu-id="25cc9-140">MaxDate</span><span class="sxs-lookup"><span data-stu-id="25cc9-140">MaxDate</span></span>    | [<span data-ttu-id="25cc9-141">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="25cc9-141">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="25cc9-142">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-142">N</span></span>   | <span data-ttu-id="25cc9-143">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-143">Y</span></span>        |
| <span data-ttu-id="25cc9-144">Idiomas</span><span class="sxs-lookup"><span data-stu-id="25cc9-144">Languages</span></span>  | [<span data-ttu-id="25cc9-145">Text</span><span class="sxs-lookup"><span data-stu-id="25cc9-145">Text</span></span>](text.md)                   | <span data-ttu-id="25cc9-146">N</span><span class="sxs-lookup"><span data-stu-id="25cc9-146">N</span></span>   | <span data-ttu-id="25cc9-147">S</span><span class="sxs-lookup"><span data-stu-id="25cc9-147">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="25cc9-148">Colunas</span><span class="sxs-lookup"><span data-stu-id="25cc9-148">Columns</span></span>

<dl> <dt>

<span data-ttu-id="25cc9-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span><span class="sxs-lookup"><span data-stu-id="25cc9-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-150">A coluna de assinatura é uma assinatura de arquivo exclusiva.</span><span class="sxs-lookup"><span data-stu-id="25cc9-150">The Signature column is a unique file signature.</span></span>

</dd> <dt>

<span data-ttu-id="25cc9-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="25cc9-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-152">O nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-152">The name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="25cc9-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span><span class="sxs-lookup"><span data-stu-id="25cc9-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-154">A versão mínima do arquivo, com uma comparação de idioma.</span><span class="sxs-lookup"><span data-stu-id="25cc9-154">The minimum version of the file, with a language comparison.</span></span> <span data-ttu-id="25cc9-155">Se esse campo for especificado, o arquivo deverá ter uma versão que seja pelo menos igual a MinVersion.</span><span class="sxs-lookup"><span data-stu-id="25cc9-155">If this field is specified, then the file must have a version that is at least equal to MinVersion.</span></span> <span data-ttu-id="25cc9-156">Se o arquivo tiver uma versão igual ao valor do campo MinVersion, mas o idioma especificado na coluna idiomas for diferente, o arquivo não atenderá aos critérios do filtro de assinatura.</span><span class="sxs-lookup"><span data-stu-id="25cc9-156">If the file has an equal version to the MinVersion field value but the language specified in the Languages column differs, the file does not satisfy the signature filter criteria.</span></span>

> [!Note]  
> <span data-ttu-id="25cc9-157">O idioma especificado na coluna idiomas é usado na comparação e não há como ignorar o idioma.</span><span class="sxs-lookup"><span data-stu-id="25cc9-157">The language specified in the Languages column is used in the comparison and there is no way to ignore language.</span></span> <span data-ttu-id="25cc9-158">Se desejar que um arquivo atenda ao requisito de campo MinVersion independentemente da linguagem, você deverá inserir um valor no campo MinVersion que seja menor que o valor real.</span><span class="sxs-lookup"><span data-stu-id="25cc9-158">If you want a file to meet the MinVersion field requirement regardless of language, you must enter a value in the MinVersion field that is one less than the actual value.</span></span> <span data-ttu-id="25cc9-159">Por exemplo, se a versão mínima para o filtro for 2.0.2600.1183, use 2.0.2600.1182 para localizar o arquivo sem corresponder às informações de idioma.</span><span class="sxs-lookup"><span data-stu-id="25cc9-159">For example, if the minimum version for the filter is 2.0.2600.1183, use 2.0.2600.1182 to find the file without matching the language information.</span></span>

 

</dd> <dt>

<span data-ttu-id="25cc9-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span><span class="sxs-lookup"><span data-stu-id="25cc9-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-161">A versão máxima do arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-161">The maximum version of the file.</span></span> <span data-ttu-id="25cc9-162">Se esse campo for especificado, o arquivo deverá ter uma versão que seja, no máximo, igual a MaxVersion.</span><span class="sxs-lookup"><span data-stu-id="25cc9-162">If this field is specified, then the file must have a version that is at most equal to MaxVersion.</span></span>

</dd> <dt>

<span data-ttu-id="25cc9-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span><span class="sxs-lookup"><span data-stu-id="25cc9-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-164">O tamanho mínimo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-164">The minimum size of the file.</span></span> <span data-ttu-id="25cc9-165">Se esse campo for especificado, o arquivo em inspeção deverá ter um tamanho que seja, pelo menos, igual a MinSize.</span><span class="sxs-lookup"><span data-stu-id="25cc9-165">If this field is specified, then the file under inspection must have a size that is at least equal to MinSize.</span></span> <span data-ttu-id="25cc9-166">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-166">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="25cc9-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span><span class="sxs-lookup"><span data-stu-id="25cc9-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-168">O tamanho máximo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-168">The maximum size of the file.</span></span> <span data-ttu-id="25cc9-169">Se esse campo for especificado, o arquivo em inspeção deverá ter um tamanho que seja, no máximo, igual a MaxSize.</span><span class="sxs-lookup"><span data-stu-id="25cc9-169">If this field is specified, then the file under inspection must have a size that is at most equal to MaxSize.</span></span> <span data-ttu-id="25cc9-170">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-170">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="25cc9-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>Lembre-se</span><span class="sxs-lookup"><span data-stu-id="25cc9-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-172">A data e a hora mínimas de modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-172">The minimum modification date and time of the file.</span></span> <span data-ttu-id="25cc9-173">Se esse campo for especificado, o arquivo em inspeção deverá ter uma data e hora de modificação que seja, pelo menos, igual a.</span><span class="sxs-lookup"><span data-stu-id="25cc9-173">If this field is specified, then the file under inspection must have a modification date and time that is at least equal to MinDate.</span></span> <span data-ttu-id="25cc9-174">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-174">This must be a non-negative number.</span></span> <span data-ttu-id="25cc9-175">O formato desse campo é dois valores de 16 bits empacotados do tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="25cc9-175">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="25cc9-176">O valor de **palavra** de ordem superior especifica a data no formato de data do MS-dos.</span><span class="sxs-lookup"><span data-stu-id="25cc9-176">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="25cc9-177">O valor de **palavra** de ordem inferior Especifica a hora no formato de hora do MS-dos.</span><span class="sxs-lookup"><span data-stu-id="25cc9-177">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="25cc9-178">Um valor de 0 para o valor de hora representa meia-noite.</span><span class="sxs-lookup"><span data-stu-id="25cc9-178">A value of 0 for the time value represents midnight.</span></span> <span data-ttu-id="25cc9-179">Consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="25cc9-179">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="25cc9-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span><span class="sxs-lookup"><span data-stu-id="25cc9-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-181">A data de criação máxima do arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-181">The maximum creation date of the file.</span></span> <span data-ttu-id="25cc9-182">Se esse campo for especificado, o arquivo em inspeção deverá ter uma data de criação que seja, no máximo, igual a MaxDate.</span><span class="sxs-lookup"><span data-stu-id="25cc9-182">If this field is specified, then the file under inspection must have a creation date that is at most equal to MaxDate.</span></span> <span data-ttu-id="25cc9-183">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-183">This must be a non-negative number.</span></span> <span data-ttu-id="25cc9-184">O formato desse campo é dois valores de 16 bits empacotados do tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="25cc9-184">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="25cc9-185">O valor de **palavra** de ordem superior especifica a data no formato de data do MS-dos.</span><span class="sxs-lookup"><span data-stu-id="25cc9-185">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="25cc9-186">O valor de **palavra** de ordem inferior Especifica a hora no formato de hora do MS-dos.</span><span class="sxs-lookup"><span data-stu-id="25cc9-186">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="25cc9-187">Um valor de 0 para o valor de tempo representa meia-noite.</span><span class="sxs-lookup"><span data-stu-id="25cc9-187">A value of 0 for the time value represent midnight.</span></span> <span data-ttu-id="25cc9-188">Consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="25cc9-188">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="25cc9-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Idiomas</span><span class="sxs-lookup"><span data-stu-id="25cc9-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Languages</span></span>
</dt> <dd>

<span data-ttu-id="25cc9-190">Os idiomas com suporte no arquivo.</span><span class="sxs-lookup"><span data-stu-id="25cc9-190">The languages supported by the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25cc9-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="25cc9-191">Remarks</span></span>

<span data-ttu-id="25cc9-192">Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="25cc9-192">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="25cc9-193">A assinatura é pesquisada usando a [tabela RegLocator](reglocator-table.md), a [tabela IniLocator](inilocator-table.md), a [tabela CompLocator](complocator-table.md)e a [tabela DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="25cc9-193">The signature is searched for using the [RegLocator table](reglocator-table.md), the [IniLocator table](inilocator-table.md), the [CompLocator table](complocator-table.md), and the [DrLocator table](drlocator-table.md).</span></span> <span data-ttu-id="25cc9-194">As colunas desta tabela geralmente não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="25cc9-194">This table's columns are generally not localized.</span></span> <span data-ttu-id="25cc9-195">Se um autor decidir procurar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="25cc9-195">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="25cc9-196">A tabela de assinatura geralmente segue as Windows Installer [regras de controle de versão do arquivo](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="25cc9-196">The Signature table generally follows the Windows Installer [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="25cc9-197">Os idiomas especificados na coluna idiomas da tabela de assinatura não são avaliados, a menos que as versões de arquivo sejam equivalentes.</span><span class="sxs-lookup"><span data-stu-id="25cc9-197">Languages specified in the Languages column of the Signature table are not evaluated unless the file versions are equivalent.</span></span> <span data-ttu-id="25cc9-198">A coluna idiomas garantirá que um arquivo seja de um idioma específico se for da versão solicitada.</span><span class="sxs-lookup"><span data-stu-id="25cc9-198">The Languages column will ensure that a file is of a particular language if it is of the requested version.</span></span> <span data-ttu-id="25cc9-199">Não há nenhum método disponível para ignorar a coluna de idiomas.</span><span class="sxs-lookup"><span data-stu-id="25cc9-199">There is no method available to ignore the Languages column.</span></span> <span data-ttu-id="25cc9-200">Um valor nulo inserido na coluna idiomas é tratado como um arquivo sem idioma e não corresponde à assinatura de arquivo de um arquivo com uma linguagem que aparece na tabela de assinatura.</span><span class="sxs-lookup"><span data-stu-id="25cc9-200">A NULL value entered in the Languages column is treated as a file without a language and does not match the file signature of a file with a language appearing in the Signature table.</span></span> <span data-ttu-id="25cc9-201">O exemplo a seguir pesquisa uma versão específica do MSI.DLL.</span><span class="sxs-lookup"><span data-stu-id="25cc9-201">The following example searches for a particular version of MSI.DLL.</span></span>

[<span data-ttu-id="25cc9-202">Tabela DrLocator</span><span class="sxs-lookup"><span data-stu-id="25cc9-202">DrLocator table</span></span>](drlocator-table.md)

| <span data-ttu-id="25cc9-203">Signature\_</span><span class="sxs-lookup"><span data-stu-id="25cc9-203">Signature\_</span></span> | <span data-ttu-id="25cc9-204">Pai</span><span class="sxs-lookup"><span data-stu-id="25cc9-204">Parent</span></span> | <span data-ttu-id="25cc9-205">Caminho</span><span class="sxs-lookup"><span data-stu-id="25cc9-205">Path</span></span>                  | <span data-ttu-id="25cc9-206">Profundidade</span><span class="sxs-lookup"><span data-stu-id="25cc9-206">Depth</span></span> |
|-------------|--------|-----------------------|-------|
| <span data-ttu-id="25cc9-207">MsiDll</span><span class="sxs-lookup"><span data-stu-id="25cc9-207">MsiDll</span></span>      | <span data-ttu-id="25cc9-208">nulo</span><span class="sxs-lookup"><span data-stu-id="25cc9-208">{null}</span></span> | <span data-ttu-id="25cc9-209">c: \\ Windows \\ System32</span><span class="sxs-lookup"><span data-stu-id="25cc9-209">c:\\windows\\system32</span></span> | <span data-ttu-id="25cc9-210">0</span><span class="sxs-lookup"><span data-stu-id="25cc9-210">0</span></span>     |



 

[<span data-ttu-id="25cc9-211">Tabela AppSearch</span><span class="sxs-lookup"><span data-stu-id="25cc9-211">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="25cc9-212">Propriedade</span><span class="sxs-lookup"><span data-stu-id="25cc9-212">Property</span></span> | <span data-ttu-id="25cc9-213">Signature\_</span><span class="sxs-lookup"><span data-stu-id="25cc9-213">Signature\_</span></span> |
|----------|-------------|
| <span data-ttu-id="25cc9-214">MSIDLL</span><span class="sxs-lookup"><span data-stu-id="25cc9-214">MSIDLL</span></span>   | <span data-ttu-id="25cc9-215">MsiDll</span><span class="sxs-lookup"><span data-stu-id="25cc9-215">MsiDll</span></span>      |



 

<span data-ttu-id="25cc9-216">Tabela de assinatura</span><span class="sxs-lookup"><span data-stu-id="25cc9-216">Signature table</span></span>



| <span data-ttu-id="25cc9-217">Assinatura</span><span class="sxs-lookup"><span data-stu-id="25cc9-217">Signature</span></span> | <span data-ttu-id="25cc9-218">FileName</span><span class="sxs-lookup"><span data-stu-id="25cc9-218">FileName</span></span> | <span data-ttu-id="25cc9-219">MinVersion</span><span class="sxs-lookup"><span data-stu-id="25cc9-219">MinVersion</span></span>    | <span data-ttu-id="25cc9-220">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="25cc9-220">MaxVersion</span></span> | <span data-ttu-id="25cc9-221">MinSize</span><span class="sxs-lookup"><span data-stu-id="25cc9-221">MinSize</span></span> | <span data-ttu-id="25cc9-222">MaxSize</span><span class="sxs-lookup"><span data-stu-id="25cc9-222">MaxSize</span></span> | <span data-ttu-id="25cc9-223">Lembre-se</span><span class="sxs-lookup"><span data-stu-id="25cc9-223">MinDate</span></span> | <span data-ttu-id="25cc9-224">MaxDate</span><span class="sxs-lookup"><span data-stu-id="25cc9-224">MaxDate</span></span> | <span data-ttu-id="25cc9-225">Idiomas</span><span class="sxs-lookup"><span data-stu-id="25cc9-225">Languages</span></span> |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| <span data-ttu-id="25cc9-226">MsiDll</span><span class="sxs-lookup"><span data-stu-id="25cc9-226">MsiDll</span></span>    | <span data-ttu-id="25cc9-227">msi.dll</span><span class="sxs-lookup"><span data-stu-id="25cc9-227">msi.dll</span></span>  | <span data-ttu-id="25cc9-228">2.0.2600.1106</span><span class="sxs-lookup"><span data-stu-id="25cc9-228">2.0.2600.1106</span></span> | <span data-ttu-id="25cc9-229">nulo</span><span class="sxs-lookup"><span data-stu-id="25cc9-229">{null}</span></span>     | <span data-ttu-id="25cc9-230">nulo</span><span class="sxs-lookup"><span data-stu-id="25cc9-230">{null}</span></span>  | <span data-ttu-id="25cc9-231">nulo</span><span class="sxs-lookup"><span data-stu-id="25cc9-231">{null}</span></span>  | <span data-ttu-id="25cc9-232">nulo</span><span class="sxs-lookup"><span data-stu-id="25cc9-232">{null}</span></span>  | <span data-ttu-id="25cc9-233">nulo</span><span class="sxs-lookup"><span data-stu-id="25cc9-233">{null}</span></span>  | <span data-ttu-id="25cc9-234">0</span><span class="sxs-lookup"><span data-stu-id="25cc9-234">0</span></span>         |



 

<span data-ttu-id="25cc9-235">Nesse caso, e no Windows XP SP1, a [ação AppSearch](appsearch-action.md) define MSIDLL como c: \\ Windows \\ System32 \\msi.dll porque MSI.DLL é um arquivo de idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="25cc9-235">In this case, and on Windows XP SP1, the [AppSearch action](appsearch-action.md) sets MSIDLL to c:\\windows\\system32\\msi.dll because MSI.DLL is a language neutral file.</span></span> <span data-ttu-id="25cc9-236">Se o valor da coluna languages for alterado de 0 para 1033, a ação AppSearch falhará ao localizar o msi.dll correspondente e a propriedade MSIDLL será indefinida.</span><span class="sxs-lookup"><span data-stu-id="25cc9-236">If the value of the Languages column is changed from 0 to 1033, then the AppSearch action fails to find the matching msi.dll and the MSIDLL property is undefined.</span></span>

<span data-ttu-id="25cc9-237">Você não pode usar a tabela de assinatura para consultar apenas os idiomas.</span><span class="sxs-lookup"><span data-stu-id="25cc9-237">You cannot use the Signature table to query on languages alone.</span></span> <span data-ttu-id="25cc9-238">Para pesquisar versões de idioma diferentes de um arquivo, você deve ter uma entrada separada na tabela de assinatura para cada versão de idioma.</span><span class="sxs-lookup"><span data-stu-id="25cc9-238">To search for different language versions of a file, you must have a separate entry in the Signature table for each language version.</span></span> <span data-ttu-id="25cc9-239">Se vários idiomas forem fornecidos na coluna idiomas, a pesquisa será para um arquivo que dá suporte a todos esses idiomas.</span><span class="sxs-lookup"><span data-stu-id="25cc9-239">If multiple languages are provided in the Languages column, then the search is for a file that supports all of those languages.</span></span>

<span data-ttu-id="25cc9-240">O formato das colunas mental e MaxDate são dois valores de 16 bits empacotados do tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="25cc9-240">The format of MinDate and MaxDate columns are two packed 16-bit values of type **WORD**.</span></span>

<span data-ttu-id="25cc9-241">**Palavra** de data</span><span class="sxs-lookup"><span data-stu-id="25cc9-241">Date **WORD**</span></span>



| <span data-ttu-id="25cc9-242">Bits</span><span class="sxs-lookup"><span data-stu-id="25cc9-242">Bits</span></span> | <span data-ttu-id="25cc9-243">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="25cc9-243">Content</span></span>                                             |
|------|-----------------------------------------------------|
| <span data-ttu-id="25cc9-244">0 a 4</span><span class="sxs-lookup"><span data-stu-id="25cc9-244">0–4</span></span>  | <span data-ttu-id="25cc9-245">Dia do mês (1-31)</span><span class="sxs-lookup"><span data-stu-id="25cc9-245">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="25cc9-246">5-8</span><span class="sxs-lookup"><span data-stu-id="25cc9-246">5-8</span></span>  | <span data-ttu-id="25cc9-247">Mês (1 = Janeiro, 2 = fevereiro e assim por diante)</span><span class="sxs-lookup"><span data-stu-id="25cc9-247">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="25cc9-248">9-15</span><span class="sxs-lookup"><span data-stu-id="25cc9-248">9-15</span></span> | <span data-ttu-id="25cc9-249">Deslocamento de ano de 1980 (adicione 1980 para obter o ano real)</span><span class="sxs-lookup"><span data-stu-id="25cc9-249">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

<span data-ttu-id="25cc9-250">Hora da **palavra**</span><span class="sxs-lookup"><span data-stu-id="25cc9-250">Time **WORD**</span></span>



| <span data-ttu-id="25cc9-251">Bits</span><span class="sxs-lookup"><span data-stu-id="25cc9-251">Bits</span></span>  | <span data-ttu-id="25cc9-252">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="25cc9-252">Content</span></span>                     |
|-------|-----------------------------|
| <span data-ttu-id="25cc9-253">0 a 4</span><span class="sxs-lookup"><span data-stu-id="25cc9-253">0–4</span></span>   | <span data-ttu-id="25cc9-254">Segundos dividido por 2</span><span class="sxs-lookup"><span data-stu-id="25cc9-254">Seconds divided by 2</span></span>        |
| <span data-ttu-id="25cc9-255">5-10</span><span class="sxs-lookup"><span data-stu-id="25cc9-255">5-10</span></span>  | <span data-ttu-id="25cc9-256">Minutos (0-59)</span><span class="sxs-lookup"><span data-stu-id="25cc9-256">Minutes (0-59)</span></span>              |
| <span data-ttu-id="25cc9-257">11-15</span><span class="sxs-lookup"><span data-stu-id="25cc9-257">11-15</span></span> | <span data-ttu-id="25cc9-258">Hora (0-23 no relógio de 24 horas)</span><span class="sxs-lookup"><span data-stu-id="25cc9-258">Hour(0-23 on 24 hour clock)</span></span> |



 

<span data-ttu-id="25cc9-259">A fórmula para calcular os valores de campo mentale e MaxDate é:</span><span class="sxs-lookup"><span data-stu-id="25cc9-259">The formula for calculating the MinDate and MaxDate field values is:</span></span>

<span data-ttu-id="25cc9-260">(Ano-1980) \* 512 + mês \* 32 + dia) \* 65536 + horas \* 2048 + minutos \* 32 + segundos/2</span><span class="sxs-lookup"><span data-stu-id="25cc9-260">( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2</span></span>

## <a name="validation"></a><span data-ttu-id="25cc9-261">Validação</span><span class="sxs-lookup"><span data-stu-id="25cc9-261">Validation</span></span>

<dl>

[<span data-ttu-id="25cc9-262">ICE03</span><span class="sxs-lookup"><span data-stu-id="25cc9-262">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="25cc9-263">ICE06</span><span class="sxs-lookup"><span data-stu-id="25cc9-263">ICE06</span></span>](ice06.md)  
</dl>

 

 



