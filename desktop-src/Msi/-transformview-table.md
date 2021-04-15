---
description: Esta é uma tabela temporária somente leitura usada para exibir transformações com o modo de exibição de transformação. Essa tabela nunca é persistida pelo instalador.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: Tabela de _TransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505804"
---
# <a name="_transformview-table"></a><span data-ttu-id="779a2-104">\_Tabela de transformview</span><span class="sxs-lookup"><span data-stu-id="779a2-104">\_TransformView Table</span></span>

<span data-ttu-id="779a2-105">Esta é uma tabela temporária somente leitura usada para exibir transformações com o modo de exibição de transformação.</span><span class="sxs-lookup"><span data-stu-id="779a2-105">This is a read-only temporary table used to view transforms with the transform view mode.</span></span> <span data-ttu-id="779a2-106">Essa tabela nunca é persistida pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="779a2-106">This table is never persisted by the installer.</span></span>

<span data-ttu-id="779a2-107">Para invocar o modo de exibição de transformação, obtenha um identificador e abra o banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="779a2-107">To invoke the transform view mode, obtain a handle and open the reference database.</span></span> <span data-ttu-id="779a2-108">Consulte [obtendo um identificador de banco de dados](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-108">See [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span> <span data-ttu-id="779a2-109">Chame [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) com o \_ erro MSITRANSFORM \_ VIEWTRANSFORM.</span><span class="sxs-lookup"><span data-stu-id="779a2-109">Call [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) with MSITRANSFORM\_ERROR\_VIEWTRANSFORM.</span></span> <span data-ttu-id="779a2-110">Isso interrompe a transformação de ser aplicada ao banco de dados e despeja o conteúdo da transformação na \_ tabela do transformview.</span><span class="sxs-lookup"><span data-stu-id="779a2-110">This stops the transform from being applied to the database and dumps the transform contents into the \_TransformView table.</span></span> <span data-ttu-id="779a2-111">Os dados na tabela podem ser acessados usando consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="779a2-111">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="779a2-112">Consulte [trabalhando com consultas](working-with-queries.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-112">See [Working with Queries](working-with-queries.md).</span></span>

<span data-ttu-id="779a2-113">A \_ tabela transformview não é limpa quando outra transformação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="779a2-113">The \_TransformView table is not cleared when another transform is applied.</span></span> <span data-ttu-id="779a2-114">A tabela reflete o efeito cumulativo de aplicativos sucessivos.</span><span class="sxs-lookup"><span data-stu-id="779a2-114">The table reflects the cumulative effect of successive applications.</span></span> <span data-ttu-id="779a2-115">Para exibir as transformações separadamente, você deve liberar a tabela.</span><span class="sxs-lookup"><span data-stu-id="779a2-115">To view the transforms separately you must release the table.</span></span>

<span data-ttu-id="779a2-116">A \_ tabela transformview tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="779a2-116">The \_TransformView Table has the following columns.</span></span>



| <span data-ttu-id="779a2-117">Coluna</span><span class="sxs-lookup"><span data-stu-id="779a2-117">Column</span></span>  | <span data-ttu-id="779a2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="779a2-118">Type</span></span>                         | <span data-ttu-id="779a2-119">Chave</span><span class="sxs-lookup"><span data-stu-id="779a2-119">Key</span></span> | <span data-ttu-id="779a2-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="779a2-120">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="779a2-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="779a2-121">Table</span></span>   | [<span data-ttu-id="779a2-122">Identificador</span><span class="sxs-lookup"><span data-stu-id="779a2-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="779a2-123">S</span><span class="sxs-lookup"><span data-stu-id="779a2-123">Y</span></span>   | <span data-ttu-id="779a2-124">N</span><span class="sxs-lookup"><span data-stu-id="779a2-124">N</span></span>        |
| <span data-ttu-id="779a2-125">Coluna</span><span class="sxs-lookup"><span data-stu-id="779a2-125">Column</span></span>  | [<span data-ttu-id="779a2-126">Text</span><span class="sxs-lookup"><span data-stu-id="779a2-126">Text</span></span>](text.md)             | <span data-ttu-id="779a2-127">S</span><span class="sxs-lookup"><span data-stu-id="779a2-127">Y</span></span>   | <span data-ttu-id="779a2-128">N</span><span class="sxs-lookup"><span data-stu-id="779a2-128">N</span></span>        |
| <span data-ttu-id="779a2-129">Linha</span><span class="sxs-lookup"><span data-stu-id="779a2-129">Row</span></span>     | [<span data-ttu-id="779a2-130">Text</span><span class="sxs-lookup"><span data-stu-id="779a2-130">Text</span></span>](text.md)             | <span data-ttu-id="779a2-131">S</span><span class="sxs-lookup"><span data-stu-id="779a2-131">Y</span></span>   | <span data-ttu-id="779a2-132">S</span><span class="sxs-lookup"><span data-stu-id="779a2-132">Y</span></span>        |
| <span data-ttu-id="779a2-133">Dados</span><span class="sxs-lookup"><span data-stu-id="779a2-133">Data</span></span>    | [<span data-ttu-id="779a2-134">Text</span><span class="sxs-lookup"><span data-stu-id="779a2-134">Text</span></span>](text.md)             | <span data-ttu-id="779a2-135">N</span><span class="sxs-lookup"><span data-stu-id="779a2-135">N</span></span>   | <span data-ttu-id="779a2-136">S</span><span class="sxs-lookup"><span data-stu-id="779a2-136">Y</span></span>        |
| <span data-ttu-id="779a2-137">Current</span><span class="sxs-lookup"><span data-stu-id="779a2-137">Current</span></span> | [<span data-ttu-id="779a2-138">Text</span><span class="sxs-lookup"><span data-stu-id="779a2-138">Text</span></span>](text.md)             | <span data-ttu-id="779a2-139">N</span><span class="sxs-lookup"><span data-stu-id="779a2-139">N</span></span>   | <span data-ttu-id="779a2-140">S</span><span class="sxs-lookup"><span data-stu-id="779a2-140">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="779a2-141">Coluna</span><span class="sxs-lookup"><span data-stu-id="779a2-141">Column</span></span>

<dl> <dt>

<span data-ttu-id="779a2-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="779a2-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="779a2-143">Nome de uma tabela de banco de dados alterada.</span><span class="sxs-lookup"><span data-stu-id="779a2-143">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="779a2-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Pilha</span><span class="sxs-lookup"><span data-stu-id="779a2-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="779a2-145">Nome de uma coluna de tabela alterada ou inserir, excluir, criar ou descartar.</span><span class="sxs-lookup"><span data-stu-id="779a2-145">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="779a2-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila</span><span class="sxs-lookup"><span data-stu-id="779a2-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="779a2-147">Uma lista dos valores de chave primária separados por tabulações.</span><span class="sxs-lookup"><span data-stu-id="779a2-147">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="779a2-148">Valores nulos de chave primária são representados por um único caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="779a2-148">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="779a2-149">Um valor nulo nesta coluna indica uma alteração de esquema.</span><span class="sxs-lookup"><span data-stu-id="779a2-149">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="779a2-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado</span><span class="sxs-lookup"><span data-stu-id="779a2-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="779a2-151">Dados, nome de um fluxo de dados ou uma definição de coluna.</span><span class="sxs-lookup"><span data-stu-id="779a2-151">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="779a2-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Atualizados</span><span class="sxs-lookup"><span data-stu-id="779a2-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="779a2-153">Valor atual do banco de dados de referência ou de um número de coluna.</span><span class="sxs-lookup"><span data-stu-id="779a2-153">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="779a2-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="779a2-154">Remarks</span></span>

<span data-ttu-id="779a2-155">O \_ transformview é mantido na memória por uma contagem de bloqueios, que pode ser lançada com o comando SQL a seguir.</span><span class="sxs-lookup"><span data-stu-id="779a2-155">The \_TransformView is held in memory by a lock count, that can be released with the following SQL command.</span></span>

<span data-ttu-id="779a2-156">"ALTER TABLE \_ Exformview Free".</span><span class="sxs-lookup"><span data-stu-id="779a2-156">"ALTER TABLE \_TransformView FREE".</span></span>

<span data-ttu-id="779a2-157">Os dados na tabela podem ser acessados usando consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="779a2-157">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="779a2-158">A linguagem SQL tem duas divisões principais: DDL (linguagem de definição de dados) que é usada para definir todos os objetos em um banco de dados SQL e DML (linguagem de manipulação de dados) usada para selecionar, inserir, atualizar e excluir dados nos objetos definidos usando DDL.</span><span class="sxs-lookup"><span data-stu-id="779a2-158">The SQL language has two main divisions: Data Definition Language (DDL) that is used to define all the objects in an SQL database, and Data Manipulation Language (DML) that is used to select, insert, update, and delete data in the objects defined using DDL.</span></span>

<span data-ttu-id="779a2-159">As operações de transformação DML (linguagem de manipulação de dados) são indicadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="779a2-159">The Data Manipulation Language (DML) transform operations are indicated as follows.</span></span> <span data-ttu-id="779a2-160">DML (linguagem de manipulação de dados) são as instruções no SQL que manipulam, em vez de definir, os dados.</span><span class="sxs-lookup"><span data-stu-id="779a2-160">Data Manipulation Language (DML) are those statements in SQL that manipulate, as opposed to define, data.</span></span>



| <span data-ttu-id="779a2-161">Operação de transformação</span><span class="sxs-lookup"><span data-stu-id="779a2-161">Transform operation</span></span> | <span data-ttu-id="779a2-162">Resultado do SQL</span><span class="sxs-lookup"><span data-stu-id="779a2-162">SQL result</span></span>                                    |
|---------------------|-----------------------------------------------|
| <span data-ttu-id="779a2-163">Modificar dados</span><span class="sxs-lookup"><span data-stu-id="779a2-163">Modify data</span></span>         | <span data-ttu-id="779a2-164">tabela pilha fila dado {valor atual}</span><span class="sxs-lookup"><span data-stu-id="779a2-164">{table} {column} {row} {data} {current value}</span></span> |
| <span data-ttu-id="779a2-165">Inserir linha</span><span class="sxs-lookup"><span data-stu-id="779a2-165">Insert row</span></span>          | <span data-ttu-id="779a2-166">tabela "Inserir" {Row} nulo NULL</span><span class="sxs-lookup"><span data-stu-id="779a2-166">{table} "INSERT" {row} NULL NULL</span></span>              |
| <span data-ttu-id="779a2-167">Excluir linha</span><span class="sxs-lookup"><span data-stu-id="779a2-167">Delete row</span></span>          | <span data-ttu-id="779a2-168">tabela "Excluir" {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="779a2-168">{table} "DELETE" {row} NULL NULL</span></span>              |



 

<span data-ttu-id="779a2-169">As operações de transformação DDL (linguagem de definição de dados) são indicadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="779a2-169">The Data Definition Language (DDL) transform operations are indicated as follows.</span></span> <span data-ttu-id="779a2-170">O DDL (linguagem de definição de dados) são as instruções no SQL que definem, em vez de manipular, os dados.</span><span class="sxs-lookup"><span data-stu-id="779a2-170">Data Definition Language (DDL) are those statements in SQL that define, as opposed to manipulate, data.</span></span>



| <span data-ttu-id="779a2-171">Operação de transformação</span><span class="sxs-lookup"><span data-stu-id="779a2-171">Transform operation</span></span> | <span data-ttu-id="779a2-172">Resultado do SQL</span><span class="sxs-lookup"><span data-stu-id="779a2-172">SQL result</span></span>                                   |
|---------------------|----------------------------------------------|
| <span data-ttu-id="779a2-173">Adicionar coluna</span><span class="sxs-lookup"><span data-stu-id="779a2-173">Add column</span></span>          | <span data-ttu-id="779a2-174">tabela pilha NULL {defn} {número da coluna}</span><span class="sxs-lookup"><span data-stu-id="779a2-174">{table} {column} NULL {defn} {column number}</span></span> |
| <span data-ttu-id="779a2-175">Adicionar tabela</span><span class="sxs-lookup"><span data-stu-id="779a2-175">Add table</span></span>           | <span data-ttu-id="779a2-176">tabela "CREATE" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="779a2-176">{table} "CREATE" NULL NULL NULL</span></span>              |
| <span data-ttu-id="779a2-177">Remover tabela</span><span class="sxs-lookup"><span data-stu-id="779a2-177">Drop table</span></span>          | <span data-ttu-id="779a2-178">tabela "REMOVER" NULL NULL NULO</span><span class="sxs-lookup"><span data-stu-id="779a2-178">{table} "DROP" NULL NULL NULL</span></span>                |



 

<span data-ttu-id="779a2-179">Quando o aplicativo de uma transformação adiciona essa tabela, o campo de dados recebe texto que pode ser interpretado como um valor inteiro de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="779a2-179">When the application of a transform adds this table, the Data field receives text that can be interpreted as a 16-bit integer value.</span></span> <span data-ttu-id="779a2-180">O valor descreve a coluna denominada no campo coluna.</span><span class="sxs-lookup"><span data-stu-id="779a2-180">The value describes the column named in the Column field.</span></span> <span data-ttu-id="779a2-181">Você pode comparar o valor inteiro com as constantes na tabela a seguir para determinar a definição da coluna alterada.</span><span class="sxs-lookup"><span data-stu-id="779a2-181">You can compare the integer value to the constants in the following table to determine the definition of the altered column.</span></span>



| <span data-ttu-id="779a2-182">bit</span><span class="sxs-lookup"><span data-stu-id="779a2-182">Bit</span></span>                                                                                                       | <span data-ttu-id="779a2-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="779a2-183">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a2-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span><span class="sxs-lookup"><span data-stu-id="779a2-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span></span><br/>         | <span data-ttu-id="779a2-185">Hexadecimal: 0x0000 0x0100</span><span class="sxs-lookup"><span data-stu-id="779a2-185">Hexadecimal: 0x0000 0x0100</span></span><br/> <span data-ttu-id="779a2-186">Decimal: 0 255</span><span class="sxs-lookup"><span data-stu-id="779a2-186">Decimal: 0 255</span></span><br/> <span data-ttu-id="779a2-187">Largura da Coluna</span><span class="sxs-lookup"><span data-stu-id="779a2-187">Column width</span></span><br/>                                                                                                                                                                                                                                  |
| <span data-ttu-id="779a2-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span><span class="sxs-lookup"><span data-stu-id="779a2-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span></span><br/>                  | <span data-ttu-id="779a2-189">Hexadecimal: 0x0100</span><span class="sxs-lookup"><span data-stu-id="779a2-189">Hexadecimal: 0x0100</span></span><br/> <span data-ttu-id="779a2-190">Decimal: 256</span><span class="sxs-lookup"><span data-stu-id="779a2-190">Decimal: 256</span></span><br/> <span data-ttu-id="779a2-191">Uma coluna persistente.</span><span class="sxs-lookup"><span data-stu-id="779a2-191">A persistent column.</span></span> <span data-ttu-id="779a2-192">Zero significa uma coluna temporária.</span><span class="sxs-lookup"><span data-stu-id="779a2-192">Zero means a temporary column.</span></span> <br/>                                                                                                                                                                                                   |
| <span data-ttu-id="779a2-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span><span class="sxs-lookup"><span data-stu-id="779a2-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span></span><br/>                  | <span data-ttu-id="779a2-194">Hexadecimal: 0x0200</span><span class="sxs-lookup"><span data-stu-id="779a2-194">Hexadecimal: 0x0200</span></span><br/> <span data-ttu-id="779a2-195">Decimal: 1023</span><span class="sxs-lookup"><span data-stu-id="779a2-195">Decimal: 1023</span></span><br/> <span data-ttu-id="779a2-196">Uma coluna localizável.</span><span class="sxs-lookup"><span data-stu-id="779a2-196">A localizable column.</span></span> <span data-ttu-id="779a2-197">Zero significa que a coluna não pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="779a2-197">Zero means the column cannot be localized.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="779a2-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span><span class="sxs-lookup"><span data-stu-id="779a2-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span></span><br/> | <span data-ttu-id="779a2-199">Hexadecimal: 0x0000</span><span class="sxs-lookup"><span data-stu-id="779a2-199">Hexadecimal: 0x0000</span></span><br/> <span data-ttu-id="779a2-200">Decimal: 0</span><span class="sxs-lookup"><span data-stu-id="779a2-200">Decimal: 0</span></span><br/> <span data-ttu-id="779a2-201">Long integer</span><span class="sxs-lookup"><span data-stu-id="779a2-201">Long integer</span></span><br/> <span data-ttu-id="779a2-202">Hexadecimal: 0x0400</span><span class="sxs-lookup"><span data-stu-id="779a2-202">Hexadecimal: 0x0400</span></span><br/> <span data-ttu-id="779a2-203">Decimal: 1024</span><span class="sxs-lookup"><span data-stu-id="779a2-203">Decimal: 1024</span></span><br/> <span data-ttu-id="779a2-204">Inteiro curto</span><span class="sxs-lookup"><span data-stu-id="779a2-204">Short integer</span></span><br/> <span data-ttu-id="779a2-205">Hexadecimal: 0x0800</span><span class="sxs-lookup"><span data-stu-id="779a2-205">Hexadecimal: 0x0800</span></span><br/> <span data-ttu-id="779a2-206">Decimal: 2048</span><span class="sxs-lookup"><span data-stu-id="779a2-206">Decimal: 2048</span></span><br/> <span data-ttu-id="779a2-207">Objeto Binary</span><span class="sxs-lookup"><span data-stu-id="779a2-207">Binary object</span></span><br/> <span data-ttu-id="779a2-208">Hexadecimal: 0x0C00</span><span class="sxs-lookup"><span data-stu-id="779a2-208">Hexadecimal: 0x0C00</span></span><br/> <span data-ttu-id="779a2-209">Decimal: 3072</span><span class="sxs-lookup"><span data-stu-id="779a2-209">Decimal: 3072</span></span><br/> <span data-ttu-id="779a2-210">String</span><span class="sxs-lookup"><span data-stu-id="779a2-210">String</span></span><br/> |
| <span data-ttu-id="779a2-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span><span class="sxs-lookup"><span data-stu-id="779a2-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span></span><br/>              | <span data-ttu-id="779a2-212">Hexadecimal: 0x1000</span><span class="sxs-lookup"><span data-stu-id="779a2-212">Hexadecimal: 0x1000</span></span><br/> <span data-ttu-id="779a2-213">Decimal: 4096</span><span class="sxs-lookup"><span data-stu-id="779a2-213">Decimal: 4096</span></span><br/> <span data-ttu-id="779a2-214">Coluna anulável.</span><span class="sxs-lookup"><span data-stu-id="779a2-214">Nullable column.</span></span> <span data-ttu-id="779a2-215">Zero significa que a coluna não permite valor nulo.</span><span class="sxs-lookup"><span data-stu-id="779a2-215">Zero means the column is non-nullable.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="779a2-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span><span class="sxs-lookup"><span data-stu-id="779a2-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span></span><br/>              | <span data-ttu-id="779a2-217">Hexadecimal: 0x2000</span><span class="sxs-lookup"><span data-stu-id="779a2-217">Hexadecimal: 0x2000</span></span><br/> <span data-ttu-id="779a2-218">Decimal: 8192</span><span class="sxs-lookup"><span data-stu-id="779a2-218">Decimal: 8192</span></span><br/> <span data-ttu-id="779a2-219">Coluna de chave primária.</span><span class="sxs-lookup"><span data-stu-id="779a2-219">Primary key column.</span></span> <span data-ttu-id="779a2-220">Zero significa que esta coluna não é uma chave primária.</span><span class="sxs-lookup"><span data-stu-id="779a2-220">Zero means this column is not a primary key.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="779a2-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span><span class="sxs-lookup"><span data-stu-id="779a2-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span></span><br/> | <span data-ttu-id="779a2-222">Hexadecimal: 0x4000 0x8000</span><span class="sxs-lookup"><span data-stu-id="779a2-222">Hexadecimal: 0x4000 0x8000</span></span><br/> <span data-ttu-id="779a2-223">Decimal: 16384 32768</span><span class="sxs-lookup"><span data-stu-id="779a2-223">Decimal: 16384 32768</span></span><br/> <span data-ttu-id="779a2-224">Reservado</span><span class="sxs-lookup"><span data-stu-id="779a2-224">Reserved</span></span><br/>                                                                                                                                                                                                                                |



 

<span data-ttu-id="779a2-225">Para obter um exemplo de script que demonstre a \_ tabela transformview, consulte [exibir uma transformação](view-a-transform.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-225">For a script sample that demonstrates the \_TransformView table, see [View a Transform](view-a-transform.md).</span></span>

 

 




