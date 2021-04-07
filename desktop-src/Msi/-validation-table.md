---
description: A \_ tabela de validação é uma tabela do sistema que contém os nomes de coluna e os valores de coluna para todas as tabelas no banco de dados.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: Tabela de _Validation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828101"
---
# <a name="_validation-table"></a><span data-ttu-id="a4030-103">\_Tabela de validação</span><span class="sxs-lookup"><span data-stu-id="a4030-103">\_Validation Table</span></span>

<span data-ttu-id="a4030-104">A \_ tabela de validação é uma tabela do sistema que contém os nomes de coluna e os valores de coluna para todas as tabelas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a4030-104">The \_Validation table is a system table that contains the column names and the column values for all of the tables in the database.</span></span> <span data-ttu-id="a4030-105">Ele é usado durante o processo de validação do banco de dados para garantir que todas as colunas sejam contadas e tenham os valores corretos.</span><span class="sxs-lookup"><span data-stu-id="a4030-105">It is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="a4030-106">Esta tabela não é enviada com o banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="a4030-106">This table is not shipped with the installer database.</span></span>

<span data-ttu-id="a4030-107">A \_ tabela de validação tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4030-107">The \_Validation table has the following columns.</span></span>



| <span data-ttu-id="a4030-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="a4030-108">Column</span></span>      | <span data-ttu-id="a4030-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4030-109">Type</span></span>                               | <span data-ttu-id="a4030-110">Chave</span><span class="sxs-lookup"><span data-stu-id="a4030-110">Key</span></span> | <span data-ttu-id="a4030-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a4030-111">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="a4030-112">Tabela</span><span class="sxs-lookup"><span data-stu-id="a4030-112">Table</span></span>       | [<span data-ttu-id="a4030-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="a4030-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="a4030-114">S</span><span class="sxs-lookup"><span data-stu-id="a4030-114">Y</span></span>   | <span data-ttu-id="a4030-115">N</span><span class="sxs-lookup"><span data-stu-id="a4030-115">N</span></span>        |
| <span data-ttu-id="a4030-116">Coluna</span><span class="sxs-lookup"><span data-stu-id="a4030-116">Column</span></span>      | [<span data-ttu-id="a4030-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="a4030-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="a4030-118">S</span><span class="sxs-lookup"><span data-stu-id="a4030-118">Y</span></span>   | <span data-ttu-id="a4030-119">N</span><span class="sxs-lookup"><span data-stu-id="a4030-119">N</span></span>        |
| <span data-ttu-id="a4030-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="a4030-120">Nullable</span></span>    | [<span data-ttu-id="a4030-121">Text</span><span class="sxs-lookup"><span data-stu-id="a4030-121">Text</span></span>](text.md)                   | <span data-ttu-id="a4030-122">N</span><span class="sxs-lookup"><span data-stu-id="a4030-122">N</span></span>   | <span data-ttu-id="a4030-123">N</span><span class="sxs-lookup"><span data-stu-id="a4030-123">N</span></span>        |
| <span data-ttu-id="a4030-124">MinValue</span><span class="sxs-lookup"><span data-stu-id="a4030-124">MinValue</span></span>    | [<span data-ttu-id="a4030-125">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a4030-125">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a4030-126">N</span><span class="sxs-lookup"><span data-stu-id="a4030-126">N</span></span>   | <span data-ttu-id="a4030-127">S</span><span class="sxs-lookup"><span data-stu-id="a4030-127">Y</span></span>        |
| <span data-ttu-id="a4030-128">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a4030-128">MaxValue</span></span>    | [<span data-ttu-id="a4030-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a4030-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a4030-130">N</span><span class="sxs-lookup"><span data-stu-id="a4030-130">N</span></span>   | <span data-ttu-id="a4030-131">S</span><span class="sxs-lookup"><span data-stu-id="a4030-131">Y</span></span>        |
| <span data-ttu-id="a4030-132">KeyTable</span><span class="sxs-lookup"><span data-stu-id="a4030-132">KeyTable</span></span>    | [<span data-ttu-id="a4030-133">Identificador</span><span class="sxs-lookup"><span data-stu-id="a4030-133">Identifier</span></span>](identifier.md)       | <span data-ttu-id="a4030-134">N</span><span class="sxs-lookup"><span data-stu-id="a4030-134">N</span></span>   | <span data-ttu-id="a4030-135">S</span><span class="sxs-lookup"><span data-stu-id="a4030-135">Y</span></span>        |
| <span data-ttu-id="a4030-136">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="a4030-136">KeyColumn</span></span>   | [<span data-ttu-id="a4030-137">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a4030-137">Integer</span></span>](integer.md)             | <span data-ttu-id="a4030-138">N</span><span class="sxs-lookup"><span data-stu-id="a4030-138">N</span></span>   | <span data-ttu-id="a4030-139">S</span><span class="sxs-lookup"><span data-stu-id="a4030-139">Y</span></span>        |
| <span data-ttu-id="a4030-140">Categoria</span><span class="sxs-lookup"><span data-stu-id="a4030-140">Category</span></span>    | [<span data-ttu-id="a4030-141">Text</span><span class="sxs-lookup"><span data-stu-id="a4030-141">Text</span></span>](text.md)                   | <span data-ttu-id="a4030-142">N</span><span class="sxs-lookup"><span data-stu-id="a4030-142">N</span></span>   | <span data-ttu-id="a4030-143">S</span><span class="sxs-lookup"><span data-stu-id="a4030-143">Y</span></span>        |
| <span data-ttu-id="a4030-144">Definir</span><span class="sxs-lookup"><span data-stu-id="a4030-144">Set</span></span>         | [<span data-ttu-id="a4030-145">Text</span><span class="sxs-lookup"><span data-stu-id="a4030-145">Text</span></span>](text.md)                   | <span data-ttu-id="a4030-146">N</span><span class="sxs-lookup"><span data-stu-id="a4030-146">N</span></span>   | <span data-ttu-id="a4030-147">S</span><span class="sxs-lookup"><span data-stu-id="a4030-147">Y</span></span>        |
| <span data-ttu-id="a4030-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4030-148">Description</span></span> | [<span data-ttu-id="a4030-149">Text</span><span class="sxs-lookup"><span data-stu-id="a4030-149">Text</span></span>](text.md)                   | <span data-ttu-id="a4030-150">N</span><span class="sxs-lookup"><span data-stu-id="a4030-150">N</span></span>   | <span data-ttu-id="a4030-151">S</span><span class="sxs-lookup"><span data-stu-id="a4030-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a4030-152">Colunas</span><span class="sxs-lookup"><span data-stu-id="a4030-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a4030-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="a4030-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="a4030-154">Usado para identificar uma tabela específica.</span><span class="sxs-lookup"><span data-stu-id="a4030-154">Used to identify a particular table.</span></span> <span data-ttu-id="a4030-155">Essa chave e a chave de coluna formam a chave primária da \_ tabela de validação.</span><span class="sxs-lookup"><span data-stu-id="a4030-155">This key and the Column key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="a4030-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Pilha</span><span class="sxs-lookup"><span data-stu-id="a4030-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="a4030-157">Usado para identificar uma coluna específica da tabela.</span><span class="sxs-lookup"><span data-stu-id="a4030-157">Used to identify a particular column of the table.</span></span> <span data-ttu-id="a4030-158">Essa chave e a chave de tabela formam a chave primária da \_ tabela de validação.</span><span class="sxs-lookup"><span data-stu-id="a4030-158">This key and the Table key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="a4030-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Anula</span><span class="sxs-lookup"><span data-stu-id="a4030-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span></span>
</dt> <dd>

<span data-ttu-id="a4030-160">Identifica se a coluna pode conter um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="a4030-160">Identifies whether the column may contain a Null value.</span></span>

<span data-ttu-id="a4030-161">Essa coluna pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4030-161">This column may have one of the following values.</span></span>



| <span data-ttu-id="a4030-162">String</span><span class="sxs-lookup"><span data-stu-id="a4030-162">String</span></span> | <span data-ttu-id="a4030-163">Significado</span><span class="sxs-lookup"><span data-stu-id="a4030-163">Meaning</span></span>                                   |
|--------|-------------------------------------------|
| <span data-ttu-id="a4030-164">S</span><span class="sxs-lookup"><span data-stu-id="a4030-164">Y</span></span>      | <span data-ttu-id="a4030-165">Sim, a coluna pode ter um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="a4030-165">Yes, the column may have a Null value.</span></span>    |
| <span data-ttu-id="a4030-166">N</span><span class="sxs-lookup"><span data-stu-id="a4030-166">N</span></span>      | <span data-ttu-id="a4030-167">Não, a coluna pode não ter um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="a4030-167">No, the column may not have a Null value.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a4030-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span><span class="sxs-lookup"><span data-stu-id="a4030-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span></span>
</dt> <dd>

<span data-ttu-id="a4030-169">Este campo se aplica a colunas com valor numérico.</span><span class="sxs-lookup"><span data-stu-id="a4030-169">This field applies to columns having numeric value.</span></span> <span data-ttu-id="a4030-170">O campo contém o valor mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="a4030-170">The field contains the minimum permissible value.</span></span> <span data-ttu-id="a4030-171">Esse pode ser o valor mínimo de um inteiro ou o valor mínimo para uma cadeia de caracteres de data ou versão.</span><span class="sxs-lookup"><span data-stu-id="a4030-171">This can be the minimum value for an integer or the minimum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="a4030-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span><span class="sxs-lookup"><span data-stu-id="a4030-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span></span>
</dt> <dd>

<span data-ttu-id="a4030-173">Este campo se aplica a colunas com valor numérico.</span><span class="sxs-lookup"><span data-stu-id="a4030-173">This field applies to columns having numeric value.</span></span> <span data-ttu-id="a4030-174">O campo é o valor máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="a4030-174">The field is the maximum permissible value.</span></span> <span data-ttu-id="a4030-175">Esse pode ser o valor máximo de um inteiro ou o valor máximo para uma cadeia de caracteres de data ou versão.</span><span class="sxs-lookup"><span data-stu-id="a4030-175">This may be the maximum value for an integer or the maximum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="a4030-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span><span class="sxs-lookup"><span data-stu-id="a4030-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span></span>
</dt> <dd>

<span data-ttu-id="a4030-177">Esse campo se aplica a colunas que são chaves externas.</span><span class="sxs-lookup"><span data-stu-id="a4030-177">This field applies to columns that are external keys.</span></span> <span data-ttu-id="a4030-178">O campo identificado na coluna deve ser vinculado ao número da coluna especificado por KeyColumn na tabela chamada em keyTable.</span><span class="sxs-lookup"><span data-stu-id="a4030-178">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="a4030-179">Isso pode ser uma lista de tabelas separadas por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="a4030-179">This can be a list of tables separated by semicolons.</span></span>

</dd> <dt>

<span data-ttu-id="a4030-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span><span class="sxs-lookup"><span data-stu-id="a4030-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span></span>
</dt> <dd>

<span data-ttu-id="a4030-181">Esse campo se aplica a colunas de tabela que são chaves externas.</span><span class="sxs-lookup"><span data-stu-id="a4030-181">This field applies to table columns that are external keys.</span></span> <span data-ttu-id="a4030-182">O campo identificado na coluna deve ser vinculado ao número da coluna especificado por KeyColumn na tabela chamada em keyTable.</span><span class="sxs-lookup"><span data-stu-id="a4030-182">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="a4030-183">O intervalo permitido do campo KeyColumn é 1-32.</span><span class="sxs-lookup"><span data-stu-id="a4030-183">The permissible range of the KeyColumn field is 1-32.</span></span>

</dd> <dt>

<span data-ttu-id="a4030-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias</span><span class="sxs-lookup"><span data-stu-id="a4030-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="a4030-185">Esse é o tipo de dados contidos no campo de banco de dado especificado pelas colunas de tabela e coluna da \_ tabela de validação.</span><span class="sxs-lookup"><span data-stu-id="a4030-185">This is the type of data contained by the database field specified by the Table and Column columns of the \_Validation table.</span></span> <span data-ttu-id="a4030-186">Se for um tipo com um valor numérico, como [Integer](integer.md), [DoubleInteger](doubleinteger.md) ou [Time/Date](time-date.md), insira NULL nesse campo e especifique o intervalo do valor usando as colunas MinValue e MaxValue.</span><span class="sxs-lookup"><span data-stu-id="a4030-186">If this is a type having a numeric value, such as [Integer](integer.md), [DoubleInteger](doubleinteger.md) or [Time/Date](time-date.md), then enter null into this field and specify the value's range using the MinValue and MaxValue columns.</span></span> <span data-ttu-id="a4030-187">Use a coluna categoria para especificar os tipos de dados não numéricos descritos em [tipos de dados de coluna](column-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="a4030-187">Use the Category column to specify the non-numeric data types described in [Column Data Types](column-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4030-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Definição</span><span class="sxs-lookup"><span data-stu-id="a4030-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span></span>
</dt> <dd>

<span data-ttu-id="a4030-189">Esta é uma lista de valores permitidos para este campo separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="a4030-189">This is a list of permissible values for this field separated by semicolons.</span></span> <span data-ttu-id="a4030-190">Esse campo é geralmente usado para enumerações.</span><span class="sxs-lookup"><span data-stu-id="a4030-190">This field is usually used for enumerations.</span></span>

</dd> <dt>

<span data-ttu-id="a4030-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="a4030-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="a4030-192">Uma descrição dos dados que são armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="a4030-192">A description of the data that is stored in the column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="a4030-193">Validação</span><span class="sxs-lookup"><span data-stu-id="a4030-193">Validation</span></span>

<dl>

[<span data-ttu-id="a4030-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="a4030-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a4030-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="a4030-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a4030-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="a4030-196">ICE32</span></span>](ice32.md)  
</dl>

## <a name="remarks"></a><span data-ttu-id="a4030-197">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4030-197">Remarks</span></span>

<span data-ttu-id="a4030-198">O campo Categoria desta tabela se aplica somente a dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a4030-198">The Category field of this table only applies to string data.</span></span> <span data-ttu-id="a4030-199">Se o campo de coluna se referir a uma coluna com dados binários, o tipo de dados Binary deverá ser especificado no campo Categoria.</span><span class="sxs-lookup"><span data-stu-id="a4030-199">If the Column field refers to a column with binary data, the binary data type must be specified in the Category field.</span></span> <span data-ttu-id="a4030-200">Os tipos de coluna de dados inteiros ignoram o campo de categoria durante a validação.</span><span class="sxs-lookup"><span data-stu-id="a4030-200">Integer data Column types ignore the Category field during validation.</span></span>

 

 



