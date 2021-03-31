---
description: 'Saiba mais sobre: estrutura de JET_TABLECREATE'
title: Estrutura JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089888"
---
# <a name="jet_tablecreate-structure"></a><span data-ttu-id="22ee1-103">Estrutura JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="22ee1-103">JET_TABLECREATE Structure</span></span>


<span data-ttu-id="22ee1-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="22ee1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate-structure"></a><span data-ttu-id="22ee1-105">Estrutura JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="22ee1-105">JET_TABLECREATE Structure</span></span>

<span data-ttu-id="22ee1-106">A estrutura de **JET_TABLECREATE** contém as informações necessárias para criar uma tabela populada com colunas e índices em um banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="22ee1-106">The **JET_TABLECREATE** structure contains the information that is necessary to create a table populated with columns and indexes in an ESE database.</span></span> <span data-ttu-id="22ee1-107">A estrutura de **JET_TABLECREATE** é usada pelo [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span><span class="sxs-lookup"><span data-stu-id="22ee1-107">The **JET_TABLECREATE** structure is used by [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span></span>

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a><span data-ttu-id="22ee1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="22ee1-108">Members</span></span>

<span data-ttu-id="22ee1-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="22ee1-109">**cbStruct**</span></span>

<span data-ttu-id="22ee1-110">O tamanho dessa estrutura em bytes (para expansão futura).</span><span class="sxs-lookup"><span data-stu-id="22ee1-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="22ee1-111">Ele deve ser definido como sizeof (JET_TABLECREATE) em bytes.</span><span class="sxs-lookup"><span data-stu-id="22ee1-111">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="22ee1-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="22ee1-112">**szTableName**</span></span>

<span data-ttu-id="22ee1-113">O nome da tabela a ser criada.</span><span class="sxs-lookup"><span data-stu-id="22ee1-113">The name of the table to create.</span></span>

<span data-ttu-id="22ee1-114">O nome deve usar atender às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="22ee1-114">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="22ee1-115">Ter um valor menor que JET_cbNameMost, não incluindo o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="22ee1-115">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="22ee1-116">Consiste no seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ), ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="22ee1-116">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="22ee1-117">Não comece com um espaço.</span><span class="sxs-lookup"><span data-stu-id="22ee1-117">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="22ee1-118">Consistir em pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="22ee1-118">Consist of at least one non-space character.</span></span>

<span data-ttu-id="22ee1-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="22ee1-119">**szTemplateTableName**</span></span>

<span data-ttu-id="22ee1-120">O nome de uma tabela já existente da qual herdar DDL base (linguagem de definição de dados).</span><span class="sxs-lookup"><span data-stu-id="22ee1-120">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="22ee1-121">O uso de uma tabela de modelo permite a fácil criação de muitas tabelas com colunas e índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="22ee1-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="22ee1-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="22ee1-122">**ulPages**</span></span>

<span data-ttu-id="22ee1-123">O número inicial de páginas de banco de dados a serem alocadas para a tabela.</span><span class="sxs-lookup"><span data-stu-id="22ee1-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="22ee1-124">A especificação de um número maior que um pode reduzir a fragmentação se várias linhas forem inseridas nessa tabela.</span><span class="sxs-lookup"><span data-stu-id="22ee1-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="22ee1-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="22ee1-125">**ulDensity**</span></span>

<span data-ttu-id="22ee1-126">A densidade da tabela, em pontos percentuais.</span><span class="sxs-lookup"><span data-stu-id="22ee1-126">The table density, in percentage points.</span></span> <span data-ttu-id="22ee1-127">O número deve ser 0 ou estar no intervalo de 20 a 100.</span><span class="sxs-lookup"><span data-stu-id="22ee1-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="22ee1-128">Passar 0 significa que o valor padrão deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="22ee1-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="22ee1-129">O padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="22ee1-129">The default is 80.</span></span>

<span data-ttu-id="22ee1-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="22ee1-130">**rgcolumncreate**</span></span>

<span data-ttu-id="22ee1-131">Uma matriz de estruturas [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada uma correspondendo a uma coluna a ser criada na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="22ee1-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="22ee1-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="22ee1-132">**cColumns**</span></span>

<span data-ttu-id="22ee1-133">O número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) em **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="22ee1-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="22ee1-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="22ee1-134">**rgindexcreate**</span></span>

<span data-ttu-id="22ee1-135">Uma matriz de estruturas [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada uma delas corresponde a um índice a ser criado na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="22ee1-135">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="22ee1-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="22ee1-136">**cIndexes**</span></span>

<span data-ttu-id="22ee1-137">O número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) em **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="22ee1-137">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="22ee1-138">**grbit**</span><span class="sxs-lookup"><span data-stu-id="22ee1-138">**grbit**</span></span>

<span data-ttu-id="22ee1-139">Um grupo de bits que contém as opções para essa chamada, que incluem zero ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="22ee1-139">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22ee1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="22ee1-140">Value</span></span></p></th>
<th><p><span data-ttu-id="22ee1-141">Significado</span><span class="sxs-lookup"><span data-stu-id="22ee1-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22ee1-142">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="22ee1-142">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="22ee1-143">A configuração JET_bitTableCreateFixedDDL impede operações DDL na tabela (como adicionar ou remover colunas).</span><span class="sxs-lookup"><span data-stu-id="22ee1-143">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22ee1-144">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="22ee1-144">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="22ee1-145">A configuração JET_bitTableCreateTemplateTable faz com que a tabela seja uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="22ee1-145">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="22ee1-146">As novas tabelas podem especificar o nome dessa tabela como sua tabela de modelos.</span><span class="sxs-lookup"><span data-stu-id="22ee1-146">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="22ee1-147">A configuração JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="22ee1-147">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22ee1-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="22ee1-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="22ee1-149">Preterido.</span><span class="sxs-lookup"><span data-stu-id="22ee1-149">Deprecated.</span></span> <span data-ttu-id="22ee1-150">Não use.</span><span class="sxs-lookup"><span data-stu-id="22ee1-150">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22ee1-151">**TableID**</span><span class="sxs-lookup"><span data-stu-id="22ee1-151">**tableid**</span></span>

<span data-ttu-id="22ee1-152">Um campo de saída que mantém o [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="22ee1-152">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="22ee1-153">Se a chamada à API falhar, o valor será indefinido.</span><span class="sxs-lookup"><span data-stu-id="22ee1-153">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="22ee1-154">**cCreated**</span><span class="sxs-lookup"><span data-stu-id="22ee1-154">**cCreated**</span></span>

<span data-ttu-id="22ee1-155">Um campo de saída que contém a contagem de objetos criados se a chamada à API for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="22ee1-155">An output field that contains the count of objects created if the API call succeeds.</span></span> <span data-ttu-id="22ee1-156">Se a chamada à API falhar, o valor será indefinido.</span><span class="sxs-lookup"><span data-stu-id="22ee1-156">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="22ee1-157">A contagem de objetos criados é igual à soma de colunas, tabelas e índices criados com êxito.</span><span class="sxs-lookup"><span data-stu-id="22ee1-157">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="22ee1-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22ee1-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22ee1-159"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="22ee1-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="22ee1-160">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="22ee1-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22ee1-161"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="22ee1-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="22ee1-162">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="22ee1-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22ee1-163"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="22ee1-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="22ee1-164">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="22ee1-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22ee1-165"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="22ee1-165"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="22ee1-166">Implementado como <strong>JET_TABLECREATE_W</strong> (Unicode) e <strong>JET_TABLECREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="22ee1-166">Implemented as <strong>JET_TABLECREATE_W</strong> (Unicode) and <strong>JET_TABLECREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="22ee1-167">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="22ee1-167">See Also</span></span>

[<span data-ttu-id="22ee1-168">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="22ee1-168">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="22ee1-169">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="22ee1-169">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="22ee1-170">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="22ee1-170">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="22ee1-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="22ee1-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="22ee1-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="22ee1-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="22ee1-173">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="22ee1-173">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="22ee1-174">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="22ee1-174">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="22ee1-175">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="22ee1-175">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="22ee1-176">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="22ee1-176">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="22ee1-177">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="22ee1-177">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
