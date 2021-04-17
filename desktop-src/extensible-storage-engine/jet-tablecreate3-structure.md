---
description: 'Saiba mais sobre: estrutura de JET_TABLECREATE3'
title: Estrutura JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798425"
---
# <a name="jet_tablecreate3-structure"></a><span data-ttu-id="61efd-103">Estrutura JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="61efd-103">JET_TABLECREATE3 Structure</span></span>


<span data-ttu-id="61efd-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="61efd-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="61efd-105">A estrutura de **JET_TABLECREATE3** contém as informações necessárias para criar uma tabela populada com colunas e índices em um banco de dados ESE (mecanismo de armazenamento extensível) e que designa uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="61efd-105">The **JET_TABLECREATE3** structure contains the information that is needed to create a table populated with columns and indexes in an Extensible Storage Engine (ESE) database, and that designates a callback function.</span></span> <span data-ttu-id="61efd-106">A estrutura de **JET_TABLECREATE3** é usada pela função [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) .</span><span class="sxs-lookup"><span data-stu-id="61efd-106">The **JET_TABLECREATE3** structure is used by the [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) function.</span></span>

<span data-ttu-id="61efd-107">A estrutura de **JET_TABLECREATE3** foi introduzida no sistema operacional Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61efd-107">The **JET_TABLECREATE3** structure was introduced in the Windows 7 operating system.</span></span>

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a><span data-ttu-id="61efd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="61efd-108">Members</span></span>

<span data-ttu-id="61efd-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="61efd-109">**cbStruct**</span></span>

<span data-ttu-id="61efd-110">O tamanho dessa estrutura em bytes (para expansão futura).</span><span class="sxs-lookup"><span data-stu-id="61efd-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="61efd-111">Ele deve ser definido como sizeof (JET_TABLECREATE3) em bytes.</span><span class="sxs-lookup"><span data-stu-id="61efd-111">It must be set to sizeof( JET_TABLECREATE3 ) in bytes.</span></span>

<span data-ttu-id="61efd-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="61efd-112">**szTableName**</span></span>

<span data-ttu-id="61efd-113">O nome da tabela a ser criada.</span><span class="sxs-lookup"><span data-stu-id="61efd-113">The name of the table to create.</span></span>

<span data-ttu-id="61efd-114">O nome deve atender às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="61efd-114">The name must meet the following conditions:</span></span>

  - <span data-ttu-id="61efd-115">Ele deve ter um valor menor que JET_cbNameMost, não incluindo o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="61efd-115">It must have a value that is less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="61efd-116">Ele deve consistir no seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ); ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="61efd-116">It must consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]); that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="61efd-117">Ele não deve começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="61efd-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="61efd-118">Ele deve consistir em pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="61efd-118">It must consist of at least one non-space character.</span></span>

<span data-ttu-id="61efd-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="61efd-119">**szTemplateTableName**</span></span>

<span data-ttu-id="61efd-120">O nome de uma tabela existente da qual herdar a linguagem de definição de dados (DDL) base.</span><span class="sxs-lookup"><span data-stu-id="61efd-120">The name of an existing table from which to inherit the base data definition language (DDL).</span></span> <span data-ttu-id="61efd-121">O uso de uma tabela de modelo permite a fácil criação de muitas tabelas com colunas e índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="61efd-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="61efd-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="61efd-122">**ulPages**</span></span>

<span data-ttu-id="61efd-123">O número inicial de páginas de banco de dados a serem alocadas para a tabela.</span><span class="sxs-lookup"><span data-stu-id="61efd-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="61efd-124">A especificação de um número maior que um pode reduzir a fragmentação se várias linhas forem inseridas nessa tabela.</span><span class="sxs-lookup"><span data-stu-id="61efd-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="61efd-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="61efd-125">**ulDensity**</span></span>

<span data-ttu-id="61efd-126">A densidade da tabela, em pontos percentuais.</span><span class="sxs-lookup"><span data-stu-id="61efd-126">The table density, in percentage points.</span></span> <span data-ttu-id="61efd-127">O número deve ser 0 ou estar no intervalo de 20 a 100.</span><span class="sxs-lookup"><span data-stu-id="61efd-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="61efd-128">Passar 0 significa que o valor padrão deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="61efd-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="61efd-129">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="61efd-129">The default value is 80.</span></span>

<span data-ttu-id="61efd-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="61efd-130">**rgcolumncreate**</span></span>

<span data-ttu-id="61efd-131">Uma matriz de estruturas [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada uma correspondendo a uma coluna a ser criada na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="61efd-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="61efd-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="61efd-132">**cColumns**</span></span>

<span data-ttu-id="61efd-133">O número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) no parâmetro *rgcolumncreate* .</span><span class="sxs-lookup"><span data-stu-id="61efd-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in the *rgcolumncreate* parameter.</span></span>

<span data-ttu-id="61efd-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="61efd-134">**rgindexcreate**</span></span>

<span data-ttu-id="61efd-135">Uma matriz de estruturas [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada uma delas corresponde a um índice a ser criado na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="61efd-135">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="61efd-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="61efd-136">**cIndexes**</span></span>

<span data-ttu-id="61efd-137">O número de elementos [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) no parâmetro *rgindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="61efd-137">The number of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) elements in the *rgindexcreate* parameter.</span></span>

<span data-ttu-id="61efd-138">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="61efd-138">**szCallback**</span></span>

<span data-ttu-id="61efd-139">A função que é chamada durante determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="61efd-139">The function that gets called during certain events.</span></span> <span data-ttu-id="61efd-140">**cbtyp** determina quando a função de retorno de chamada será chamada.</span><span class="sxs-lookup"><span data-stu-id="61efd-140">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="61efd-141">O formato de **szCallback** deve ser "função do módulo \! " — por exemplo, "Alpha \! beta" refere-se à função beta no módulo chamado "Alpha".</span><span class="sxs-lookup"><span data-stu-id="61efd-141">The format of **szCallback** must be "module\!function" — for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span>

<span data-ttu-id="61efd-142">O protótipo da função deve corresponder à função de retorno de chamada [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="61efd-142">The prototype of the function must match the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span>

<span data-ttu-id="61efd-143">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="61efd-143">**cbtyp**</span></span>

<span data-ttu-id="61efd-144">Descreve o tipo de função de retorno de chamada designado por **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="61efd-144">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="61efd-145">Para obter mais informações, consulte [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="61efd-145">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span>

<span data-ttu-id="61efd-146">Este campo de bits é composto de um ou mais valores de bit listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61efd-146">This bitfield is composed of one or more of the bit values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61efd-147">Valor</span><span class="sxs-lookup"><span data-stu-id="61efd-147">Value</span></span></p></th>
<th><p><span data-ttu-id="61efd-148">Significado</span><span class="sxs-lookup"><span data-stu-id="61efd-148">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61efd-149">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="61efd-149">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="61efd-150">A função de retorno de chamada será chamada quando uma coluna que pode ser finalizada tiver passado para zero.</span><span class="sxs-lookup"><span data-stu-id="61efd-150">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-151">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="61efd-151">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="61efd-152">A função de retorno de chamada será chamada antes da inserção do registro.</span><span class="sxs-lookup"><span data-stu-id="61efd-152">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61efd-153">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="61efd-153">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="61efd-154">A função de retorno de chamada será chamada depois que o mecanismo de banco de dados terminar de inserir um registro.</span><span class="sxs-lookup"><span data-stu-id="61efd-154">The callback function will be called after the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-155">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="61efd-155">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="61efd-156">A função de retorno de chamada será chamada antes da modificação de um registro.</span><span class="sxs-lookup"><span data-stu-id="61efd-156">The callback function will be called prior to the modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61efd-157">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="61efd-157">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="61efd-158">A função de retorno de chamada será chamada depois de concluir a modificação de um registro.</span><span class="sxs-lookup"><span data-stu-id="61efd-158">The callback function will be called after finishing the modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-159">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="61efd-159">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="61efd-160">A função de retorno de chamada será chamada antes da exclusão de um registro.</span><span class="sxs-lookup"><span data-stu-id="61efd-160">The callback function will be called prior to the deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61efd-161">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="61efd-161">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="61efd-162">A função de retorno de chamada será chamada depois que um registro tiver sido excluído.</span><span class="sxs-lookup"><span data-stu-id="61efd-162">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-163">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="61efd-163">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="61efd-164">A função de retorno de chamada será chamada para calcular um padrão definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61efd-164">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61efd-165">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="61efd-165">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="61efd-166">A função de retorno de chamada será chamada quando o armazenamento local associado a um cursor precisar ser liberado.</span><span class="sxs-lookup"><span data-stu-id="61efd-166">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-167">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="61efd-167">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="61efd-168">A função de retorno de chamada será chamada quando o armazenamento local associado a uma tabela precisar ser liberado.</span><span class="sxs-lookup"><span data-stu-id="61efd-168">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61efd-169">**grbit**</span><span class="sxs-lookup"><span data-stu-id="61efd-169">**grbit**</span></span>

<span data-ttu-id="61efd-170">Um grupo de bits que contém zero ou mais valores de opção de chamada listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61efd-170">A group of bits that contains zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61efd-171">Valor</span><span class="sxs-lookup"><span data-stu-id="61efd-171">Value</span></span></p></th>
<th><p><span data-ttu-id="61efd-172">Significado</span><span class="sxs-lookup"><span data-stu-id="61efd-172">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61efd-173">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="61efd-173">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="61efd-174">Impede operações DDL na tabela (como adicionar ou remover colunas).</span><span class="sxs-lookup"><span data-stu-id="61efd-174">Prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-175">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="61efd-175">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="61efd-176">Faz com que a tabela seja uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="61efd-176">Causes the table to be a template table.</span></span> <span data-ttu-id="61efd-177">As novas tabelas podem especificar o nome dessa tabela como sua tabela de modelos.</span><span class="sxs-lookup"><span data-stu-id="61efd-177">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="61efd-178">A configuração JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="61efd-178">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61efd-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="61efd-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="61efd-180">Deve ser usado em conjunto com JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="61efd-180">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="61efd-181">Preterido.</span><span class="sxs-lookup"><span data-stu-id="61efd-181">Deprecated.</span></span> <span data-ttu-id="61efd-182">Não use.</span><span class="sxs-lookup"><span data-stu-id="61efd-182">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61efd-183">**pSeqSpacehints**</span><span class="sxs-lookup"><span data-stu-id="61efd-183">**pSeqSpacehints**</span></span>

<span data-ttu-id="61efd-184">Um ponteiro para uma estrutura de [JET_SPACEHINTS](./jet-spacehints-structure.md) para o índice sequencial padrão.</span><span class="sxs-lookup"><span data-stu-id="61efd-184">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for default sequential index.</span></span>

<span data-ttu-id="61efd-185">o **pSeqSpacehints** foi introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61efd-185">**pSeqSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="61efd-186">**pLVSpacehints**</span><span class="sxs-lookup"><span data-stu-id="61efd-186">**pLVSpacehints**</span></span>

<span data-ttu-id="61efd-187">Um ponteiro para uma estrutura de [JET_SPACEHINTS](./jet-spacehints-structure.md) para uma árvore de valores longos separados.</span><span class="sxs-lookup"><span data-stu-id="61efd-187">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for a Separated Long Value tree.</span></span>

<span data-ttu-id="61efd-188">o **pLVSpacehints** foi introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61efd-188">**pLVSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="61efd-189">**cbSeparateLV**</span><span class="sxs-lookup"><span data-stu-id="61efd-189">**cbSeparateLV**</span></span>

<span data-ttu-id="61efd-190">O tamanho para separar um LV intrínseco do registro principal.</span><span class="sxs-lookup"><span data-stu-id="61efd-190">The size to separate an intrinsic LV from the primary record.</span></span> <span data-ttu-id="61efd-191">Qualquer estrutura c de valor longo para uma árvore LV separada.</span><span class="sxs-lookup"><span data-stu-id="61efd-191">Any long-value c structure for a Separated LV tree.</span></span> <span data-ttu-id="61efd-192">Para obter mais informações, consulte ng-Value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span><span class="sxs-lookup"><span data-stu-id="61efd-192">For more information, see ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span></span> <span data-ttu-id="61efd-193">Colunas de valor longo menores que esse valor podem ser separadas se o registro se tornar muito grande.</span><span class="sxs-lookup"><span data-stu-id="61efd-193">Long-value columns smaller than this value may be separated if the record becomes too large.</span></span>

<span data-ttu-id="61efd-194">o **cbSeparateLV** foi introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61efd-194">**cbSeparateLV** was introduced in Windows 7.</span></span>

<span data-ttu-id="61efd-195">**TableID**</span><span class="sxs-lookup"><span data-stu-id="61efd-195">**tableid**</span></span>

<span data-ttu-id="61efd-196">Um campo de saída que mantém o [JET_TABLEID](./jet-tableid.md) da nova tabela se a chamada à API for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="61efd-196">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="61efd-197">Se a chamada à API falhar, o valor será indefinido.</span><span class="sxs-lookup"><span data-stu-id="61efd-197">If the API call fails, the value is undefined.</span></span> <span data-ttu-id="61efd-198">Esta tabela é aberta exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="61efd-198">This table is opened exclusively.</span></span>

<span data-ttu-id="61efd-199">**cCreated**</span><span class="sxs-lookup"><span data-stu-id="61efd-199">**cCreated**</span></span>

<span data-ttu-id="61efd-200">Um campo de saída que contém a contagem de objetos que são criados se a chamada à API for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="61efd-200">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="61efd-201">Se a chamada à API falhar, o valor será indefinido.</span><span class="sxs-lookup"><span data-stu-id="61efd-201">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="61efd-202">A contagem de objetos criados é igual à soma de colunas, tabelas e índices criados com êxito.</span><span class="sxs-lookup"><span data-stu-id="61efd-202">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="61efd-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61efd-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61efd-204"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="61efd-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="61efd-205">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="61efd-205">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-206"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="61efd-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="61efd-207">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="61efd-207">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61efd-208"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="61efd-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="61efd-209">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="61efd-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61efd-210"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="61efd-210"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="61efd-211">Implementado como <strong>JET_TABLECREATE3_W</strong> (Unicode) e <strong>JET_TABLECREATE3_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="61efd-211">Implemented as <strong>JET_TABLECREATE3_W</strong> (Unicode) and <strong>JET_TABLECREATE3_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="61efd-212">Confira também</span><span class="sxs-lookup"><span data-stu-id="61efd-212">See also</span></span>

[<span data-ttu-id="61efd-213">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="61efd-213">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="61efd-214">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="61efd-214">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="61efd-215">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="61efd-215">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="61efd-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="61efd-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="61efd-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="61efd-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="61efd-218">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="61efd-218">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="61efd-219">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="61efd-219">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="61efd-220">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="61efd-220">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="61efd-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="61efd-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="61efd-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="61efd-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="61efd-223">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="61efd-223">JetDefragment2</span></span>](./jetdefragment2-function.md)
