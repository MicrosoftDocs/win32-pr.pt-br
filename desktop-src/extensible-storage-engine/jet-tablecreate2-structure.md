---
description: 'Saiba mais sobre: estrutura de JET_TABLECREATE2'
title: Estrutura JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837448"
---
# <a name="jet_tablecreate2-structure"></a><span data-ttu-id="97e24-103">Estrutura JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="97e24-103">JET_TABLECREATE2 Structure</span></span>


<span data-ttu-id="97e24-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="97e24-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate2-structure"></a><span data-ttu-id="97e24-105">Estrutura JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="97e24-105">JET_TABLECREATE2 Structure</span></span>

<span data-ttu-id="97e24-106">A estrutura de **JET_TABLECREATE2** contém as informações necessárias para criar uma tabela populada com colunas e índices em um banco de dados ESE e que designa uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="97e24-106">The **JET_TABLECREATE2** structure contains the information that is needed to create a table populated with columns and indexes in an ESE database, and that designates a callback function.</span></span> <span data-ttu-id="97e24-107">A estrutura de **JET_TABLECREATE2** é usada pelo [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="97e24-107">The **JET_TABLECREATE2** structure is used by [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span>

<span data-ttu-id="97e24-108">**Windows XP:** A estrutura de **JET_TABLECREATE2** é introduzida no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97e24-108">**Windows XP:** The **JET_TABLECREATE2** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a><span data-ttu-id="97e24-109">Membros</span><span class="sxs-lookup"><span data-stu-id="97e24-109">Members</span></span>

<span data-ttu-id="97e24-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="97e24-110">**cbStruct**</span></span>

<span data-ttu-id="97e24-111">O tamanho dessa estrutura em bytes (para expansão futura).</span><span class="sxs-lookup"><span data-stu-id="97e24-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="97e24-112">Ele deve ser definido como sizeof (JET_TABLECREATE2) em bytes.</span><span class="sxs-lookup"><span data-stu-id="97e24-112">It must be set to sizeof( JET_TABLECREATE2 ) in bytes.</span></span>

<span data-ttu-id="97e24-113">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="97e24-113">**szTableName**</span></span>

<span data-ttu-id="97e24-114">O nome da tabela a ser criada.</span><span class="sxs-lookup"><span data-stu-id="97e24-114">The name of table to create.</span></span>

<span data-ttu-id="97e24-115">O nome deve usar atender às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="97e24-115">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="97e24-116">Ter um valor menor que JET_cbNameMost, não incluindo o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="97e24-116">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="97e24-117">Consiste no seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ), ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="97e24-117">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="97e24-118">Não comece com um espaço.</span><span class="sxs-lookup"><span data-stu-id="97e24-118">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="97e24-119">Consistir em pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="97e24-119">Consist of at least one non-space character.</span></span>

<span data-ttu-id="97e24-120">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="97e24-120">**szTemplateTableName**</span></span>

<span data-ttu-id="97e24-121">O nome de uma tabela já existente da qual herdar DDL base (linguagem de definição de dados).</span><span class="sxs-lookup"><span data-stu-id="97e24-121">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="97e24-122">O uso de uma tabela de modelo permite a fácil criação de muitas tabelas com colunas e índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="97e24-122">Using a template table allows easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="97e24-123">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="97e24-123">**ulPages**</span></span>

<span data-ttu-id="97e24-124">O número inicial de páginas de banco de dados a serem alocadas para a tabela.</span><span class="sxs-lookup"><span data-stu-id="97e24-124">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="97e24-125">A especificação de um número maior que um pode reduzir a fragmentação se várias linhas forem inseridas nessa tabela.</span><span class="sxs-lookup"><span data-stu-id="97e24-125">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="97e24-126">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="97e24-126">**ulDensity**</span></span>

<span data-ttu-id="97e24-127">A densidade da tabela, em pontos percentuais.</span><span class="sxs-lookup"><span data-stu-id="97e24-127">The table density, in percentage points.</span></span> <span data-ttu-id="97e24-128">O número deve ser 0 ou estar no intervalo de 20 a 100.</span><span class="sxs-lookup"><span data-stu-id="97e24-128">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="97e24-129">Passar 0 significa que o valor padrão deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="97e24-129">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="97e24-130">O padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="97e24-130">The default is 80.</span></span>

<span data-ttu-id="97e24-131">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="97e24-131">**rgcolumncreate**</span></span>

<span data-ttu-id="97e24-132">Uma matriz de estruturas [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada uma correspondendo a uma coluna a ser criada na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="97e24-132">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="97e24-133">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="97e24-133">**cColumns**</span></span>

<span data-ttu-id="97e24-134">o número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) em **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="97e24-134">the number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="97e24-135">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="97e24-135">**rgindexcreate**</span></span>

<span data-ttu-id="97e24-136">Uma matriz de estruturas [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada uma delas corresponde a um índice a ser criado na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="97e24-136">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="97e24-137">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="97e24-137">**cIndexes**</span></span>

<span data-ttu-id="97e24-138">O número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) em **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="97e24-138">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="97e24-139">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="97e24-139">**szCallback**</span></span>

<span data-ttu-id="97e24-140">A função que é chamada durante determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="97e24-140">The function that gets called during certain events.</span></span> <span data-ttu-id="97e24-141">**cbtyp** determina quando a função de retorno de chamada será chamada.</span><span class="sxs-lookup"><span data-stu-id="97e24-141">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="97e24-142">O formato de **szCallback** deve ser "função do módulo \! " — por exemplo, "Alpha \! beta" refere-se à função beta no módulo chamado "Alpha".</span><span class="sxs-lookup"><span data-stu-id="97e24-142">The format of **szCallback** must be "module\!function"—for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span> <span data-ttu-id="97e24-143">O protótipo da função deve corresponder a [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="97e24-143">The prototype of the function must match [JET_CALLBACK](./jet-callback-callback-function.md).</span></span> <span data-ttu-id="97e24-144">Para obter mais informações, consulte [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="97e24-144">For more information, see [JET_CALLBACK](./jet-callback-callback-function.md).</span></span>

<span data-ttu-id="97e24-145">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="97e24-145">**cbtyp**</span></span>

<span data-ttu-id="97e24-146">Descreve o tipo de função de retorno de chamada designado por **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="97e24-146">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="97e24-147">Para obter mais informações, consulte [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="97e24-147">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span> <span data-ttu-id="97e24-148">Este campo de bits é composto de um ou mais dos seguintes itens.</span><span class="sxs-lookup"><span data-stu-id="97e24-148">This bitfield is composed of one or more of the following bits.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97e24-149">Valor</span><span class="sxs-lookup"><span data-stu-id="97e24-149">Value</span></span></p></th>
<th><p><span data-ttu-id="97e24-150">Significado</span><span class="sxs-lookup"><span data-stu-id="97e24-150">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97e24-151">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="97e24-151">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="97e24-152">A função de retorno de chamada será chamada quando uma coluna que pode ser finalizada tiver passado para zero.</span><span class="sxs-lookup"><span data-stu-id="97e24-152">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-153">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="97e24-153">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="97e24-154">A função de retorno de chamada será chamada antes da inserção do registro.</span><span class="sxs-lookup"><span data-stu-id="97e24-154">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e24-155">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="97e24-155">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="97e24-156">A função de retorno de chamada será chamada depois que o mecanismo de banco de dados terminar de inserir um registro.</span><span class="sxs-lookup"><span data-stu-id="97e24-156">The callback function will be called once the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-157">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="97e24-157">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="97e24-158">A função de retorno de chamada será chamada antes da modificação de um registro.</span><span class="sxs-lookup"><span data-stu-id="97e24-158">The callback function will be called prior to modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e24-159">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="97e24-159">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="97e24-160">A função de retorno de chamada será chamada depois de concluir a modificação de um registro.</span><span class="sxs-lookup"><span data-stu-id="97e24-160">The callback function will be called after finishing modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-161">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="97e24-161">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="97e24-162">A função de retorno de chamada será chamada antes da exclusão de um registro.</span><span class="sxs-lookup"><span data-stu-id="97e24-162">The callback function will be called prior to deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e24-163">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="97e24-163">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="97e24-164">A função de retorno de chamada será chamada depois que um registro tiver sido excluído.</span><span class="sxs-lookup"><span data-stu-id="97e24-164">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-165">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="97e24-165">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="97e24-166">A função de retorno de chamada será chamada para calcular um padrão definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="97e24-166">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e24-167">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="97e24-167">JET_cbtypOnlineDefragCompleted</span></span></p></td>
<td><p><span data-ttu-id="97e24-168">A função de retorno de chamada será chamada depois que uma chamada para <a href="gg294095(v=exchg.10).md">JetDefragment2</a> for concluída.</span><span class="sxs-lookup"><span data-stu-id="97e24-168">The callback function will be called after a call to <a href="gg294095(v=exchg.10).md">JetDefragment2</a> has completed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-169">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="97e24-169">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="97e24-170">A função de retorno de chamada será chamada quando o armazenamento local associado a um cursor precisar ser liberado.</span><span class="sxs-lookup"><span data-stu-id="97e24-170">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e24-171">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="97e24-171">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="97e24-172">A função de retorno de chamada será chamada quando o armazenamento local associado a uma tabela precisar ser liberado.</span><span class="sxs-lookup"><span data-stu-id="97e24-172">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97e24-173">**grbit**</span><span class="sxs-lookup"><span data-stu-id="97e24-173">**grbit**</span></span>

<span data-ttu-id="97e24-174">Um grupo de bits que contém as opções para essa chamada, que incluem zero ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="97e24-174">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97e24-175">Valor</span><span class="sxs-lookup"><span data-stu-id="97e24-175">Value</span></span></p></th>
<th><p><span data-ttu-id="97e24-176">Significado</span><span class="sxs-lookup"><span data-stu-id="97e24-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97e24-177">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="97e24-177">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="97e24-178">A configuração JET_bitTableCreateFixedDDL impede operações DDL na tabela (como adicionar ou remover colunas).</span><span class="sxs-lookup"><span data-stu-id="97e24-178">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-179">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="97e24-179">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="97e24-180">A configuração JET_bitTableCreateTemplateTable faz com que a tabela seja uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="97e24-180">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="97e24-181">As novas tabelas podem especificar o nome dessa tabela como sua tabela de modelos.</span><span class="sxs-lookup"><span data-stu-id="97e24-181">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="97e24-182">A configuração JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="97e24-182">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e24-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="97e24-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="97e24-184">Deve ser usado em conjunto com JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="97e24-184">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="97e24-185">Preterido.</span><span class="sxs-lookup"><span data-stu-id="97e24-185">Deprecated.</span></span> <span data-ttu-id="97e24-186">Não use.</span><span class="sxs-lookup"><span data-stu-id="97e24-186">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97e24-187">**TableID**</span><span class="sxs-lookup"><span data-stu-id="97e24-187">**tableid**</span></span>

<span data-ttu-id="97e24-188">Um campo de saída que mantém o [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="97e24-188">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="97e24-189">Se a chamada à API falhar, o valor será indefinido.</span><span class="sxs-lookup"><span data-stu-id="97e24-189">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="97e24-190">**cCreated**</span><span class="sxs-lookup"><span data-stu-id="97e24-190">**cCreated**</span></span>

<span data-ttu-id="97e24-191">Um campo de saída que contém a contagem de objetos que são criados se a chamada à API for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="97e24-191">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="97e24-192">Se a chamada à API falhar, o valor será indefinido.</span><span class="sxs-lookup"><span data-stu-id="97e24-192">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="97e24-193">A contagem de objetos que é criada é igual à soma de colunas, tabelas e índices criados com êxito.</span><span class="sxs-lookup"><span data-stu-id="97e24-193">The count of objects that is created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="97e24-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97e24-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97e24-195"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="97e24-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="97e24-196">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97e24-196">Requires Windows  Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-197"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="97e24-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="97e24-198">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="97e24-198">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e24-199"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="97e24-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="97e24-200">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="97e24-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e24-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="97e24-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="97e24-202">Implementado como <strong>JET_TABLECREATE2_W</strong> (Unicode) e <strong>JET_TABLECREATE2_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="97e24-202">Implemented as <strong>JET_TABLECREATE2_W</strong> (Unicode) and <strong>JET_TABLECREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="97e24-203">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="97e24-203">See Also</span></span>

[<span data-ttu-id="97e24-204">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="97e24-204">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="97e24-205">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="97e24-205">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="97e24-206">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="97e24-206">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="97e24-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="97e24-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="97e24-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="97e24-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="97e24-209">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="97e24-209">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="97e24-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="97e24-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="97e24-211">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="97e24-211">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="97e24-212">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="97e24-212">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="97e24-213">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="97e24-213">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="97e24-214">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="97e24-214">JetDefragment2</span></span>](./jetdefragment2-function.md)
