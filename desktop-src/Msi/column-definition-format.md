---
description: MsiViewGetColumnInfo e a Propriedade ColumnInfo do objeto View usam o formato a seguir para descrever as definições de coluna do banco de dados.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato de definição de coluna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169869"
---
# <a name="column-definition-format"></a><span data-ttu-id="f93ec-103">Formato de definição de coluna</span><span class="sxs-lookup"><span data-stu-id="f93ec-103">Column Definition Format</span></span>

<span data-ttu-id="f93ec-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) e a [**Propriedade ColumnInfo**](view-columninfo.md) do objeto [**View**](view-object.md) usam o formato a seguir para descrever as definições de coluna do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f93ec-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) and the [**ColumnInfo Property**](view-columninfo.md) of the [**View**](view-object.md) object use the following format to describe database column definitions.</span></span> <span data-ttu-id="f93ec-105">Cada coluna é descrita por uma cadeia de caracteres no campo de registro correspondente retornado pela função ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="f93ec-105">Each column is described by a string in the corresponding record field returned by the function or property.</span></span> <span data-ttu-id="f93ec-106">A cadeia de caracteres de definição consiste em uma única letra que representa o tipo de dados seguido pela largura da coluna (em caracteres quando aplicável; caso contrário, bytes).</span><span class="sxs-lookup"><span data-stu-id="f93ec-106">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise).</span></span> <span data-ttu-id="f93ec-107">Uma largura de zero designa uma largura não associada (por exemplo, campos de texto longo e fluxos).</span><span class="sxs-lookup"><span data-stu-id="f93ec-107">A width of zero designates an unbounded width (for example, long text fields and streams).</span></span> <span data-ttu-id="f93ec-108">Uma letra maiúscula indica que valores nulos são permitidos na coluna.</span><span class="sxs-lookup"><span data-stu-id="f93ec-108">An uppercase letter indicates that null values are allowed in the column.</span></span>



| <span data-ttu-id="f93ec-109">Descritor de coluna</span><span class="sxs-lookup"><span data-stu-id="f93ec-109">Column descriptor</span></span> | <span data-ttu-id="f93ec-110">Cadeia de caracteres de definição</span><span class="sxs-lookup"><span data-stu-id="f93ec-110">Definition string</span></span>                 |
|-------------------|-----------------------------------|
| <span data-ttu-id="f93ec-111">&?</span><span class="sxs-lookup"><span data-stu-id="f93ec-111">s?</span></span>                | <span data-ttu-id="f93ec-112">Cadeia de caracteres, comprimento variável (? = 1-255)</span><span class="sxs-lookup"><span data-stu-id="f93ec-112">String, variable length (?=1-255)</span></span> |
| <span data-ttu-id="f93ec-113">S0</span><span class="sxs-lookup"><span data-stu-id="f93ec-113">s0</span></span>                | <span data-ttu-id="f93ec-114">Cadeia de caracteres, comprimento variável</span><span class="sxs-lookup"><span data-stu-id="f93ec-114">String, variable length</span></span>           |
| <span data-ttu-id="f93ec-115">i2</span><span class="sxs-lookup"><span data-stu-id="f93ec-115">i2</span></span>                | <span data-ttu-id="f93ec-116">Inteiro curto</span><span class="sxs-lookup"><span data-stu-id="f93ec-116">Short integer</span></span>                     |
| <span data-ttu-id="f93ec-117">i4</span><span class="sxs-lookup"><span data-stu-id="f93ec-117">i4</span></span>                | <span data-ttu-id="f93ec-118">Long integer</span><span class="sxs-lookup"><span data-stu-id="f93ec-118">Long integer</span></span>                      |
| <span data-ttu-id="f93ec-119">V0</span><span class="sxs-lookup"><span data-stu-id="f93ec-119">v0</span></span>                | <span data-ttu-id="f93ec-120">Fluxo binário</span><span class="sxs-lookup"><span data-stu-id="f93ec-120">Binary Stream</span></span>                     |
| <span data-ttu-id="f93ec-121">m?</span><span class="sxs-lookup"><span data-stu-id="f93ec-121">g?</span></span>                | <span data-ttu-id="f93ec-122">Cadeia de caracteres temporária (? = 0-255)</span><span class="sxs-lookup"><span data-stu-id="f93ec-122">Temporary string (?=0-255)</span></span>        |
| <span data-ttu-id="f93ec-123">j?</span><span class="sxs-lookup"><span data-stu-id="f93ec-123">j?</span></span>                | <span data-ttu-id="f93ec-124">Inteiro temporário (? = 0, 1, 2, 4)</span><span class="sxs-lookup"><span data-stu-id="f93ec-124">Temporary integer (?=0,1,2,4)</span></span>     |
| <span data-ttu-id="f93ec-125">O0</span><span class="sxs-lookup"><span data-stu-id="f93ec-125">O0</span></span>                | <span data-ttu-id="f93ec-126">Objeto temporário</span><span class="sxs-lookup"><span data-stu-id="f93ec-126">Temporary object</span></span>                  |



 

<span data-ttu-id="f93ec-127">As cadeias de caracteres usadas para descrever as colunas têm a seguinte relação com as cadeias de caracteres de consulta SQL usadas por CREATE e ALTER.</span><span class="sxs-lookup"><span data-stu-id="f93ec-127">The strings used to describe columns have the following relationship to the SQL query strings used by CREATE and ALTER.</span></span> <span data-ttu-id="f93ec-128">Para obter mais informações, consulte [sintaxe SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f93ec-128">For more information, see [SQL Syntax](sql-syntax.md).</span></span>



| <span data-ttu-id="f93ec-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f93ec-129">Returned value</span></span> | <span data-ttu-id="f93ec-130">Sintaxe SQL</span><span class="sxs-lookup"><span data-stu-id="f93ec-130">SQL syntax</span></span>                |
|----------------|---------------------------|
| <span data-ttu-id="f93ec-131">S0</span><span class="sxs-lookup"><span data-stu-id="f93ec-131">s0</span></span>             | <span data-ttu-id="f93ec-132">LONGCHAR</span><span class="sxs-lookup"><span data-stu-id="f93ec-132">LONGCHAR</span></span>                  |
| <span data-ttu-id="f93ec-133">L0</span><span class="sxs-lookup"><span data-stu-id="f93ec-133">l0</span></span>             | <span data-ttu-id="f93ec-134">LONGCHAR LOCALIZÁVEL</span><span class="sxs-lookup"><span data-stu-id="f93ec-134">LONGCHAR LOCALIZABLE</span></span>      |
| <span data-ttu-id="f93ec-135">& \#</span><span class="sxs-lookup"><span data-stu-id="f93ec-135">s \#</span></span>           | <span data-ttu-id="f93ec-136">CHAR ( \# )</span><span class="sxs-lookup"><span data-stu-id="f93ec-136">CHAR(\#)</span></span>                  |
| <span data-ttu-id="f93ec-137">& \#</span><span class="sxs-lookup"><span data-stu-id="f93ec-137">s \#</span></span>           | <span data-ttu-id="f93ec-138">CARACTERE ( \# )</span><span class="sxs-lookup"><span data-stu-id="f93ec-138">CHARACTER(\#)</span></span>             |
| <span data-ttu-id="f93ec-139">debug \#</span><span class="sxs-lookup"><span data-stu-id="f93ec-139">l \#</span></span>           | <span data-ttu-id="f93ec-140">CHAR ( \# ) localizável</span><span class="sxs-lookup"><span data-stu-id="f93ec-140">CHAR(\#) LOCALIZABLE</span></span>      |
| <span data-ttu-id="f93ec-141">debug \#</span><span class="sxs-lookup"><span data-stu-id="f93ec-141">l \#</span></span>           | <span data-ttu-id="f93ec-142">CARACTERE ( \# ) localizável</span><span class="sxs-lookup"><span data-stu-id="f93ec-142">CHARACTER(\#) LOCALIZABLE</span></span> |
| <span data-ttu-id="f93ec-143">i2</span><span class="sxs-lookup"><span data-stu-id="f93ec-143">i2</span></span>             | <span data-ttu-id="f93ec-144">BAIXO</span><span class="sxs-lookup"><span data-stu-id="f93ec-144">SHORT</span></span>                     |
| <span data-ttu-id="f93ec-145">i2</span><span class="sxs-lookup"><span data-stu-id="f93ec-145">i2</span></span>             | <span data-ttu-id="f93ec-146">INT</span><span class="sxs-lookup"><span data-stu-id="f93ec-146">INT</span></span>                       |
| <span data-ttu-id="f93ec-147">i2</span><span class="sxs-lookup"><span data-stu-id="f93ec-147">i2</span></span>             | <span data-ttu-id="f93ec-148">INTEGER</span><span class="sxs-lookup"><span data-stu-id="f93ec-148">INTEGER</span></span>                   |
| <span data-ttu-id="f93ec-149">i4</span><span class="sxs-lookup"><span data-stu-id="f93ec-149">i4</span></span>             | <span data-ttu-id="f93ec-150">LONG</span><span class="sxs-lookup"><span data-stu-id="f93ec-150">LONG</span></span>                      |
| <span data-ttu-id="f93ec-151">V0</span><span class="sxs-lookup"><span data-stu-id="f93ec-151">v0</span></span>             | <span data-ttu-id="f93ec-152">OBJECT</span><span class="sxs-lookup"><span data-stu-id="f93ec-152">OBJECT</span></span>                    |



 

<span data-ttu-id="f93ec-153">Se a letra não estiver em letras maiúsculas, a instrução SQL deverá ser anexada com NOT NULL.</span><span class="sxs-lookup"><span data-stu-id="f93ec-153">If the letter is not capitalized, the SQL statement should be appended with NOT NULL.</span></span>



| <span data-ttu-id="f93ec-154">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f93ec-154">Returned value</span></span> | <span data-ttu-id="f93ec-155">Sintaxe SQL</span><span class="sxs-lookup"><span data-stu-id="f93ec-155">SQL syntax</span></span>        |
|----------------|-------------------|
| <span data-ttu-id="f93ec-156">S0</span><span class="sxs-lookup"><span data-stu-id="f93ec-156">s0</span></span>             | <span data-ttu-id="f93ec-157">LONGCHAR NÃO NULO</span><span class="sxs-lookup"><span data-stu-id="f93ec-157">LONGCHAR NOT NULL</span></span> |



 

<span data-ttu-id="f93ec-158">O instalador não limita internamente o comprimento de colunas para o valor especificado pelo formato de definição de coluna.</span><span class="sxs-lookup"><span data-stu-id="f93ec-158">The installer does not internally limit the length of columns to the value specified by the column definition format.</span></span> <span data-ttu-id="f93ec-159">Se os dados inseridos em um campo excederem o comprimento de coluna especificado, o pacote não passará na [validação do pacote](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="f93ec-159">If the data entered into a field exceeds the specified column length, the package fails to pass [package validation](package-validation.md).</span></span> <span data-ttu-id="f93ec-160">Para passar a validação nesse caso, os dados ou o esquema de banco de dados devem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="f93ec-160">To pass validation in this case, either the data or the database schema must be changed.</span></span> <span data-ttu-id="f93ec-161">O único meio de alterar o tamanho da coluna de uma tabela padrão é exportando a tabela usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editando o arquivo. IDT exportado e, em seguida, importando a tabela usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="f93ec-161">The only means to change the column length of a standard table is by exporting the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editing the exported .idt file, and then importing the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="f93ec-162">Os autores não podem alterar os tipos de dados de coluna, a nulidade ou os atributos de localização de colunas em tabelas padrão.</span><span class="sxs-lookup"><span data-stu-id="f93ec-162">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="f93ec-163">Os autores podem criar tabelas personalizadas com colunas com qualquer atributo de coluna.</span><span class="sxs-lookup"><span data-stu-id="f93ec-163">Authors can create custom tables with columns having any column attributes.</span></span>

<span data-ttu-id="f93ec-164">Ao usar o [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para mesclar um banco de dados de referência em um banco de dados de destino, os nomes de coluna, o número de chaves primárias e os tipos de dado de coluna devem corresponder.</span><span class="sxs-lookup"><span data-stu-id="f93ec-164">When using [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to merge a reference database into a target database, the column names, number of primary keys, and column data types must match.</span></span> <span data-ttu-id="f93ec-165">**MsiDatabaseMerge** ignora os atributos de comprimento de coluna e localização.</span><span class="sxs-lookup"><span data-stu-id="f93ec-165">**MsiDatabaseMerge** ignores the localization and column length attributes.</span></span> <span data-ttu-id="f93ec-166">Se uma coluna no banco de dados de referência tiver um comprimento que seja 0 ou maior do que o comprimento da coluna no banco de dados de destino, **MsiDatabaseMerge** aumentará o tamanho da coluna no banco de dados de destino para o comprimento no banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="f93ec-166">If a column in the reference database has a length that is 0 or greater than the that column's length in the target database, **MsiDatabaseMerge** increases the column length in the target database to the length in the reference database.</span></span>

<span data-ttu-id="f93ec-167">Ao usar Mergmod.dll versão 2,0, o aplicativo de um módulo de mesclagem para um arquivo. msi nunca altera o comprimento das colunas ou os tipos de coluna de uma tabela de banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="f93ec-167">When using Mergmod.dll version 2.0, the application of a merge module to a .msi file never changes the length of columns or the column types of an existing database table.</span></span> <span data-ttu-id="f93ec-168">O aplicativo de um módulo de mesclagem pode, no entanto, alterar o esquema de uma tabela de banco de dados existente se o módulo adicionar novas colunas a uma tabela para a qual ela é válida para adicionar colunas.</span><span class="sxs-lookup"><span data-stu-id="f93ec-168">The application of a merge module can however change the schema of an existing database table if the module adds new columns to a table for which it is valid to add columns.</span></span> <span data-ttu-id="f93ec-169">Ao usar uma versão Mergemod.dll inferior à versão 2,0, o aplicativo de um módulo de mesclagem nunca altera o comprimento das colunas e nunca altera o esquema do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="f93ec-169">When using a Mergemod.dll version less than version 2.0, the application of a merge module never changes the length of columns and never changes the schema of the target database.</span></span>

 

 



