---
description: 'Saiba mais sobre: função JetCreateIndex2'
title: Função JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793401"
---
# <a name="jetcreateindex2-function"></a><span data-ttu-id="65430-103">Função JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="65430-103">JetCreateIndex2 Function</span></span>


<span data-ttu-id="65430-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="65430-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex2-function"></a><span data-ttu-id="65430-105">Função JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="65430-105">JetCreateIndex2 Function</span></span>

<span data-ttu-id="65430-106">A função **JetCreateIndex2** cria índices em um banco de dados ESE, que pode ser usado para localizar dados específicos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="65430-106">The **JetCreateIndex2** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="65430-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65430-107">Parameters</span></span>

<span data-ttu-id="65430-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="65430-108">*sesid*</span></span>

<span data-ttu-id="65430-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="65430-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="65430-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="65430-110">*tableid*</span></span>

<span data-ttu-id="65430-111">A tabela na qual o índice será criado.</span><span class="sxs-lookup"><span data-stu-id="65430-111">The table on which the index will be created.</span></span>

<span data-ttu-id="65430-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="65430-112">*pindexcreate*</span></span>

<span data-ttu-id="65430-113">Uma matriz de estruturas [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada uma delas define um índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="65430-113">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="65430-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="65430-114">*cIndexCreate*</span></span>

<span data-ttu-id="65430-115">O número de elementos na matriz *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="65430-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="65430-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="65430-116">Return Value</span></span>

<span data-ttu-id="65430-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="65430-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="65430-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="65430-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65430-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="65430-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="65430-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="65430-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65430-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="65430-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="65430-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="65430-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="65430-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="65430-124">Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</span><span class="sxs-lookup"><span data-stu-id="65430-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="65430-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="65430-126">Foi feita uma tentativa de indexar uma coluna não existente.</span><span class="sxs-lookup"><span data-stu-id="65430-126">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="65430-127">A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</span><span class="sxs-lookup"><span data-stu-id="65430-127">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="65430-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="65430-129">Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for definido como um número inferior a 20 ou maior que 100.</span><span class="sxs-lookup"><span data-stu-id="65430-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="65430-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="65430-131">Foi feita uma tentativa de definir dois índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="65430-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="65430-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="65430-133">Foi feita uma tentativa de especificar mais de um índice primário para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="65430-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="65430-134">Uma tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="65430-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="65430-135">Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</span><span class="sxs-lookup"><span data-stu-id="65430-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="65430-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="65430-137">Uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="65430-137">An invalid index definition was specified.</span></span> <span data-ttu-id="65430-138">Alguns dos motivos possíveis para receber esse erro são:</span><span class="sxs-lookup"><span data-stu-id="65430-138">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="65430-139">Um índice primário é condicional (<strong>grbit</strong> membro de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é maior que zero).</span><span class="sxs-lookup"><span data-stu-id="65430-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="65430-140">Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="65430-140">Windows Server 2003 and later.</span></span> <span data-ttu-id="65430-141">Tentativa de criar um índice de tupla com limites de tupla, mas sem passar informações no membro <strong>ptuplelimits</strong> em <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ou seja, <em>grbit</em> tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</span><span class="sxs-lookup"><span data-stu-id="65430-141">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="65430-142">Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="65430-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="65430-143">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma discussão sobre definições válidas.</span><span class="sxs-lookup"><span data-stu-id="65430-143">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="65430-144">Definir o membro <strong>cbVarSegMac</strong> em <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</span><span class="sxs-lookup"><span data-stu-id="65430-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="65430-145">Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="65430-145">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="65430-146">Algumas causas comuns podem ser que o campo pidxunicode da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é nulo ou o LCID especificado na estrutura pidxunicode é inválido.</span><span class="sxs-lookup"><span data-stu-id="65430-146">Some common causes may be that the pidxunicode field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="65430-147">Especificando uma coluna com valores múltiplos para um índice primário.</span><span class="sxs-lookup"><span data-stu-id="65430-147">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="65430-148">Tentando indexar muitas colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="65430-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="65430-149">O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ser maior que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="65430-149">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="65430-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="65430-151">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="65430-151">Windows XP and later.</span></span> <span data-ttu-id="65430-152">Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites.</span><span class="sxs-lookup"><span data-stu-id="65430-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="65430-153">Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="65430-153">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="65430-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="65430-155">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="65430-155">Windows XP and later.</span></span> <span data-ttu-id="65430-156">Um índice de tupla não pode ser exclusivo (<em>grbit</em> não deve ter JET_bitIndexTuples e JET_bitIndexUnique definido).</span><span class="sxs-lookup"><span data-stu-id="65430-156">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="65430-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="65430-158">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="65430-158">Windows XP and later.</span></span> <span data-ttu-id="65430-159">Um índice de tupla só pode ser em uma única coluna (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexTuples definido, e o membro <strong>szKey</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica mais de uma coluna).</span><span class="sxs-lookup"><span data-stu-id="65430-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="65430-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="65430-161">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="65430-161">Windows XP and later.</span></span> <span data-ttu-id="65430-162">Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</span><span class="sxs-lookup"><span data-stu-id="65430-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="65430-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="65430-164">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="65430-164">Windows XP and later.</span></span> <span data-ttu-id="65430-165">Um índice de tupla só pode estar em uma coluna de texto ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="65430-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="65430-166">Uma tentativa de indexar outras colunas (por exemplo, colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="65430-166">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="65430-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="65430-168">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="65430-168">Windows XP and later.</span></span> <span data-ttu-id="65430-169">Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> seja definida.</span><span class="sxs-lookup"><span data-stu-id="65430-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="65430-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="65430-171">Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</span><span class="sxs-lookup"><span data-stu-id="65430-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="65430-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="65430-173">A definição de índice é inválida porque o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contém valores inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="65430-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains inconsistent values.</span></span> <span data-ttu-id="65430-174">Alguns motivos possíveis são:</span><span class="sxs-lookup"><span data-stu-id="65430-174">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="65430-175">Um índice primário tinha um bit de ignorar especificado (JET_bitIndexPrimary foi passado com um dos JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="65430-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="65430-176">Um índice vazio não ignora nenhum campo nulo (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</span><span class="sxs-lookup"><span data-stu-id="65430-176">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="65430-177">Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</span><span class="sxs-lookup"><span data-stu-id="65430-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="65430-178">Consulte <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="65430-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="65430-179">Ao criar vários índices de uma vez (ou seja, se o parâmetro <em>cIndexCreate</em> for maior que um), nenhum dos índices poderá conter qualquer um dos seguintes bits:</span><span class="sxs-lookup"><span data-stu-id="65430-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="65430-180">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="65430-180">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="65430-181">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="65430-181">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="65430-182">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="65430-182">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="65430-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="65430-184">Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> na estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que o membro <strong>pidxunicode</strong> na estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contém um ponteiro para, ou por meio do membro <strong>LCID</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="65430-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="65430-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="65430-186">Um nome de índice inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="65430-186">An invalid index name was specified.</span></span> <span data-ttu-id="65430-187">Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="65430-187">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="65430-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="65430-189">Um parâmetro inválido foi passado para a API.</span><span class="sxs-lookup"><span data-stu-id="65430-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="65430-190">Alguns dos motivos pelos quais esse erro pode ser retornado são:</span><span class="sxs-lookup"><span data-stu-id="65430-190">Some of the reasons this error may be returned are:</span></span></p>
<ul>
<li><p><span data-ttu-id="65430-191">O campo <strong>cbKey</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="65430-191">The <strong>cbKey</strong> field of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="65430-192">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não está definido como sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="65430-192">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="65430-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="65430-194">Ocorreu um erro ao tentar normalizar uma coluna Unicode.</span><span class="sxs-lookup"><span data-stu-id="65430-194">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="65430-195">Isso pode ser causado pela execução de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="65430-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="65430-196">Comentários</span><span class="sxs-lookup"><span data-stu-id="65430-196">Remarks</span></span>

<span data-ttu-id="65430-197">O valor de retorno é JET_errSuccess na conclusão bem-sucedida de todos os índices especificados.</span><span class="sxs-lookup"><span data-stu-id="65430-197">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="65430-198">**JetCreateIndex2** faz a iteração pelos índices fornecidos em **pindexcreate** e, às vezes, anulará na primeira falha.</span><span class="sxs-lookup"><span data-stu-id="65430-198">**JetCreateIndex2** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="65430-199">Todos os índices após o primeiro índice com um erro podem não ter sido tentados, mesmo que o membro **Err** da estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) contenha JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="65430-199">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="65430-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65430-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65430-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="65430-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="65430-202">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="65430-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-203"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="65430-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="65430-204">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="65430-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-205"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="65430-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="65430-206">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="65430-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-207"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="65430-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="65430-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="65430-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65430-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="65430-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="65430-210">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="65430-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65430-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="65430-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="65430-212">Implementado como <strong>JetCreateIndex2W</strong> (Unicode) e <strong>JetCreateIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="65430-212">Implemented as <strong>JetCreateIndex2W</strong> (Unicode) and <strong>JetCreateIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="65430-213">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="65430-213">See Also</span></span>

[<span data-ttu-id="65430-214">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="65430-214">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="65430-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="65430-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="65430-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="65430-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="65430-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="65430-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="65430-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="65430-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="65430-219">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="65430-219">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="65430-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="65430-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="65430-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="65430-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="65430-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="65430-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
