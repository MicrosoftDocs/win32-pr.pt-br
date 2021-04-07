---
description: 'Saiba mais sobre: função JetUpdate'
title: Função JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827276"
---
# <a name="jetupdate-function"></a><span data-ttu-id="09cda-103">Função JetUpdate</span><span class="sxs-lookup"><span data-stu-id="09cda-103">JetUpdate Function</span></span>


<span data-ttu-id="09cda-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="09cda-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate-function"></a><span data-ttu-id="09cda-105">Função JetUpdate</span><span class="sxs-lookup"><span data-stu-id="09cda-105">JetUpdate Function</span></span>

<span data-ttu-id="09cda-106">A função **JetUpdate** executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="09cda-106">The **JetUpdate** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="09cda-107">A exclusão de uma linha de tabela é executada chamando [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="09cda-107">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="09cda-108">**JetUpdate** é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="09cda-108">**JetUpdate** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="09cda-109">A atualização é iniciada chamando [JetPrepareUpdate](./jetprepareupdate-function.md) e, em seguida, chamando [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="09cda-109">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="09cda-110">Por fim, **JetUpdate** é chamado para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="09cda-110">Finally, **JetUpdate** is called to complete the update operation.</span></span> <span data-ttu-id="09cda-111">Os índices são atualizados somente por **JetUpdate** ou [JetUpdate2](./jetupdate2-function.md), e não durante [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="09cda-111">Indexes are updated only by **JetUpdate** or [JetUpdate2](./jetupdate2-function.md), and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="09cda-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09cda-112">Parameters</span></span>

<span data-ttu-id="09cda-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="09cda-113">*sesid*</span></span>

<span data-ttu-id="09cda-114">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="09cda-114">The session to use for this call.</span></span>

<span data-ttu-id="09cda-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="09cda-115">*tableid*</span></span>

<span data-ttu-id="09cda-116">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="09cda-116">The cursor to use for this call.</span></span>

<span data-ttu-id="09cda-117">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="09cda-117">*pvBookmark*</span></span>

<span data-ttu-id="09cda-118">Ponteiro para um indicador retornado para uma linha inserida.</span><span class="sxs-lookup"><span data-stu-id="09cda-118">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="09cda-119">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="09cda-119">*cbBookmark*</span></span>

<span data-ttu-id="09cda-120">Tamanho do buffer apontado por *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="09cda-120">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="09cda-121">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="09cda-121">*pcbActual*</span></span>

<span data-ttu-id="09cda-122">O tamanho retornado do indicador para a linha inserida retornada em *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="09cda-122">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

### <a name="return-value"></a><span data-ttu-id="09cda-123">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="09cda-123">Return Value</span></span>

<span data-ttu-id="09cda-124">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="09cda-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="09cda-125">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="09cda-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09cda-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="09cda-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="09cda-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="09cda-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09cda-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="09cda-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="09cda-129">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="09cda-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-130">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="09cda-130">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="09cda-131">O buffer fornecido para o indicador de registro não é suficientemente grande o suficiente para armazenar o indicador de registro.</span><span class="sxs-lookup"><span data-stu-id="09cda-131">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="09cda-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="09cda-133">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="09cda-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-134">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="09cda-134">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="09cda-135">O mesmo que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="09cda-135">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-136">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="09cda-136">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="09cda-137">A operação de atualização requer o crescimento do arquivo de banco de dados ou a alocação do arquivo de log, mas a unidade de disco em que reside o arquivo de banco de dados ou a série de logs está cheia.</span><span class="sxs-lookup"><span data-stu-id="09cda-137">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="09cda-138">Como alternativa, o arquivo de banco de dados está em um volume formatado em FAT32 e o arquivo de banco de dados já está 4GBytes, o limite por arquivo para FAT32.</span><span class="sxs-lookup"><span data-stu-id="09cda-138">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="09cda-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="09cda-140">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="09cda-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="09cda-141"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="09cda-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="09cda-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="09cda-143">O parâmetro <em>Prep</em> fornecido na função <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> não é um sinalizador válido.</span><span class="sxs-lookup"><span data-stu-id="09cda-143">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-144">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="09cda-144">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="09cda-145">Uma chave de índice para este registro é uma duplicata de outra chave de índice para outro registro que já está na tabela e o índice não permite duplicatas.</span><span class="sxs-lookup"><span data-stu-id="09cda-145">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-146">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="09cda-146">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="09cda-147">O registro inserido ou atualizado tem um ou mais índices para os quais a chave gerada teria excedido o tamanho máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="09cda-147">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="09cda-148">Como resultado, a operação falhou ao impedir o truncamento de chave.</span><span class="sxs-lookup"><span data-stu-id="09cda-148">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-149">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="09cda-149">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="09cda-150">O registro inserido ou atualizado tem uma coluna de vários valores indexada com dois ou mais valores que são idênticos no tamanho de chave de comprimento máximo definido para o índice.</span><span class="sxs-lookup"><span data-stu-id="09cda-150">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="09cda-151">Como resultado, o registro tem duas entradas idênticas no índice que são inválidas.</span><span class="sxs-lookup"><span data-stu-id="09cda-151">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="09cda-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="09cda-153">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="09cda-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-154">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="09cda-154">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="09cda-155">Uma ou mais colunas no registro a serem inseridas ou no estado atualizado de um registro que está sendo substituído são <strong>nulas</strong> , o que viola a restrição definida para essas colunas.</span><span class="sxs-lookup"><span data-stu-id="09cda-155">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-156">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="09cda-156">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="09cda-157">Um ou mais índices estão definidos para não permitir uma chave <strong>nula</strong> e o estado inserido ou atualizado de um registro que está sendo substituído viola essa restrição definida.</span><span class="sxs-lookup"><span data-stu-id="09cda-157">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-158">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="09cda-158">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="09cda-159">Uma operação de substituição de registro atualizou a chave primária.</span><span class="sxs-lookup"><span data-stu-id="09cda-159">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="09cda-160">As atualizações nas colunas de chave primária devem ser feitas por meio da exclusão do registro existente e da inserção de um novo registro com os dados desejados.</span><span class="sxs-lookup"><span data-stu-id="09cda-160">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="09cda-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="09cda-162">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="09cda-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="09cda-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="09cda-164">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="09cda-164">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="09cda-165"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="09cda-165"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="09cda-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="09cda-167">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="09cda-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-168">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="09cda-168">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="09cda-169">É ilegal tentar uma atualização quando dentro do escopo de uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09cda-169">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="09cda-170">Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="09cda-170">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="09cda-171"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="09cda-171"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-172">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="09cda-172">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="09cda-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> foi chamado com JET_prepCancel, mas o cursor não estava no estado preparado.</span><span class="sxs-lookup"><span data-stu-id="09cda-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-174">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="09cda-174">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="09cda-175">A operação falhou porque não há memória suficiente para reter informações transacionais sobre a atualização.</span><span class="sxs-lookup"><span data-stu-id="09cda-175">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-176">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="09cda-176">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="09cda-177">Outra sessão bloqueou anteriormente o registro para atualização.</span><span class="sxs-lookup"><span data-stu-id="09cda-177">Another session has previously locked the record for update.</span></span> <span data-ttu-id="09cda-178">A atualização tentada por esta sessão falhará.</span><span class="sxs-lookup"><span data-stu-id="09cda-178">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09cda-179">Em caso de sucesso, a operação abrir atualização no cursor é concluída.</span><span class="sxs-lookup"><span data-stu-id="09cda-179">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="09cda-180">Se uma coluna de incremento automático for definida para a tabela, esse valor será definido para registros inseridos.</span><span class="sxs-lookup"><span data-stu-id="09cda-180">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="09cda-181">Se uma coluna de versão for definida para a tabela, seu valor será inicializado para registros recentemente inseridos ou incrementado cada vez que um registro for substituído.</span><span class="sxs-lookup"><span data-stu-id="09cda-181">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="09cda-182">Todos os índices, incluindo índices clusterizados e não clusterizados, são atualizados.</span><span class="sxs-lookup"><span data-stu-id="09cda-182">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="09cda-183">Em caso de falha, nenhuma alteração de qualquer tipo é feita no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="09cda-183">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="09cda-184">Antes de INSERT e before, as funções REPLACE de retorno de chamada podem ter sido chamadas, mas após INSERT e After Replace não serão chamadas, já que o último não pode fazer com que uma atualização falhe.</span><span class="sxs-lookup"><span data-stu-id="09cda-184">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="09cda-185">O buffer de cópia do cursor é deixado em seu estado preparado, para que a oportunidade exista para corrigir incrementalmente os problemas que causaram erros e repita a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="09cda-185">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="09cda-186">Comentários</span><span class="sxs-lookup"><span data-stu-id="09cda-186">Remarks</span></span>

<span data-ttu-id="09cda-187">As funções de retorno de chamada podem ser registradas para serem chamadas antes ou depois da inserção, e antes ou após a atualização.</span><span class="sxs-lookup"><span data-stu-id="09cda-187">Callback functions can be registered to be called before or after insert, and before or after update.</span></span>

<span data-ttu-id="09cda-188">As limitações de tamanho de registro são impostas por [JetSetColumn](./jetsetcolumn-function.md)e não em geral por **JetUpdate**.</span><span class="sxs-lookup"><span data-stu-id="09cda-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by **JetUpdate**.</span></span>

<span data-ttu-id="09cda-189">É importante entender o impacto da execução de um grande número de operações de atualização dentro de uma única transação.</span><span class="sxs-lookup"><span data-stu-id="09cda-189">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="09cda-190">Cada atualização do banco de dados deve ser controlada pelo mecanismo de banco de dados no repositório de versão.</span><span class="sxs-lookup"><span data-stu-id="09cda-190">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="09cda-191">O repositório de versão mantém um registro ao vivo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas.</span><span class="sxs-lookup"><span data-stu-id="09cda-191">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="09cda-192">Essas versões são usadas para dar suporte ao controle de simultaneidade de várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando o isolamento de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="09cda-192">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="09cda-193">Depois que o mecanismo de banco de dados tiver esgotado os recursos usados para armazenar essas versões, ele não poderá mais aceitar outras alterações até que algumas transações tenham sido concluídas para permitir que esses recursos sejam recuperados.</span><span class="sxs-lookup"><span data-stu-id="09cda-193">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="09cda-194">Quando o mecanismo estiver nesse estado, todas as atualizações falharão com JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="09cda-194">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="09cda-195">Os recursos disponíveis para o mecanismo de banco de dados para armazenar essas versões podem ser controlados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramMaxVerPages](./resource-parameters.md) e [JET_paramGlobalMinVerPages](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="09cda-195">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramMaxVerPages](./resource-parameters.md) and [JET_paramGlobalMinVerPages](./resource-parameters.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="09cda-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09cda-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09cda-197"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="09cda-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="09cda-198">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="09cda-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-199"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="09cda-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="09cda-200">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="09cda-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-201"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="09cda-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="09cda-202">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="09cda-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cda-203"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="09cda-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="09cda-204">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="09cda-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cda-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="09cda-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="09cda-206">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="09cda-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="09cda-207">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="09cda-207">See Also</span></span>

[<span data-ttu-id="09cda-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="09cda-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="09cda-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="09cda-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="09cda-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="09cda-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="09cda-211">JetDelete</span><span class="sxs-lookup"><span data-stu-id="09cda-211">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="09cda-212">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="09cda-212">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="09cda-213">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="09cda-213">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="09cda-214">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="09cda-214">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="09cda-215">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="09cda-215">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="09cda-216">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="09cda-216">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="09cda-217">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="09cda-217">JetSetColumns</span></span>](./jetsetcolumns-function.md)  
[<span data-ttu-id="09cda-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="09cda-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="09cda-219">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="09cda-219">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
