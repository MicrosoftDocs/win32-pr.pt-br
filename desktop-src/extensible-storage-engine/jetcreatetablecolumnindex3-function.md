---
description: 'Saiba mais sobre: função JetCreateTableColumnIndex3'
title: Função JetCreateTableColumnIndex3
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766563"
---
# <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="537f9-103">Função JetCreateTableColumnIndex3</span><span class="sxs-lookup"><span data-stu-id="537f9-103">JetCreateTableColumnIndex3 Function</span></span>


<span data-ttu-id="537f9-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="537f9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="537f9-105">Função JetCreateTableColumnIndex3</span><span class="sxs-lookup"><span data-stu-id="537f9-105">JetCreateTableColumnIndex3 Function</span></span>

<span data-ttu-id="537f9-106">A função **JetCreateTableColumnIndex3** cria uma tabela em um banco de dados ESE com um conjunto inicial de índices e um conjunto inicial de colunas de uma matriz de estruturas de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="537f9-106">The **JetCreateTableColumnIndex3** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="537f9-107">A estrutura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permite que uma função de retorno de chamada seja especificada.</span><span class="sxs-lookup"><span data-stu-id="537f9-107">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="537f9-108">**Windows 7:** o **JetCreateTableColumnIndex3** é introduzido no sistema operacional Windows 7.</span><span class="sxs-lookup"><span data-stu-id="537f9-108">**Windows 7:** **JetCreateTableColumnIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="537f9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="537f9-109">Parameters</span></span>

<span data-ttu-id="537f9-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="537f9-110">*sesid*</span></span>

<span data-ttu-id="537f9-111">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="537f9-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="537f9-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="537f9-112">*dbid*</span></span>

<span data-ttu-id="537f9-113">O identificador de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="537f9-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="537f9-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="537f9-114">*ptablecreate*</span></span>

<span data-ttu-id="537f9-115">Um ponteiro para uma estrutura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) que define a tabela a ser criada.</span><span class="sxs-lookup"><span data-stu-id="537f9-115">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="537f9-116">Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="537f9-116">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="537f9-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="537f9-117">Return Value</span></span>

<span data-ttu-id="537f9-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="537f9-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="537f9-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="537f9-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="537f9-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="537f9-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="537f9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="537f9-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="537f9-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="537f9-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="537f9-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="537f9-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="537f9-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="537f9-125">A função de retorno de chamada não pôde ser resolvida.</span><span class="sxs-lookup"><span data-stu-id="537f9-125">The callback function could not be resolved.</span></span> <span data-ttu-id="537f9-126">A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada.</span><span class="sxs-lookup"><span data-stu-id="537f9-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="537f9-127">Com o registro em log suficiente habilitado, o log de eventos fornecerá mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="537f9-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="537f9-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="537f9-129">Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</span><span class="sxs-lookup"><span data-stu-id="537f9-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="537f9-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="537f9-131">Se ptablecreate- &gt; grbit especificar JET_bitTableCreateTemplateTable, mas ptablecreate- &gt; szTemplateTableName será definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="537f9-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="537f9-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="537f9-133">Já existe uma coluna.</span><span class="sxs-lookup"><span data-stu-id="537f9-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="537f9-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="537f9-135">Foi feita uma tentativa de indexar uma coluna não existente.</span><span class="sxs-lookup"><span data-stu-id="537f9-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="537f9-136">A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</span><span class="sxs-lookup"><span data-stu-id="537f9-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="537f9-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="537f9-138">Foi feita uma tentativa de adicionar uma coluna redundante.</span><span class="sxs-lookup"><span data-stu-id="537f9-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="537f9-139">Não deve haver mais de uma coluna de incremento automático e não há mais de uma coluna de versão por tabela.</span><span class="sxs-lookup"><span data-stu-id="537f9-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="537f9-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="537f9-141">Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número inferior a 20 ou maior que 100.</span><span class="sxs-lookup"><span data-stu-id="537f9-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="537f9-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="537f9-143">Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha JET_bitTableCreateTemplateTable definido).</span><span class="sxs-lookup"><span data-stu-id="537f9-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="537f9-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="537f9-145">Foi feita uma tentativa de definir dois índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="537f9-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="537f9-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="537f9-147">Foi feita uma tentativa de especificar mais de um índice primário para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="537f9-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="537f9-148">Uma tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="537f9-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="537f9-149">Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</span><span class="sxs-lookup"><span data-stu-id="537f9-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="537f9-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="537f9-151">Uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="537f9-151">An invalid index definition was specified.</span></span> <span data-ttu-id="537f9-152">A seguir estão alguns dos possíveis motivos para receber esse erro:</span><span class="sxs-lookup"><span data-stu-id="537f9-152">The following are some of the possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="537f9-153">Um índice primário é condicional (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</span><span class="sxs-lookup"><span data-stu-id="537f9-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="537f9-154">Windows Server 2003 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="537f9-154">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="537f9-155">Tentativa de criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, o membro <strong>grbit</strong> da estrutura de JET_INDEXCREATE2 tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</span><span class="sxs-lookup"><span data-stu-id="537f9-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the JET_INDEXCREATE2 structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="537f9-156">Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="537f9-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="537f9-157">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter uma discussão sobre definições válidas.</span><span class="sxs-lookup"><span data-stu-id="537f9-157">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="537f9-158">Definir o membro <strong>cbVarSegMac</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</span><span class="sxs-lookup"><span data-stu-id="537f9-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="537f9-159">Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="537f9-159">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="537f9-160">Algumas causas comuns incluem o membro <strong>pidxunicode</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</span><span class="sxs-lookup"><span data-stu-id="537f9-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="537f9-161">Especificando uma coluna com valores múltiplos para um índice primário.</span><span class="sxs-lookup"><span data-stu-id="537f9-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="537f9-162">Tentando indexar muitas colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="537f9-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="537f9-163">O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ser maior que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="537f9-163">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="537f9-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="537f9-165">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="537f9-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="537f9-166">Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites.</span><span class="sxs-lookup"><span data-stu-id="537f9-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="537f9-167">Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="537f9-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="537f9-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="537f9-169">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="537f9-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="537f9-170">Um índice de tupla não pode ser exclusivo (ou seja, o membro <em>grbit</em> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexUnique definido).</span><span class="sxs-lookup"><span data-stu-id="537f9-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="537f9-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="537f9-172">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="537f9-172">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="537f9-173">Um índice de tupla só pode ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiver JET_bitIndexTuples definido e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especificar mais de uma coluna).</span><span class="sxs-lookup"><span data-stu-id="537f9-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="537f9-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="537f9-175">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="537f9-175">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="537f9-176">Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</span><span class="sxs-lookup"><span data-stu-id="537f9-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="537f9-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="537f9-178">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="537f9-178">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="537f9-179">Um índice de tupla só pode estar em uma coluna de texto ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="537f9-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="537f9-180">Uma tentativa de indexar outras colunas (como colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="537f9-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="537f9-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="537f9-182">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="537f9-182">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="537f9-183">Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> seja definida.</span><span class="sxs-lookup"><span data-stu-id="537f9-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="537f9-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="537f9-185">Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</span><span class="sxs-lookup"><span data-stu-id="537f9-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="537f9-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="537f9-187">O membro <strong>CP</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida.</span><span class="sxs-lookup"><span data-stu-id="537f9-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="537f9-188">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="537f9-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="537f9-189">Um valor de 0 significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="537f9-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="537f9-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="537f9-191">O membro <strong>coltyp</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</span><span class="sxs-lookup"><span data-stu-id="537f9-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="537f9-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="537f9-193">A seguir estão alguns motivos pelos quais esse erro pode ocorrer:</span><span class="sxs-lookup"><span data-stu-id="537f9-193">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="537f9-194">O membro <strong>rgindexcreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="537f9-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="537f9-195">O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="537f9-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="537f9-196">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não foi definido como um valor válido.</span><span class="sxs-lookup"><span data-stu-id="537f9-196">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="537f9-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="537f9-198">Uma combinação inválida de membros <strong>grbit</strong> foi especificada em <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span><span class="sxs-lookup"><span data-stu-id="537f9-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span></span></p>
<p><span data-ttu-id="537f9-199">A definição do índice é inválida porque o membro <strong>grbit</strong> contém valores inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="537f9-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="537f9-200">Estes são alguns motivos possíveis:</span><span class="sxs-lookup"><span data-stu-id="537f9-200">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="537f9-201">Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary foi passado com JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="537f9-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="537f9-202">Um índice vazio não ignora quaisquer membros nulos (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</span><span class="sxs-lookup"><span data-stu-id="537f9-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="537f9-203">Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</span><span class="sxs-lookup"><span data-stu-id="537f9-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="537f9-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="537f9-205">Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> da estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que é apontada pelo membro <strong>pidxunicode</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ou pelo campo <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="537f9-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="537f9-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="537f9-207">Um parâmetro inválido foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="537f9-207">An invalid parameter was given.</span></span> <span data-ttu-id="537f9-208">Estes são alguns motivos possíveis:</span><span class="sxs-lookup"><span data-stu-id="537f9-208">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="537f9-209">O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> é nulo.</span><span class="sxs-lookup"><span data-stu-id="537f9-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="537f9-210">O membro <strong>cbStruct</strong> de uma das estruturas de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dadas no membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="537f9-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="537f9-211">O membro <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="537f9-211">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="537f9-212">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="537f9-212">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="537f9-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="537f9-214">O registro é muito grande.</span><span class="sxs-lookup"><span data-stu-id="537f9-214">The record is too big.</span></span> <span data-ttu-id="537f9-215">A soma do membro <strong>cbMax</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="537f9-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="537f9-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="537f9-217">A tabela já existe.</span><span class="sxs-lookup"><span data-stu-id="537f9-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="537f9-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="537f9-219">Foi feita uma tentativa de adicionar muitas colunas à tabela.</span><span class="sxs-lookup"><span data-stu-id="537f9-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="537f9-220">Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="537f9-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="537f9-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="537f9-222">Ocorreu um erro ao tentar normalizar uma coluna Unicode.</span><span class="sxs-lookup"><span data-stu-id="537f9-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="537f9-223">Isso pode ser causado pela execução de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="537f9-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-224">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="537f9-224">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="537f9-225">Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</span><span class="sxs-lookup"><span data-stu-id="537f9-225">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="537f9-226">Comentários</span><span class="sxs-lookup"><span data-stu-id="537f9-226">Remarks</span></span>

<span data-ttu-id="537f9-227">O nome **JetCreateTableColumnIndex3** vem da ordem de criação dos objetos: ele primeiro cria uma tabela, colunas e, finalmente, índices.</span><span class="sxs-lookup"><span data-stu-id="537f9-227">The name **JetCreateTableColumnIndex3** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="537f9-228">**JetCreateTableColumnIndex3** cria uma tabela com um conjunto inicial de colunas e índices.</span><span class="sxs-lookup"><span data-stu-id="537f9-228">**JetCreateTableColumnIndex3** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="537f9-229">Colunas e índices adicionais podem ser adicionados e removidos dinamicamente com [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="537f9-229">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="537f9-230">Assim como o [JetOpenTable](./jetopentable-function.md), quando o aplicativo é feito usando a *tabelaid* retornada, ele normalmente deve ser fechado com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="537f9-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="537f9-231">Requisitos</span><span class="sxs-lookup"><span data-stu-id="537f9-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="537f9-232"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="537f9-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="537f9-233">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="537f9-233">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-234"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="537f9-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="537f9-235">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="537f9-235">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-236"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="537f9-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="537f9-237">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="537f9-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-238"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="537f9-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="537f9-239">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="537f9-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="537f9-240"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="537f9-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="537f9-241">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="537f9-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="537f9-242"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="537f9-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="537f9-243">Implementado como <strong>JetCreateTableColumnIndex3W</strong> (Unicode) e <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="537f9-243">Implemented as <strong>JetCreateTableColumnIndex3W</strong> (Unicode) and <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="537f9-244">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="537f9-244">See Also</span></span>

[<span data-ttu-id="537f9-245">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="537f9-245">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="537f9-246">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="537f9-246">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="537f9-247">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="537f9-247">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="537f9-248">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="537f9-248">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="537f9-249">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="537f9-249">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="537f9-250">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="537f9-250">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="537f9-251">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="537f9-251">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="537f9-252">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="537f9-252">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="537f9-253">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="537f9-253">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="537f9-254">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="537f9-254">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="537f9-255">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="537f9-255">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="537f9-256">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="537f9-256">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="537f9-257">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="537f9-257">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="537f9-258">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="537f9-258">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="537f9-259">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="537f9-259">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="537f9-260">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="537f9-260">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="537f9-261">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="537f9-261">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="537f9-262">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="537f9-262">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="537f9-263">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="537f9-263">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
