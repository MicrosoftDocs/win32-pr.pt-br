---
description: 'Saiba mais sobre: função JetCreateIndex4W'
title: Função JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762506"
---
# <a name="jetcreateindex4w-function"></a><span data-ttu-id="b571f-103">Função JetCreateIndex4W</span><span class="sxs-lookup"><span data-stu-id="b571f-103">JetCreateIndex4W Function</span></span>


<span data-ttu-id="b571f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b571f-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="b571f-105">A função **JetCreateIndex4W** cria índices em um banco de dados ESE (mecanismo de armazenamento extensível), que pode ser usado para localizar dados específicos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b571f-105">The **JetCreateIndex4W** function creates indexes over data in an Extensible Storage Engine (ESE) database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="b571f-106">A função **JetCreateIndex4W** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b571f-106">The **JetCreateIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a><span data-ttu-id="b571f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b571f-107">Parameters</span></span>

<span data-ttu-id="b571f-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b571f-108">*sesid*</span></span>

<span data-ttu-id="b571f-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="b571f-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="b571f-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b571f-110">*tableid*</span></span>

<span data-ttu-id="b571f-111">A tabela na qual o índice será criado.</span><span class="sxs-lookup"><span data-stu-id="b571f-111">The table on which the index will be created.</span></span>

<span data-ttu-id="b571f-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="b571f-112">*pindexcreate*</span></span>

<span data-ttu-id="b571f-113">Uma matriz de estruturas [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada uma delas define um índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b571f-113">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="b571f-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="b571f-114">*cIndexCreate*</span></span>

<span data-ttu-id="b571f-115">O número de elementos na matriz *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="b571f-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="b571f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b571f-116">Return value</span></span>

<span data-ttu-id="b571f-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b571f-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="b571f-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b571f-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b571f-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b571f-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="b571f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b571f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b571f-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b571f-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b571f-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b571f-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="b571f-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="b571f-124">Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</span><span class="sxs-lookup"><span data-stu-id="b571f-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="b571f-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="b571f-126">Foi feita uma tentativa de indexar uma coluna inexistente.</span><span class="sxs-lookup"><span data-stu-id="b571f-126">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="b571f-127">Uma tentativa de indexar condicionalmente uma coluna inexistente também pode produzir esse erro.</span><span class="sxs-lookup"><span data-stu-id="b571f-127">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="b571f-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="b571f-129">Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número inferior a 20 ou maior que 100.</span><span class="sxs-lookup"><span data-stu-id="b571f-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="b571f-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b571f-131">Foi feita uma tentativa de definir dois índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="b571f-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="b571f-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="b571f-133">Foi feita uma tentativa de especificar mais de um índice primário para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b571f-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="b571f-134">Uma tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="b571f-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="b571f-135">Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</span><span class="sxs-lookup"><span data-stu-id="b571f-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="b571f-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="b571f-137">Uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="b571f-137">An invalid index definition was specified.</span></span> <span data-ttu-id="b571f-138">Estes são alguns motivos possíveis para esse erro:</span><span class="sxs-lookup"><span data-stu-id="b571f-138">The following are some possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="b571f-139">Um índice primário é condicional (<strong>grbit</strong> membro de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem <strong>JET_bitIndexPrimary</strong> definido e o membro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</span><span class="sxs-lookup"><span data-stu-id="b571f-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="b571f-140">Aplica-se às versões do Windows a partir do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b571f-140">Applies to versions of Windows starting with Windows Server 2003.</span></span> <span data-ttu-id="b571f-141">Foi feita uma tentativa de criar um índice de tupla com limites de tupla, mas sem passar informações no membro <strong>ptuplelimits</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, <em>grbit</em> tem <strong>JET_bitIndexTupleLimits</strong> definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</span><span class="sxs-lookup"><span data-stu-id="b571f-141">An attempt was made to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has <strong>JET_bitIndexTupleLimits</strong> set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="b571f-142">Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="b571f-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="b571f-143">Para obter informações sobre definições válidas, consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="b571f-143">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="b571f-144">Definir o membro <strong>cbVarSegMac</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ser maior que <strong>JET_cbPrimaryKeyMost</strong> (para um índice primário) ou maior que <strong>JET_cbSecondaryKeyMost</strong> (para um índice secundário).</span><span class="sxs-lookup"><span data-stu-id="b571f-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than <strong>JET_cbPrimaryKeyMost</strong> (for a primary index) or greater than <strong>JET_cbSecondaryKeyMost</strong> (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="b571f-145">Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits <strong>JET_bitIndexUnicode</strong> no membro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="b571f-145">Passing an invalid combination for a user-defined Unicode index (one which has the <strong>JET_bitIndexUnicode</strong> bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="b571f-146">Algumas causas comuns podem ser que o campo pidxunicode da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é nulo ou o LCID especificado na estrutura pidxunicode é inválido.</span><span class="sxs-lookup"><span data-stu-id="b571f-146">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="b571f-147">Especificando uma coluna com valores de um índice primário.</span><span class="sxs-lookup"><span data-stu-id="b571f-147">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="b571f-148">Tentando indexar muitas colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="b571f-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="b571f-149">O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ser maior que <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="b571f-149">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="b571f-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="b571f-151">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b571f-151">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b571f-152">Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites.</span><span class="sxs-lookup"><span data-stu-id="b571f-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="b571f-153">Para obter mais informações, consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="b571f-153">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="b571f-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="b571f-155">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b571f-155">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b571f-156">Um índice de tupla não pode ser exclusivo (<em>grbit</em> não deve ter <strong>JET_bitIndexTuples</strong> e <strong>JET_bitIndexUnique</strong> definido).</span><span class="sxs-lookup"><span data-stu-id="b571f-156">A tuple index cannot be unique (<em>grbit</em> must not have both <strong>JET_bitIndexTuples</strong> and <strong>JET_bitIndexUnique</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="b571f-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="b571f-158">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b571f-158">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b571f-159">Um índice de tupla só pode ser em uma única coluna (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem <strong>JET_bitIndexTuples</strong> definido, e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica mais de uma coluna).</span><span class="sxs-lookup"><span data-stu-id="b571f-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexTuples</strong> set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="b571f-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="b571f-161">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b571f-161">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b571f-162">Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter <strong>JET_bitIndexPrimary</strong> e <strong>JET_bitIndexTuples</strong> definido).</span><span class="sxs-lookup"><span data-stu-id="b571f-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both <strong>JET_bitIndexPrimary</strong> and <strong>JET_bitIndexTuples</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="b571f-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="b571f-164">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b571f-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b571f-165">Um índice de tupla só pode estar em uma coluna de texto ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="b571f-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="b571f-166">Uma tentativa de indexar outras colunas (por exemplo, colunas binárias) resultará em <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span><span class="sxs-lookup"><span data-stu-id="b571f-166">An attempt to index other columns (for example, binary columns) will result in <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="b571f-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="b571f-168">Aplica-se às versões do Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b571f-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b571f-169">Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> seja definida.</span><span class="sxs-lookup"><span data-stu-id="b571f-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="b571f-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="b571f-171">Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</span><span class="sxs-lookup"><span data-stu-id="b571f-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="b571f-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="b571f-173">A definição de índice é inválida porque o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém valores inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="b571f-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="b571f-174">Estes são alguns motivos possíveis:</span><span class="sxs-lookup"><span data-stu-id="b571f-174">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="b571f-175">Um índice primário tinha um bit de ignorar especificado (JET_bitIndexPrimary foi passado com um dos <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>ou <strong>JET_bitIndexIgnoreFirstNull</strong>).</span><span class="sxs-lookup"><span data-stu-id="b571f-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>, or <strong>JET_bitIndexIgnoreFirstNull</strong>).</span></span></p></li>
<li><p><span data-ttu-id="b571f-176">Um índice vazio não ignora nenhum campo nulo (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem <strong>JET_bitIndexEmpty</strong> definido, mas não tem <strong>JET_bitIndexIgnoreAnyNull</strong> definido).</span><span class="sxs-lookup"><span data-stu-id="b571f-176">An empty index does not ignore any null fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexEmpty</strong> set, but does not have <strong>JET_bitIndexIgnoreAnyNull</strong> set).</span></span></p></li>
<li><p><span data-ttu-id="b571f-177">Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</span><span class="sxs-lookup"><span data-stu-id="b571f-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="b571f-178">Consulte <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="b571f-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="b571f-179">Ao criar vários índices de uma vez (ou seja, se o parâmetro <em>cIndexCreate</em> for maior que um), nenhum dos índices poderá conter qualquer um dos seguintes bits:</span><span class="sxs-lookup"><span data-stu-id="b571f-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="b571f-180"><strong>JET_bitIndexPrimary</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-180"><strong>JET_bitIndexPrimary</strong></span></span></p></li>
<li><p><span data-ttu-id="b571f-181"><strong>JET_bitIndexUnversioned</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-181"><strong>JET_bitIndexUnversioned</strong></span></span></p></li>
<li><p><span data-ttu-id="b571f-182"><strong>JET_bitIndexEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-182"><strong>JET_bitIndexEmpty</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="b571f-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="b571f-184">Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> na estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que o membro <strong>pidxunicode</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém um ponteiro para, ou por meio do membro <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="b571f-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="b571f-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="b571f-186">Um nome de índice inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="b571f-186">An invalid index name was specified.</span></span> <span data-ttu-id="b571f-187">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="b571f-187">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b571f-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b571f-189">Um parâmetro inválido foi passado para a API.</span><span class="sxs-lookup"><span data-stu-id="b571f-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="b571f-190">A seguir estão alguns motivos pelos quais esse erro pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="b571f-190">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="b571f-191">O campo <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b571f-191">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="b571f-192">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="b571f-192">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof(JET_INDEXCREATE2).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="b571f-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="b571f-194">Ocorreu um erro ao tentar normalizar uma coluna Unicode.</span><span class="sxs-lookup"><span data-stu-id="b571f-194">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="b571f-195">Isso pode ser causado pela execução de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="b571f-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-196">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="b571f-196">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="b571f-197">Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</span><span class="sxs-lookup"><span data-stu-id="b571f-197">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b571f-198">Comentários</span><span class="sxs-lookup"><span data-stu-id="b571f-198">Remarks</span></span>

<span data-ttu-id="b571f-199">A função **JetCreateIndex4W** itera através dos índices fornecidos no parâmetro *pindexcreate* e, às vezes, é anulada na primeira falha.</span><span class="sxs-lookup"><span data-stu-id="b571f-199">The **JetCreateIndex4W** function iterates through the indexes given in the *pindexcreate* parameter, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="b571f-200">Todos os índices após o primeiro índice com um erro podem não ter sido tentados, mesmo que o membro **Err** da estrutura de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contenha JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="b571f-200">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b571f-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b571f-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b571f-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b571f-203">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b571f-203">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-204"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b571f-205">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b571f-205">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-206"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b571f-207">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b571f-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b571f-208"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b571f-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b571f-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b571f-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b571f-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b571f-211">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b571f-211">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b571f-212">Confira também</span><span class="sxs-lookup"><span data-stu-id="b571f-212">See also</span></span>

[<span data-ttu-id="b571f-213">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="b571f-213">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="b571f-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b571f-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b571f-215">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b571f-215">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b571f-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b571f-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b571f-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b571f-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b571f-218">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="b571f-218">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="b571f-219">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="b571f-219">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="b571f-220">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="b571f-220">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="b571f-221">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="b571f-221">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="b571f-222">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="b571f-222">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
