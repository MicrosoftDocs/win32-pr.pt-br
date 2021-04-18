---
description: 'Saiba mais sobre: função JetGetTruncateLogInfoInstance'
title: Função JetGetTruncateLogInfoInstance
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765280"
---
# <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="96ab0-103">Função JetGetTruncateLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="96ab0-103">JetGetTruncateLogInfoInstance Function</span></span>


<span data-ttu-id="96ab0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="96ab0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="96ab0-105">Função JetGetTruncateLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="96ab0-105">JetGetTruncateLogInfoInstance Function</span></span>

<span data-ttu-id="96ab0-106">A função **JetGetTruncateLogInfoInstance** é usada durante um backup iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar uma instância para obter os nomes dos arquivos de log de transações que podem ser excluídos com segurança depois que o backup for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="96ab0-106">The **JetGetTruncateLogInfoInstance** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="96ab0-107">**Windows XP:** o **JetGetTruncateLogInfoInstance** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="96ab0-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="96ab0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96ab0-108">Parameters</span></span>

<span data-ttu-id="96ab0-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="96ab0-109">*instance*</span></span>

<span data-ttu-id="96ab0-110">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="96ab0-110">The instance to use for this call.</span></span>

<span data-ttu-id="96ab0-111">*szz*</span><span class="sxs-lookup"><span data-stu-id="96ab0-111">*szz*</span></span>

<span data-ttu-id="96ab0-112">O buffer de saída que recebe a lista de cadeias de caracteres terminadas em nulo que descreve o conjunto de arquivos de log de transações que podem ser excluídos com segurança após a conclusão bem-sucedida do backup.</span><span class="sxs-lookup"><span data-stu-id="96ab0-112">The output buffer that receives the list of null-terminated strings describing the set of transaction log files that can be safely deleted after the backup has been completed successfully.</span></span>

<span data-ttu-id="96ab0-113">A lista de cadeias de caracteres que são retornadas nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="96ab0-113">The list of strings that are returned in this buffer is in the same format as a multi-string that is used by the registry.</span></span> <span data-ttu-id="96ab0-114">Cada cadeia de caracteres terminada em nulo é retornada em sequência e seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="96ab0-114">Each null-terminated string is returned in sequence and followed by a final null terminator.</span></span>

<span data-ttu-id="96ab0-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="96ab0-115">*cbMax*</span></span>

<span data-ttu-id="96ab0-116">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="96ab0-116">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="96ab0-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="96ab0-117">*pcbActual*</span></span>

<span data-ttu-id="96ab0-118">Ponteiro para o buffer de saída que recebe a quantidade real de dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="96ab0-118">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="96ab0-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="96ab0-119">Return Value</span></span>

<span data-ttu-id="96ab0-120">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="96ab0-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="96ab0-121">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="96ab0-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96ab0-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="96ab0-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="96ab0-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="96ab0-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="96ab0-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="96ab0-125">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="96ab0-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="96ab0-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="96ab0-127">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro resultou em um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="96ab0-127">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="96ab0-128"><strong>Windows XP e posterior:</strong>  Isso pode ocorrer para <strong>JetGetTruncateLogInfoInstance</strong> quando o identificador de instância especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="96ab0-128"><strong>Windows XP and later:</strong>  This can happen for <strong>JetGetTruncateLogInfoInstance</strong> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="96ab0-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="96ab0-130">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="96ab0-130">The operation cannot complete because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="96ab0-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="96ab0-132">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="96ab0-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="96ab0-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="96ab0-134">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="96ab0-134">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="96ab0-135"><strong>Windows XP:</strong>  Esse valor de retorno foi introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96ab0-135"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-136">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="96ab0-136">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="96ab0-137">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="96ab0-137">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="96ab0-138"><strong>Windows XP:</strong>  Esse valor de retorno foi introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96ab0-138"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="96ab0-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="96ab0-140">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="96ab0-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-141">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="96ab0-141">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="96ab0-142">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="96ab0-142">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="96ab0-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="96ab0-144">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="96ab0-144">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="96ab0-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="96ab0-146">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="96ab0-146">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-147"><strong>JetGetTruncateLogInfoInstance</strong></span><span class="sxs-lookup"><span data-stu-id="96ab0-147"><strong>JetGetTruncateLogInfoInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="96ab0-148">Há identificadores de arquivo pendentes que foram criados usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</span><span class="sxs-lookup"><span data-stu-id="96ab0-148">There are outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96ab0-149">Se essa função for bem-sucedida, as informações solicitadas sobre o conjunto de arquivos de log de transações que podem ser excluídas com segurança após a conclusão bem-sucedida do backup serão colocadas nos buffers de saída em que são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="96ab0-149">If this function succeeds, the requested information about the set of transaction log files that can be safely deleted after the backup has been completed successfully will be placed in the output buffers where they are provided.</span></span> <span data-ttu-id="96ab0-150">O computador de estado de backup será avançado de modo que o backup de arquivos de banco de dados não seja mais permitido.</span><span class="sxs-lookup"><span data-stu-id="96ab0-150">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="96ab0-151">Somente arquivos de patch de banco de dados e arquivos de log de transações podem ser abertos para backup além desse ponto.</span><span class="sxs-lookup"><span data-stu-id="96ab0-151">Only database patch files and transaction log files can be opened for backup beyond this point.</span></span>

<span data-ttu-id="96ab0-152">Se essa função falhar, o estado dos buffers de saída será indefinido.</span><span class="sxs-lookup"><span data-stu-id="96ab0-152">If this function fails, the state of the output buffers is undefined.</span></span> <span data-ttu-id="96ab0-153">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="96ab0-153">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="96ab0-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="96ab0-154">Remarks</span></span>

<span data-ttu-id="96ab0-155">Essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="96ab0-155">This API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="96ab0-156">O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="96ab0-156">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="96ab0-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96ab0-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="96ab0-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="96ab0-159">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96ab0-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-160"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="96ab0-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="96ab0-161">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="96ab0-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-162"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="96ab0-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="96ab0-163">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="96ab0-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-164"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="96ab0-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="96ab0-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="96ab0-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96ab0-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="96ab0-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="96ab0-167">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="96ab0-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96ab0-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="96ab0-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="96ab0-169">Implementado como <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) e <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="96ab0-169">Implemented as <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) and <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="96ab0-170">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="96ab0-170">See Also</span></span>

[<span data-ttu-id="96ab0-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="96ab0-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="96ab0-172">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="96ab0-172">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="96ab0-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="96ab0-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="96ab0-174">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="96ab0-174">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="96ab0-175">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="96ab0-175">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="96ab0-176">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="96ab0-176">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="96ab0-177">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="96ab0-177">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="96ab0-178">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="96ab0-178">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="96ab0-179">JetRollback</span><span class="sxs-lookup"><span data-stu-id="96ab0-179">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="96ab0-180">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="96ab0-180">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="96ab0-181">JetStopService</span><span class="sxs-lookup"><span data-stu-id="96ab0-181">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="96ab0-182">JetTerm</span><span class="sxs-lookup"><span data-stu-id="96ab0-182">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="96ab0-183">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="96ab0-183">JetTerm2</span></span>](./jetterm2-function.md)
