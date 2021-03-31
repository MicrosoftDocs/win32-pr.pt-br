---
description: 'Saiba mais sobre: função JetSetColumns'
title: Função JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089876"
---
# <a name="jetsetcolumns-function"></a><span data-ttu-id="c0983-103">Função JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="c0983-103">JetSetColumns Function</span></span>


<span data-ttu-id="c0983-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c0983-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumns-function"></a><span data-ttu-id="c0983-105">Função JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="c0983-105">JetSetColumns Function</span></span>

<span data-ttu-id="c0983-106">A função **JetSetColumns** é semelhante ao comportamento de [JetSetColumn](./jetsetcolumn-function.md) , mas permite que um aplicativo defina vários valores de coluna em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="c0983-106">The **JetSetColumns** function is similar in behavior to [JetSetColumn](./jetsetcolumn-function.md) but allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="c0983-107">Uma matriz de estruturas de [JET_SETCOLUMN](./jet-setcolumn-structure.md) é usada para descrever o conjunto de valores de coluna a ser definido e para descrever os buffers de entrada para cada valor de coluna a ser definido.</span><span class="sxs-lookup"><span data-stu-id="c0983-107">An array of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="c0983-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0983-108">Parameters</span></span>

<span data-ttu-id="c0983-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c0983-109">*sesid*</span></span>

<span data-ttu-id="c0983-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="c0983-110">The session to use for this call.</span></span>

<span data-ttu-id="c0983-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c0983-111">*tableid*</span></span>

<span data-ttu-id="c0983-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="c0983-112">The cursor to use for this call.</span></span>

<span data-ttu-id="c0983-113">*psetcolumn*</span><span class="sxs-lookup"><span data-stu-id="c0983-113">*psetcolumn*</span></span>

<span data-ttu-id="c0983-114">Um ponteiro para uma matriz de uma ou mais estruturas de [JET_SETCOLUMN](./jet-setcolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c0983-114">A pointer to an array of one or more [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures.</span></span> <span data-ttu-id="c0983-115">Cada estrutura inclui descrições de qual valor de coluna definir e de onde obter dados de coluna a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="c0983-115">Each structure includes descriptions of which column value to set and from where to get column data to set.</span></span>

<span data-ttu-id="c0983-116">*csetcolumn*</span><span class="sxs-lookup"><span data-stu-id="c0983-116">*csetcolumn*</span></span>

<span data-ttu-id="c0983-117">O número de estruturas de [JET_SETCOLUMN](./jet-setcolumn-structure.md) na matriz fornecida por *psetcolumn*.</span><span class="sxs-lookup"><span data-stu-id="c0983-117">The number of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures in the array given by *psetcolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="c0983-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c0983-118">Return Value</span></span>

<span data-ttu-id="c0983-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0983-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c0983-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c0983-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0983-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c0983-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="c0983-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0983-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0983-123">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="c0983-123">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="c0983-124">A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="c0983-124">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c0983-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c0983-126">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c0983-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-127">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="c0983-127">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="c0983-128">O mesmo que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="c0983-128">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-129">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="c0983-129">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="c0983-130">A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="c0983-130">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-131">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="c0983-131">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="c0983-132">Foi feita uma tentativa ilegal de atualizar um valor longo durante uma operação de exclusão de atualização original de cópia de inserção.</span><span class="sxs-lookup"><span data-stu-id="c0983-132">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-133">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="c0983-133">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="c0983-134">Os dados de valor de coluna fornecidos no buffer de entrada excedem a limitação de tamanho natural para uma coluna de comprimento fixo ou configurados para texto de comprimento fixo ou colunas binárias.</span><span class="sxs-lookup"><span data-stu-id="c0983-134">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="c0983-135">Esse erro também é retornado ao passar mais de 1024 bytes de dados para uma coluna longa e definir o sinalizador de JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="c0983-135">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c0983-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c0983-137">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="c0983-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c0983-138">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="c0983-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="c0983-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="c0983-140">O tamanho de dados do valor da coluna fornecido não corresponde ao que é natural para o tipo de dados de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="c0983-140">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-141">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="c0983-141">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="c0983-142">Foi feita uma tentativa ilegal de atualizar uma coluna de incremento automático durante uma operação de inserção ou atualização, ou para atualizar uma coluna de versão durante uma operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="c0983-142">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-143">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="c0983-143">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="c0983-144">As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bit conhecido.</span><span class="sxs-lookup"><span data-stu-id="c0983-144">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c0983-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c0983-146">O psetinfo- &gt; cbStruct fornecido não é um tamanho válido para a estrutura de <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="c0983-146">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-147">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="c0983-147">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="c0983-148">A operação definir coluna tentou criar um valor duplicado e especificou JET_bitSetUniqueMultiValues ou JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="c0983-148">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-149">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c0983-149">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c0983-150">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="c0983-150">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-151">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="c0983-151">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="c0983-152">Foi feita uma tentativa ilegal de atualizar um valor de coluna longo quando a sessão de chamada não estava em uma transação.</span><span class="sxs-lookup"><span data-stu-id="c0983-152">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-153">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="c0983-153">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="c0983-154">Foi feita uma tentativa ilegal de definir uma coluna não nula como nula.</span><span class="sxs-lookup"><span data-stu-id="c0983-154">An illegal attempt was made to set a non-NULL column to NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-155">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="c0983-155">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="c0983-156">O valor da coluna não pôde ser definido como o valor no buffer de entrada porque ele teria feito com que o registro excedesse sua limitação de tamanho relacionada ao tamanho da página.</span><span class="sxs-lookup"><span data-stu-id="c0983-156">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="c0983-157">As colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> podem ser armazenadas separadamente dos dados de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="c0983-157">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="c0983-158">No entanto, outras colunas devem ser armazenadas com o registro e podem fazer com que a limitação do tamanho do registro seja excedida.</span><span class="sxs-lookup"><span data-stu-id="c0983-158">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="c0983-159">Colunas longas exigem 5 bytes de espaço dentro do registro como uma ligação e isso também pode levar a JET_errRecordTooBig retornando.</span><span class="sxs-lookup"><span data-stu-id="c0983-159">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c0983-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c0983-161">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="c0983-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c0983-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c0983-163">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c0983-163">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c0983-164">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="c0983-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c0983-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c0983-166">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="c0983-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-167">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="c0983-167">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="c0983-168">O cursor não está atualmente no processo de inserir um novo registro ou atualizar um registro existente.</span><span class="sxs-lookup"><span data-stu-id="c0983-168">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="c0983-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="c0983-170">O valor da coluna no buffer de entrada excedeu o comprimento máximo configurado para uma coluna de comprimento variável e foi truncado.</span><span class="sxs-lookup"><span data-stu-id="c0983-170">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0983-171">Em caso de sucesso, para cada coluna descrita no psetcolumns, a parte desejada do valor da coluna é definida com os dados copiados do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0983-171">On success, for each column described in the psetcolumns, the desired portion of the column value is set with data copied from the input buffer.</span></span> <span data-ttu-id="c0983-172">O conjunto de dados de coluna pode ter sido truncado se excedeu o comprimento máximo especificado para uma coluna de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="c0983-172">The column data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="c0983-173">Em caso de falha, o local do cursor permanece inalterado e nenhum dado do valor da coluna é atualizado no buffer de cópia.</span><span class="sxs-lookup"><span data-stu-id="c0983-173">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c0983-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0983-174">Remarks</span></span>

<span data-ttu-id="c0983-175">Se qualquer operação de conjunto de colunas individuais retornar um erro, a operação **JetSetColumns** inteira retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c0983-175">If any individual set column operation returns an error then the whole **JetSetColumns** operation will return an error.</span></span> <span data-ttu-id="c0983-176">Os avisos, em geral, são retornados em psetcolumns- \> Error e não no código de retorno dessa função.</span><span class="sxs-lookup"><span data-stu-id="c0983-176">Warnings, in general, are returned in the psetcolumns-\>error and not in the return code from this function.</span></span> <span data-ttu-id="c0983-177">No entanto, se o último conjunto de colunas tiver um aviso, esse aviso será retornado do **JetSetColumns** em si.</span><span class="sxs-lookup"><span data-stu-id="c0983-177">However, if the last column set has a warning, then this warning will be returned from **JetSetColumns** itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c0983-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0983-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0983-179"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c0983-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c0983-180">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c0983-180">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-181"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c0983-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c0983-182">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c0983-182">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-183"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c0983-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c0983-184">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c0983-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0983-185"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="c0983-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c0983-186">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c0983-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0983-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c0983-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c0983-188">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c0983-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c0983-189">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c0983-189">See Also</span></span>

[<span data-ttu-id="c0983-190">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="c0983-190">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="c0983-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c0983-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c0983-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c0983-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c0983-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c0983-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c0983-194">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c0983-194">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="c0983-195">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="c0983-195">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="c0983-196">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="c0983-196">JetSetColumn</span></span>](./jetsetcolumn-function.md)
