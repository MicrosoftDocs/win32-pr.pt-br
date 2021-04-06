---
description: 'Saiba mais sobre: função JetUpdate2'
title: Função JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646893"
---
# <a name="jetupdate2-function"></a><span data-ttu-id="d5817-103">Função JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="d5817-103">JetUpdate2 Function</span></span>


<span data-ttu-id="d5817-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d5817-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate2-function"></a><span data-ttu-id="d5817-105">Função JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="d5817-105">JetUpdate2 Function</span></span>

<span data-ttu-id="d5817-106">A função **JetUpdate2** executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="d5817-106">The **JetUpdate2** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="d5817-107">Essa função contém uma lista de opções de *grbit* que podem ser definidas durante a execução de uma atualização.</span><span class="sxs-lookup"><span data-stu-id="d5817-107">This function contains a list of *grbit* options that can be set while performing an update.</span></span> <span data-ttu-id="d5817-108">A exclusão de uma linha de tabela é executada chamando [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="d5817-108">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="d5817-109">**Windows server 2003: o JetUpdate2** é introduzido no windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d5817-109">**Windows Server 2003:  JetUpdate2** is introduced in Windows Server 2003.</span></span>

<span data-ttu-id="d5817-110">**JetUpdate2** é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="d5817-110">**JetUpdate2** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="d5817-111">A atualização é iniciada chamando [JetPrepareUpdate](./jetprepareupdate-function.md) e, em seguida, chamando [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="d5817-111">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="d5817-112">Por fim, **JetUpdate2** é chamado para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="d5817-112">Finally, **JetUpdate2** is called to complete the update operation.</span></span> <span data-ttu-id="d5817-113">Os índices são atualizados somente por [JetUpdate](./jetupdate-function.md) ou **JetUpdate2**, e não durante [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="d5817-113">Indexes are updated only by [JetUpdate](./jetupdate-function.md) or **JetUpdate2**, and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d5817-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5817-114">Parameters</span></span>

<span data-ttu-id="d5817-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d5817-115">*sesid*</span></span>

<span data-ttu-id="d5817-116">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="d5817-116">The session to use for this call.</span></span>

<span data-ttu-id="d5817-117">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d5817-117">*tableid*</span></span>

<span data-ttu-id="d5817-118">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="d5817-118">The cursor to use for this call.</span></span>

<span data-ttu-id="d5817-119">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="d5817-119">*pvBookmark*</span></span>

<span data-ttu-id="d5817-120">Ponteiro para um indicador retornado para uma linha inserida.</span><span class="sxs-lookup"><span data-stu-id="d5817-120">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="d5817-121">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="d5817-121">*cbBookmark*</span></span>

<span data-ttu-id="d5817-122">Tamanho do buffer apontado por *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="d5817-122">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="d5817-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="d5817-123">*pcbActual*</span></span>

<span data-ttu-id="d5817-124">O tamanho retornado do indicador para a linha inserida retornada em *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="d5817-124">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

<span data-ttu-id="d5817-125">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d5817-125">*grbit*</span></span>

<span data-ttu-id="d5817-126">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5817-126">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5817-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d5817-127">Value</span></span></p></th>
<th><p><span data-ttu-id="d5817-128">Significado</span><span class="sxs-lookup"><span data-stu-id="d5817-128">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5817-129">JET_bitUpdateCheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="d5817-129">JET_bitUpdateCheckESE97Compatibility</span></span></p></td>
<td><p><span data-ttu-id="d5817-130">Esse sinalizador faz com que a atualização retorne um erro se a atualização não fosse possível na versão 2000 do Windows do ESE, que impõe um número menor máximo de instâncias de coluna com vários valores em cada registro do que as versões posteriores do ESE.</span><span class="sxs-lookup"><span data-stu-id="d5817-130">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="d5817-131">Isso é importante apenas para aplicativos que desejam replicar dados entre aplicativos hospedados no Windows 2000 e aplicativos hospedados no Windows Server 2003 ou versões posteriores do ESE.</span><span class="sxs-lookup"><span data-stu-id="d5817-131">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows Server 2003, or later versions of ESE.</span></span> <span data-ttu-id="d5817-132">Não deve ser necessário para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d5817-132">It should not be necessary for most applications.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d5817-133">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d5817-133">Return Value</span></span>

<span data-ttu-id="d5817-134">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5817-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d5817-135">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d5817-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5817-136">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d5817-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="d5817-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5817-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5817-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d5817-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d5817-139">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d5817-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-140">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d5817-140">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="d5817-141">O buffer fornecido para o indicador de registro não é suficientemente grande o suficiente para armazenar o indicador de registro.</span><span class="sxs-lookup"><span data-stu-id="d5817-141">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-142">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d5817-142">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d5817-143">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d5817-143">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-144">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="d5817-144">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="d5817-145">A operação de atualização requer o crescimento do arquivo de banco de dados ou a alocação do arquivo de log, mas a unidade de disco em que reside o arquivo de banco de dados ou a série de logs está cheia.</span><span class="sxs-lookup"><span data-stu-id="d5817-145">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="d5817-146">Como alternativa, o arquivo de banco de dados está em um volume formatado em FAT32 e o arquivo de banco de dados já está 4GBytes, o limite por arquivo para FAT32.</span><span class="sxs-lookup"><span data-stu-id="d5817-146">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d5817-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d5817-148">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="d5817-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d5817-149"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5817-149"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d5817-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d5817-151">O parâmetro <em>Prep</em> fornecido na função <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> não é um sinalizador válido.</span><span class="sxs-lookup"><span data-stu-id="d5817-151">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-152">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="d5817-152">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="d5817-153">Uma chave de índice para este registro é uma duplicata de outra chave de índice para outro registro que já está na tabela e o índice não permite duplicatas.</span><span class="sxs-lookup"><span data-stu-id="d5817-153">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-154">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="d5817-154">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="d5817-155">O registro inserido ou atualizado tem um ou mais índices para os quais a chave gerada teria excedido o tamanho máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="d5817-155">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="d5817-156">Como resultado, a operação falhou ao impedir o truncamento de chave.</span><span class="sxs-lookup"><span data-stu-id="d5817-156">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-157">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="d5817-157">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="d5817-158">O registro inserido ou atualizado tem uma coluna de vários valores indexada com dois ou mais valores que são idênticos no tamanho de chave de comprimento máximo definido para o índice.</span><span class="sxs-lookup"><span data-stu-id="d5817-158">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="d5817-159">Como resultado, o registro tem duas entradas idênticas no índice que são inválidas.</span><span class="sxs-lookup"><span data-stu-id="d5817-159">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d5817-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d5817-161">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="d5817-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-162">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="d5817-162">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="d5817-163">Uma ou mais colunas no registro a serem inseridas ou no estado atualizado de um registro que está sendo substituído são <strong>nulas</strong> , o que viola a restrição definida para essas colunas.</span><span class="sxs-lookup"><span data-stu-id="d5817-163">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-164">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="d5817-164">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="d5817-165">Um ou mais índices estão definidos para não permitir uma chave <strong>nula</strong> e o estado inserido ou atualizado de um registro que está sendo substituído viola essa restrição definida.</span><span class="sxs-lookup"><span data-stu-id="d5817-165">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-166">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="d5817-166">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="d5817-167">Uma operação de substituição de registro atualizou a chave primária.</span><span class="sxs-lookup"><span data-stu-id="d5817-167">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="d5817-168">As atualizações nas colunas de chave primária devem ser feitas por meio da exclusão do registro existente e da inserção de um novo registro com os dados desejados.</span><span class="sxs-lookup"><span data-stu-id="d5817-168">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-169">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d5817-169">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d5817-170">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="d5817-170">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-171">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d5817-171">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d5817-172">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d5817-172">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d5817-173"><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5817-173"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d5817-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d5817-175">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="d5817-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-176">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="d5817-176">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="d5817-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> foi chamado com JET_prepCancel, mas o cursor não estava no estado preparado.</span><span class="sxs-lookup"><span data-stu-id="d5817-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-178">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="d5817-178">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="d5817-179">Uma operação de substituição de registro para a qual um bloqueio de gravação ainda não foi alocado pode encontrar um conflito de gravação no momento da atualização.</span><span class="sxs-lookup"><span data-stu-id="d5817-179">A record replacement operation for which a write lock was not already allocated can encounter a write conflict at the time of update.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d5817-180">Em caso de sucesso, a operação abrir atualização no cursor é concluída.</span><span class="sxs-lookup"><span data-stu-id="d5817-180">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="d5817-181">Se uma coluna de incremento automático for definida para a tabela, esse valor será definido para registros inseridos.</span><span class="sxs-lookup"><span data-stu-id="d5817-181">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="d5817-182">Se uma coluna de versão for definida para a tabela, seu valor será inicializado para registros recentemente inseridos ou incrementado cada vez que um registro for substituído.</span><span class="sxs-lookup"><span data-stu-id="d5817-182">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="d5817-183">Todos os índices, incluindo índices clusterizados e não clusterizados, são atualizados.</span><span class="sxs-lookup"><span data-stu-id="d5817-183">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="d5817-184">Em caso de falha, nenhuma alteração de qualquer tipo é feita no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d5817-184">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="d5817-185">Antes de INSERT e before, as funções REPLACE de retorno de chamada podem ter sido chamadas, mas após INSERT e After Replace não serão chamadas, já que o último não pode fazer com que uma atualização falhe.</span><span class="sxs-lookup"><span data-stu-id="d5817-185">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="d5817-186">O buffer de cópia do cursor é deixado em seu estado preparado, para que a oportunidade exista para corrigir incrementalmente os problemas que causaram erros e repita a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="d5817-186">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5817-187">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5817-187">Remarks</span></span>

<span data-ttu-id="d5817-188">As limitações de tamanho de registro são impostas por [JetSetColumn](./jetsetcolumn-function.md)e não em geral por [JetUpdate](./jetupdate-function.md).</span><span class="sxs-lookup"><span data-stu-id="d5817-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by [JetUpdate](./jetupdate-function.md).</span></span> <span data-ttu-id="d5817-189">A única exceção é quando o sinalizador de compatibilidade JET_bitUpdateCheckESE97Compatibility está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="d5817-189">The only exception is when the JET_bitUpdateCheckESE97Compatibility compatibility flag is being used.</span></span> <span data-ttu-id="d5817-190">Nesse caso, o registro inteiro é verificado, pois uma operação [JetSetColumn](./jetsetcolumn-function.md) individual que excedeu o limite pode ser compensada por uma chamada subsequente para [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="d5817-190">In this case, the whole record is checked since an individual [JetSetColumn](./jetsetcolumn-function.md) operation that exceeded the limit may be compensated by a subsequent call to [JetSetColumn](./jetsetcolumn-function.md).</span></span>

<span data-ttu-id="d5817-191">Consulte a seção comentários em [JetUpdate](./jetupdate-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d5817-191">See the Remarks section in [JetUpdate](./jetupdate-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d5817-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5817-192">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5817-193"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d5817-193"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d5817-194">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d5817-194">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-195"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d5817-195"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d5817-196">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d5817-196">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-197"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d5817-197"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d5817-198">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d5817-198">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5817-199"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d5817-199"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d5817-200">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d5817-200">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5817-201"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d5817-201"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d5817-202">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d5817-202">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d5817-203">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d5817-203">See Also</span></span>

[<span data-ttu-id="d5817-204">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d5817-204">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d5817-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d5817-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d5817-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d5817-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d5817-207">JetDelete</span><span class="sxs-lookup"><span data-stu-id="d5817-207">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="d5817-208">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="d5817-208">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="d5817-209">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="d5817-209">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="d5817-210">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="d5817-210">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="d5817-211">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="d5817-211">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="d5817-212">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="d5817-212">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="d5817-213">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="d5817-213">JetSetColumns</span></span>](./jetsetcolumns-function.md)
