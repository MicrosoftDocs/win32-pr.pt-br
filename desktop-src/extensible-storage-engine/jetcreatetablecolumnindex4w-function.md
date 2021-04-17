---
description: 'Saiba mais sobre: função JetCreateTableColumnIndex4W'
title: Função JetCreateTableColumnIndex4W
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766445"
---
# <a name="jetcreatetablecolumnindex4w-function"></a><span data-ttu-id="e0905-103">Função JetCreateTableColumnIndex4W</span><span class="sxs-lookup"><span data-stu-id="e0905-103">JetCreateTableColumnIndex4W Function</span></span>


<span data-ttu-id="e0905-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0905-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="e0905-105">A função **JetCreateTableColumnIndex4W** cria uma tabela em um ESE (mecanismo de armazenamento extensível) (banco de dados com um conjunto inicial de índices e um conjunto inicial de colunas de uma matriz de estruturas de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e0905-105">The **JetCreateTableColumnIndex4W** function creates a table in an Extensible Storage Engine (ESE( database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="e0905-106">A estrutura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permite que uma função de retorno de chamada seja especificada.</span><span class="sxs-lookup"><span data-stu-id="e0905-106">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="e0905-107">A função **JetCreateTableColumnIndex4W** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e0905-107">The **JetCreateTableColumnIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a><span data-ttu-id="e0905-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0905-108">Parameters</span></span>

<span data-ttu-id="e0905-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e0905-109">*sesid*</span></span>

<span data-ttu-id="e0905-110">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="e0905-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="e0905-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="e0905-111">*dbid*</span></span>

<span data-ttu-id="e0905-112">O identificador de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="e0905-112">The database identifier to use for the API call.</span></span>

<span data-ttu-id="e0905-113">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="e0905-113">*ptablecreate*</span></span>

<span data-ttu-id="e0905-114">Um ponteiro para uma estrutura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) que define a tabela a ser criada.</span><span class="sxs-lookup"><span data-stu-id="e0905-114">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="e0905-115">Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e0905-115">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="e0905-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0905-116">Return value</span></span>

<span data-ttu-id="e0905-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0905-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="e0905-118">Para obter mais informações sobre os possíveis erros de ESE (Extensible Storage enginge), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e0905-118">For more information about the possible Extensible Storage Enginge (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0905-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0905-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="e0905-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0905-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0905-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e0905-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e0905-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e0905-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-123">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="e0905-123">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="e0905-124">A função de retorno de chamada não pôde ser resolvida.</span><span class="sxs-lookup"><span data-stu-id="e0905-124">The callback function could not be resolved.</span></span> <span data-ttu-id="e0905-125">A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada.</span><span class="sxs-lookup"><span data-stu-id="e0905-125">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="e0905-126">Com o registro em log suficiente habilitado, o log de eventos fornecerá mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e0905-126">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-127">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="e0905-127">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="e0905-128">Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</span><span class="sxs-lookup"><span data-stu-id="e0905-128">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-129">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="e0905-129">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="e0905-130">Retornado se o parâmetro <em>ptablecreate- &gt; grbit</em> especifica o valor JET_bitTableCreateTemplateTable, mas o parâmetro <em>ptablecreate- &gt; szTemplateTableName</em> está definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="e0905-130">Returned if the <em>ptablecreate-&gt;grbit</em> parameter specifies the JET_bitTableCreateTemplateTable value, but the <em>ptablecreate-&gt;szTemplateTableName</em> parameter is set to null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-131">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="e0905-131">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="e0905-132">Já existe uma coluna.</span><span class="sxs-lookup"><span data-stu-id="e0905-132">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="e0905-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="e0905-134">Foi feita uma tentativa de indexar uma coluna inexistente.</span><span class="sxs-lookup"><span data-stu-id="e0905-134">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="e0905-135">Uma tentativa de indexar condicionalmente uma coluna inexistente também pode produzir esse erro.</span><span class="sxs-lookup"><span data-stu-id="e0905-135">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-136">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="e0905-136">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="e0905-137">Foi feita uma tentativa de adicionar uma coluna redundante.</span><span class="sxs-lookup"><span data-stu-id="e0905-137">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="e0905-138">Não deve existir mais de uma coluna de incremento automático e não existe mais de uma coluna de versão por tabela.</span><span class="sxs-lookup"><span data-stu-id="e0905-138">No more than one autoincrement column should exist, and no more than one version column should exist per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-139">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="e0905-139">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="e0905-140">Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número inferior a 20 ou maior que 100.</span><span class="sxs-lookup"><span data-stu-id="e0905-140">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-141">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="e0905-141">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="e0905-142">Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha o valor de parâmetro JET_bitTableCreateTemplateTable definido).</span><span class="sxs-lookup"><span data-stu-id="e0905-142">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have the JET_bitTableCreateTemplateTable parameter value set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-143">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="e0905-143">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="e0905-144">Foi feita uma tentativa de definir dois índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="e0905-144">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-145">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="e0905-145">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="e0905-146">Foi feita uma tentativa de especificar mais de um índice primário para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="e0905-146">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="e0905-147">Uma tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="e0905-147">A table must have exactly one primary index.</span></span> <span data-ttu-id="e0905-148">Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</span><span class="sxs-lookup"><span data-stu-id="e0905-148">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-149">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="e0905-149">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="e0905-150">Uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="e0905-150">An invalid index definition was specified.</span></span> <span data-ttu-id="e0905-151">Estes são alguns dos motivos possíveis para esse erro:</span><span class="sxs-lookup"><span data-stu-id="e0905-151">The following are some of the possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0905-152">Um índice primário é condicional (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem o valor JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</span><span class="sxs-lookup"><span data-stu-id="e0905-152">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexPrimary value set, and the <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="e0905-153">Aplica-se às versões do sistema operacional Windows Server a partir do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e0905-153">Applies to versions of the Windows Server operating system starting with Windows Server 2003.</span></span> <span data-ttu-id="e0905-154">Uma tentativa de criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, o membro <strong>grbit</strong> da estrutura de <strong>JET_INDEXCREATE2</strong> tem JET_bitIndexTupleLimits valor definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</span><span class="sxs-lookup"><span data-stu-id="e0905-154">An attempt to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the <strong>JET_INDEXCREATE2</strong> structure has JET_bitIndexTupleLimits value set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="e0905-155">Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="e0905-155">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="e0905-156">Para obter informações sobre definições válidas, consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="e0905-156">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="e0905-157">Definir o membro <strong>cbVarSegMac</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ser maior que o valor de JET_cbPrimaryKeyMost (para um índice primário) ou maior que o valor de JET_cbSecondaryKeyMost (para um índice secundário).</span><span class="sxs-lookup"><span data-stu-id="e0905-157">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than the JET_cbPrimaryKeyMost value (for a primary index) or greater than the JET_cbSecondaryKeyMost value (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="e0905-158">Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tenha o bit de valor JET_bitIndexUnicode definido no membro <strong>grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="e0905-158">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode value bit set in the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span> <span data-ttu-id="e0905-159">Algumas causas comuns incluem o membro <strong>pidxunicode</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</span><span class="sxs-lookup"><span data-stu-id="e0905-159">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="e0905-160">Especificando uma coluna com valores de um índice primário.</span><span class="sxs-lookup"><span data-stu-id="e0905-160">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="e0905-161">Tentando indexar muitas colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="e0905-161">Trying to index too many conditional columns.</span></span> <span data-ttu-id="e0905-162">O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ser maior que <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0905-162">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-163">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="e0905-163">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="e0905-164">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0905-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="e0905-165">Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites.</span><span class="sxs-lookup"><span data-stu-id="e0905-165">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="e0905-166">Para obter mais informações, consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="e0905-166">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-167">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="e0905-167">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="e0905-168">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0905-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="e0905-169">Um índice de tupla não pode ser exclusivo (ou seja, o membro <em>grbit</em> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter os valores JET_bitIndexPrimary e JET_bitIndexUnique definidos).</span><span class="sxs-lookup"><span data-stu-id="e0905-169">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique values set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-170">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="e0905-170">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="e0905-171">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0905-171">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="e0905-172">Um índice de tupla só pode ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiver JET_bitIndexTuples valor definido e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especificar mais de uma coluna).</span><span class="sxs-lookup"><span data-stu-id="e0905-172">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples value set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-173">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="e0905-173">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="e0905-174">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0905-174">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="e0905-175">Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</span><span class="sxs-lookup"><span data-stu-id="e0905-175">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-176">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="e0905-176">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="e0905-177">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0905-177">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="e0905-178">Um índice de tupla só pode estar em uma coluna de texto ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0905-178">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="e0905-179">Uma tentativa de indexar outras colunas (como colunas binárias) resultará em um código de resposta JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="e0905-179">An attempt to index other columns (such as binary columns) will result in a JET_errIndexTuplesTextColumnsOnly response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-180">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="e0905-180">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="e0905-181">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0905-181">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="e0905-182">Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> seja definida.</span><span class="sxs-lookup"><span data-stu-id="e0905-182">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-183">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="e0905-183">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="e0905-184">Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</span><span class="sxs-lookup"><span data-stu-id="e0905-184">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-185">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="e0905-185">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="e0905-186">O membro <strong>CP</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida.</span><span class="sxs-lookup"><span data-stu-id="e0905-186">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="e0905-187">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="e0905-187">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="e0905-188">Um valor de 0 significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="e0905-188">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-189">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="e0905-189">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="e0905-190">O membro <strong>coltyp</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</span><span class="sxs-lookup"><span data-stu-id="e0905-190">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-191">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="e0905-191">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="e0905-192">A seguir estão alguns motivos pelos quais esse erro pode ocorrer:</span><span class="sxs-lookup"><span data-stu-id="e0905-192">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0905-193">O membro <strong>rgindexcreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="e0905-193">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="e0905-194">O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="e0905-194">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="e0905-195">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não foi definido como um valor válido.</span><span class="sxs-lookup"><span data-stu-id="e0905-195">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-196">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="e0905-196">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="e0905-197">Uma combinação inválida de membros <strong>grbit</strong> foi especificada na estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> .</span><span class="sxs-lookup"><span data-stu-id="e0905-197">An invalid combination of <strong>grbit</strong> members was specified in the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure.</span></span></p>
<p><span data-ttu-id="e0905-198">A definição do índice é inválida porque o membro <strong>grbit</strong> contém valores inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="e0905-198">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="e0905-199">Estes são alguns motivos possíveis:</span><span class="sxs-lookup"><span data-stu-id="e0905-199">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0905-200">Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary valor foi passado com os valores de JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="e0905-200">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary value was passed with the JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull values).</span></span></p></li>
<li><p><span data-ttu-id="e0905-201">Um índice vazio não ignora quaisquer membros nulos (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem o valor de JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull valor definido).</span><span class="sxs-lookup"><span data-stu-id="e0905-201">An empty index does not ignore any null members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexEmpty value set, but does not have JET_bitIndexIgnoreAnyNull value set).</span></span></p></li>
<li><p><span data-ttu-id="e0905-202">Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</span><span class="sxs-lookup"><span data-stu-id="e0905-202">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="e0905-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="e0905-204">Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> da estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que o membro <strong>pidxunicode</strong> na estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> aponta para ou por meio do campo <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="e0905-204">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure that the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure points to, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-205">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e0905-205">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e0905-206">Um parâmetro inválido foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="e0905-206">An invalid parameter was given.</span></span> <span data-ttu-id="e0905-207">Estes são alguns motivos possíveis:</span><span class="sxs-lookup"><span data-stu-id="e0905-207">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0905-208">O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> é nulo.</span><span class="sxs-lookup"><span data-stu-id="e0905-208">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is null.</span></span></p></li>
<li><p><span data-ttu-id="e0905-209">O membro <strong>cbStruct</strong> de uma das estruturas de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dadas no membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="e0905-209">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="e0905-210">O membro <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="e0905-210">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="e0905-211">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="e0905-211">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-212">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="e0905-212">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="e0905-213">O registro é muito grande.</span><span class="sxs-lookup"><span data-stu-id="e0905-213">The record is too big.</span></span> <span data-ttu-id="e0905-214">A soma do membro <strong>cbMax</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="e0905-214">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-215">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="e0905-215">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="e0905-216">A tabela já existe.</span><span class="sxs-lookup"><span data-stu-id="e0905-216">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-217">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="e0905-217">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="e0905-218">Foi feita uma tentativa de adicionar muitas colunas à tabela.</span><span class="sxs-lookup"><span data-stu-id="e0905-218">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="e0905-219">Uma tabela não pode ter mais de <strong>JET_ccolFixedMost</strong> colunas fixas, não mais do que <strong>JET_ccolVarMost</strong> colunas de comprimento variável e não mais do que <strong>JET_ccolTaggedMost</strong> colunas marcadas.</span><span class="sxs-lookup"><span data-stu-id="e0905-219">A table can have no more than <strong>JET_ccolFixedMost</strong> fixed columns, no more than <strong>JET_ccolVarMost</strong> variable-length columns, and no more than <strong>JET_ccolTaggedMost</strong> tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-220">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="e0905-220">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="e0905-221">Ocorreu um erro quando foi feita uma tentativa de normalizar uma coluna Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0905-221">An error occurred when an attempt was made to normalize a Unicode column.</span></span> <span data-ttu-id="e0905-222">Isso pode ser causado pela execução de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="e0905-222">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-223">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="e0905-223">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="e0905-224">Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</span><span class="sxs-lookup"><span data-stu-id="e0905-224">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e0905-225">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0905-225">Remarks</span></span>

<span data-ttu-id="e0905-226">A função **JetCreateTableColumnIndex4W** cria uma tabela com um conjunto inicial de colunas e índices.</span><span class="sxs-lookup"><span data-stu-id="e0905-226">The **JetCreateTableColumnIndex4W** function creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="e0905-227">Colunas e índices adicionais podem ser adicionados e removidos dinamicamente por meio das funções [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e0905-227">Additional columns and indexes can be added and removed dynamically by means of the [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md) functions.</span></span>

<span data-ttu-id="e0905-228">Assim como acontece com a função [JetOpenTable](./jetopentable-function.md) , quando o aplicativo é feito usando o *TableID* retornado, a função [JetCloseTable](./jetclosetable-function.md) deve fechar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0905-228">As with the [JetOpenTable](./jetopentable-function.md) function, when the application is done using the returned *tableid*, the [JetCloseTable](./jetclosetable-function.md) function should close the application.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e0905-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0905-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0905-230"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e0905-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0905-231">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e0905-231">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-232"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e0905-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0905-233">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e0905-233">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-234"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e0905-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0905-235">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e0905-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0905-236"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e0905-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e0905-237">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e0905-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0905-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e0905-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e0905-239">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e0905-239">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e0905-240">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0905-240">See also</span></span>

[<span data-ttu-id="e0905-241">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="e0905-241">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="e0905-242">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="e0905-242">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="e0905-243">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e0905-243">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e0905-244">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e0905-244">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e0905-245">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="e0905-245">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="e0905-246">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="e0905-246">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="e0905-247">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e0905-247">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e0905-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e0905-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e0905-249">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="e0905-249">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="e0905-250">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="e0905-250">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="e0905-251">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="e0905-251">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="e0905-252">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="e0905-252">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="e0905-253">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="e0905-253">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="e0905-254">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="e0905-254">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="e0905-255">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="e0905-255">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="e0905-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="e0905-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="e0905-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="e0905-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="e0905-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="e0905-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="e0905-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="e0905-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
