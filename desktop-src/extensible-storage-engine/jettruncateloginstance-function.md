---
description: 'Saiba mais sobre: função JetTruncateLogInstance'
title: Função JetTruncateLogInstance
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768290"
---
# <a name="jettruncateloginstance-function"></a><span data-ttu-id="c2170-103">Função JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="c2170-103">JetTruncateLogInstance Function</span></span>


<span data-ttu-id="c2170-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c2170-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncateloginstance-function"></a><span data-ttu-id="c2170-105">Função JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="c2170-105">JetTruncateLogInstance Function</span></span>

<span data-ttu-id="c2170-106">A função **JetTruncateLogInstance** é usada durante um backup iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para excluir todos os arquivos de log de transações que não serão mais necessários quando o backup atual for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="c2170-106">The **JetTruncateLogInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="c2170-107">**Windows XP:** o **JetTruncateLogInstance** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="c2170-107">**Windows XP:**  **JetTruncateLogInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="c2170-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2170-108">Parameters</span></span>

<span data-ttu-id="c2170-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="c2170-109">*instance*</span></span>

<span data-ttu-id="c2170-110">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="c2170-110">The instance to use for this call.</span></span>

<span data-ttu-id="c2170-111">Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="c2170-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="c2170-112">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="c2170-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="c2170-113">Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="c2170-113">For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="c2170-114">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="c2170-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="c2170-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c2170-115">Return Value</span></span>

<span data-ttu-id="c2170-116">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2170-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c2170-117">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c2170-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2170-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c2170-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="c2170-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2170-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2170-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c2170-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c2170-121">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c2170-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2170-122">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="c2170-122">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="c2170-123"><strong>Windows Server 2003:</strong>  Esse valor de retorno é introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c2170-123"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="c2170-124">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="c2170-124">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2170-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c2170-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c2170-126">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c2170-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2170-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c2170-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c2170-128">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="c2170-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c2170-129">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="c2170-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2170-130">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="c2170-130">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="c2170-131">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="c2170-131">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="c2170-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> retornará esse erro se houver identificadores de arquivo pendentes que foram criados usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</span><span class="sxs-lookup"><span data-stu-id="c2170-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2170-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c2170-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c2170-134">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="c2170-134">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="c2170-135">Isso pode ocorrer para <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> quando o identificador de instância especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="c2170-135">This can happen for <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2170-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="c2170-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="c2170-137">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="c2170-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2170-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c2170-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c2170-139">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="c2170-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2170-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c2170-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c2170-141">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="c2170-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2170-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c2170-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="c2170-143">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="c2170-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2170-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c2170-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c2170-145">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="c2170-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c2170-146">Se essa função for bem-sucedida, o conjunto de arquivos de log de transações que não será mais necessário quando o backup atual for concluído com êxito será excluído.</span><span class="sxs-lookup"><span data-stu-id="c2170-146">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="c2170-147">O computador de estado de backup será avançado de modo que o backup de arquivos de banco de dados não seja mais permitido.</span><span class="sxs-lookup"><span data-stu-id="c2170-147">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="c2170-148">Somente arquivos de patch de banco de dados e arquivos de log de transações podem ser abertos para backup além desse ponto.</span><span class="sxs-lookup"><span data-stu-id="c2170-148">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="c2170-149">Se essa função falhar, o computador de estado de backup poderá ser avançado, de modo que o backup de arquivos de banco de dados não seja mais permitido.</span><span class="sxs-lookup"><span data-stu-id="c2170-149">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="c2170-150">Um número de arquivos de log de transações pode ser excluído, que é menor que o número desejado, mas eles sempre serão excluídos do mais antigo para o mais recente.</span><span class="sxs-lookup"><span data-stu-id="c2170-150">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c2170-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2170-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2170-152"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c2170-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c2170-153">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c2170-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2170-154"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c2170-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c2170-155">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c2170-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2170-156"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c2170-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c2170-157">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c2170-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2170-158"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="c2170-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c2170-159">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c2170-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2170-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c2170-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c2170-161">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c2170-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c2170-162">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c2170-162">See Also</span></span>

[<span data-ttu-id="c2170-163">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="c2170-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="c2170-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c2170-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c2170-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c2170-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c2170-166">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="c2170-166">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="c2170-167">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="c2170-167">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="c2170-168">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="c2170-168">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="c2170-169">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c2170-169">JetStopService</span></span>](./jetstopservice-function.md)
