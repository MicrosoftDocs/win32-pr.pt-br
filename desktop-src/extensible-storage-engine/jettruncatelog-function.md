---
description: 'Saiba mais sobre: função JetTruncateLog'
title: Função JetTruncateLog
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e196a1570f769d8ae2619e962521bb181d506d63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646894"
---
# <a name="jettruncatelog-function"></a><span data-ttu-id="6bdeb-103">Função JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="6bdeb-103">JetTruncateLog Function</span></span>


<span data-ttu-id="6bdeb-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6bdeb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncatelog-function"></a><span data-ttu-id="6bdeb-105">Função JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="6bdeb-105">JetTruncateLog Function</span></span>

<span data-ttu-id="6bdeb-106">A função **JetTruncateLog** é usada durante um backup que é iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para excluir todos os arquivos de log de transações que não serão mais necessários quando o backup atual for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-106">The **JetTruncateLog** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a><span data-ttu-id="6bdeb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bdeb-107">Parameters</span></span>

<span data-ttu-id="6bdeb-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-108">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="6bdeb-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6bdeb-109">Return Value</span></span>

<span data-ttu-id="6bdeb-110">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-110">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6bdeb-111">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6bdeb-111">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6bdeb-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6bdeb-112">Return code</span></span></p></th>
<th><p><span data-ttu-id="6bdeb-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bdeb-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-114">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6bdeb-114">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-115">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-115">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdeb-116">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="6bdeb-116">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-117">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-117">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="6bdeb-118"><strong>Windows Server 2003:</strong>  Esse valor de retorno é introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-118"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6bdeb-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-120">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdeb-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6bdeb-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-122">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-122">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="6bdeb-123"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-123"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-124">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="6bdeb-124">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-125">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-125">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="6bdeb-126"><strong>JetTruncateLog</strong> retornará esse erro se houver identificadores de arquivo pendentes que foram criados usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-126"><strong>JetTruncateLog</strong> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdeb-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6bdeb-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-128">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-128">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="6bdeb-129">Isso pode ocorrer para <strong>JetTruncateLog</strong> quando o identificador de instância especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-129">This can happen for <strong>JetTruncateLog</strong> when the specified instance handle is invalid.</span></span></p>
<p><span data-ttu-id="6bdeb-130"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-130"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-131">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="6bdeb-131">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-132">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-132">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdeb-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6bdeb-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-134">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-134">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6bdeb-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-136">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdeb-137">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6bdeb-137">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-138">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-138">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-139">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6bdeb-139">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6bdeb-140">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-140">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6bdeb-141">Se essa função for bem-sucedida, o conjunto de arquivos de log de transações que não será mais necessário quando o backup atual for concluído com êxito será excluído.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-141">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="6bdeb-142">O computador de estado de backup será avançado de modo que o backup de arquivos de banco de dados não seja mais permitido.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-142">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="6bdeb-143">Somente arquivos de patch de banco de dados e arquivos de log de transações podem ser abertos para backup além desse ponto.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-143">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="6bdeb-144">Se essa função falhar, o computador de estado de backup poderá ser avançado, de modo que o backup de arquivos de banco de dados não seja mais permitido.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-144">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="6bdeb-145">Um número de arquivos de log de transações pode ser excluído, que é menor que o número desejado, mas eles sempre serão excluídos do mais antigo para o mais recente.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-145">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6bdeb-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bdeb-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-147"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6bdeb-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6bdeb-148">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdeb-149"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6bdeb-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6bdeb-150">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-151"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6bdeb-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6bdeb-152">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdeb-153"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6bdeb-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6bdeb-154">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bdeb-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6bdeb-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6bdeb-156">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6bdeb-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6bdeb-157">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6bdeb-157">See Also</span></span>

[<span data-ttu-id="6bdeb-158">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="6bdeb-158">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="6bdeb-159">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="6bdeb-159">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="6bdeb-160">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6bdeb-160">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6bdeb-161">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6bdeb-161">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="6bdeb-162">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="6bdeb-162">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="6bdeb-163">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="6bdeb-163">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="6bdeb-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="6bdeb-164">JetStopService</span></span>](./jetstopservice-function.md)
