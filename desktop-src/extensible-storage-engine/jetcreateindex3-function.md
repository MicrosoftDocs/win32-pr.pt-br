---
description: 'Saiba mais sobre: função JetCreateIndex3'
title: Função JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297042"
---
# <a name="jetcreateindex3-function"></a><span data-ttu-id="3b2fc-103">Função JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="3b2fc-103">JetCreateIndex3 Function</span></span>


<span data-ttu-id="3b2fc-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b2fc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex3-function"></a><span data-ttu-id="3b2fc-105">Função JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="3b2fc-105">JetCreateIndex3 Function</span></span>

<span data-ttu-id="3b2fc-106">A função **JetCreateIndex3** cria índices em um banco de dados ESE, que pode ser usado para localizar dados específicos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-106">The **JetCreateIndex3** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="3b2fc-107">**Windows 7: o JetCreateIndex3** é introduzido no sistema operacional Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-107">**Windows 7:  JetCreateIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="3b2fc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b2fc-108">Parameters</span></span>

<span data-ttu-id="3b2fc-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3b2fc-109">*sesid*</span></span>

<span data-ttu-id="3b2fc-110">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="3b2fc-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="3b2fc-111">*tableid*</span></span>

<span data-ttu-id="3b2fc-112">A tabela na qual o índice será criado.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-112">The table on which the index will be created.</span></span>

<span data-ttu-id="3b2fc-113">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="3b2fc-113">*pindexcreate*</span></span>

<span data-ttu-id="3b2fc-114">Uma matriz de estruturas [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada uma delas define um índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-114">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="3b2fc-115">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="3b2fc-115">*cIndexCreate*</span></span>

<span data-ttu-id="3b2fc-116">O número de elementos na matriz *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="3b2fc-116">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="3b2fc-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3b2fc-117">Return Value</span></span>

<span data-ttu-id="3b2fc-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-118">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="3b2fc-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b2fc-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b2fc-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b2fc-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b2fc-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b2fc-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-124">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="3b2fc-124">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-125">Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-125">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-126">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="3b2fc-126">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-127">Foi feita uma tentativa de indexar uma coluna não existente.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-127">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="3b2fc-128">A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-128">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-129">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="3b2fc-129">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-130">Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número inferior a 20 ou maior que 100.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-130">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-131">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="3b2fc-131">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-132">Foi feita uma tentativa de definir dois índices idênticos.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-132">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-133">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="3b2fc-133">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-134">Foi feita uma tentativa de especificar mais de um índice primário para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-134">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="3b2fc-135">Uma tabela deve ter exatamente um índice primário.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-135">A table must have exactly one primary index.</span></span> <span data-ttu-id="3b2fc-136">Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-136">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-137">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="3b2fc-137">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-138">Uma definição de índice inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-138">An invalid index definition was specified.</span></span> <span data-ttu-id="3b2fc-139">Estes são alguns motivos possíveis para receber esse erro:</span><span class="sxs-lookup"><span data-stu-id="3b2fc-139">The following are some possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b2fc-140">Um índice primário é condicional (<strong>grbit</strong> membro de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-140">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-141">Windows Server 2003 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-141">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="3b2fc-142">Tentativa de criar um índice de tupla com limites de tupla, mas sem passar informações no membro <strong>ptuplelimits</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, <em>grbit</em> tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-142">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-143">Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="3b2fc-143">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="3b2fc-144">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter uma discussão sobre definições válidas.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-144">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-145">Definir o membro <strong>cbVarSegMac</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-145">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-146">Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-146">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="3b2fc-147">Algumas causas comuns podem ser que o campo pidxunicode da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é nulo ou o LCID especificado na estrutura pidxunicode é inválido.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-147">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-148">Especificando uma coluna com valores múltiplos para um índice primário.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-148">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-149">Tentando indexar muitas colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-149">Trying to index too many conditional columns.</span></span> <span data-ttu-id="3b2fc-150">O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ser maior que JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-150">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-151">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="3b2fc-151">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-152">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-152">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="3b2fc-153">Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-153">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="3b2fc-154">Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="3b2fc-154">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-155">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="3b2fc-155">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-156">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-156">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="3b2fc-157">Um índice de tupla não pode ser exclusivo (<em>grbit</em> não deve ter JET_bitIndexTuples e JET_bitIndexUnique definido).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-157">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-158">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="3b2fc-158">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-159">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-159">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="3b2fc-160">Um índice de tupla só pode ser em uma única coluna (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexTuples definido, e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica mais de uma coluna).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-160">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-161">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="3b2fc-161">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-162">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-162">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="3b2fc-163">Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-163">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-164">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="3b2fc-164">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-165">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="3b2fc-166">Um índice de tupla só pode estar em uma coluna de texto ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-166">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="3b2fc-167">Uma tentativa de indexar outras colunas (por exemplo, colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-167">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-168">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="3b2fc-168">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-169">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="3b2fc-170">Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> seja definida.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-170">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-171">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="3b2fc-171">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-172">Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-172">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-173">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="3b2fc-173">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-174">A definição de índice é inválida porque o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém valores inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-174">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="3b2fc-175">Estes são alguns motivos possíveis:</span><span class="sxs-lookup"><span data-stu-id="3b2fc-175">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b2fc-176">Um índice primário tinha um bit de ignorar especificado (JET_bitIndexPrimary foi passado com um dos JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-176">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-177">Um índice vazio não ignora nenhum campo nulo (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-177">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-178">Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-178">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="3b2fc-179">Consulte <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-179">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="3b2fc-180">Ao criar vários índices de uma vez (ou seja, se o parâmetro <em>cIndexCreate</em> for maior que um), nenhum dos índices poderá conter qualquer um dos seguintes bits:</span><span class="sxs-lookup"><span data-stu-id="3b2fc-180">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b2fc-181">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="3b2fc-181">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-182">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="3b2fc-182">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-183">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="3b2fc-183">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-184">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="3b2fc-184">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-185">Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> na estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que o membro <strong>pidxunicode</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém um ponteiro para, ou por meio do membro <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-185">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-186">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="3b2fc-186">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-187">Um nome de índice inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-187">An invalid index name was specified.</span></span> <span data-ttu-id="3b2fc-188">Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-188">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-189">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3b2fc-189">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-190">Um parâmetro inválido foi passado para a API.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-190">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="3b2fc-191">A seguir estão alguns motivos pelos quais esse erro pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="3b2fc-191">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b2fc-192">O campo <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-192">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="3b2fc-193">O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-193">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-194">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="3b2fc-194">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-195">Ocorreu um erro ao tentar normalizar uma coluna Unicode.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-195">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="3b2fc-196">Isso pode ser causado pela execução de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-196">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-197">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="3b2fc-197">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="3b2fc-198">Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-198">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="3b2fc-199">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b2fc-199">Remarks</span></span>

<span data-ttu-id="3b2fc-200">O valor de retorno é JET_errSuccess na conclusão bem-sucedida de todos os índices especificados.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-200">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="3b2fc-201">**JetCreateIndex3** faz a iteração pelos índices fornecidos em **pindexcreate** e, às vezes, anulará na primeira falha.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-201">**JetCreateIndex3** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="3b2fc-202">Todos os índices após o primeiro índice com um erro podem não ter sido tentados, mesmo que o membro **Err** da estrutura de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contenha JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-202">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b2fc-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b2fc-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-204"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fc-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fc-205">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-206"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fc-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fc-207">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-208"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fc-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fc-209">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-210"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fc-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fc-211">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2fc-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fc-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fc-213">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b2fc-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2fc-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3b2fc-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3b2fc-215">Implementado como <strong>JetCreateIndex3W</strong> (Unicode) e <strong>JetCreateIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3b2fc-215">Implemented as <strong>JetCreateIndex3W</strong> (Unicode) and <strong>JetCreateIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b2fc-216">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3b2fc-216">See Also</span></span>

[<span data-ttu-id="3b2fc-217">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="3b2fc-217">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="3b2fc-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b2fc-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b2fc-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3b2fc-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3b2fc-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3b2fc-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3b2fc-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3b2fc-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3b2fc-222">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="3b2fc-222">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="3b2fc-223">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="3b2fc-223">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="3b2fc-224">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="3b2fc-224">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="3b2fc-225">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="3b2fc-225">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="3b2fc-226">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="3b2fc-226">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
