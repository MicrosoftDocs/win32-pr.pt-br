---
description: 'Saiba mais sobre: função JetEndExternalBackupInstance'
title: Função JetEndExternalBackupInstance
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011414"
---
# <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="655bf-103">Função JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="655bf-103">JetEndExternalBackupInstance Function</span></span>


<span data-ttu-id="655bf-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="655bf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="655bf-105">Função JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="655bf-105">JetEndExternalBackupInstance Function</span></span>

<span data-ttu-id="655bf-106">A função **JetEndExternalBackupInstance** encerra uma sessão de backup externo.</span><span class="sxs-lookup"><span data-stu-id="655bf-106">The **JetEndExternalBackupInstance** function ends an external backup session.</span></span> <span data-ttu-id="655bf-107">Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</span><span class="sxs-lookup"><span data-stu-id="655bf-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="655bf-108">**Windows XP: o JetEndExternalBackupInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="655bf-108">**Windows XP:  JetEndExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="655bf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="655bf-109">Parameters</span></span>

<span data-ttu-id="655bf-110">*cópia*</span><span class="sxs-lookup"><span data-stu-id="655bf-110">*instance*</span></span>

<span data-ttu-id="655bf-111">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="655bf-111">The instance to use for this call.</span></span>

<span data-ttu-id="655bf-112">**Windows 2000:** Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="655bf-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="655bf-113">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="655bf-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="655bf-114">**Windows XP:** Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="655bf-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="655bf-115">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="655bf-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="655bf-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="655bf-116">Return Value</span></span>

<span data-ttu-id="655bf-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="655bf-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="655bf-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="655bf-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="655bf-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="655bf-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="655bf-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="655bf-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="655bf-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="655bf-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="655bf-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="655bf-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="655bf-123">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="655bf-123">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="655bf-124"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="655bf-124"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="655bf-125">O chamador encerrou um backup no meio da sequência de backup sem sinalizar a intenção com <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="655bf-125">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="655bf-126">Esse erro é o resultado de um bug no cliente de backup no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="655bf-126">This error is the result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="655bf-127">No Windows XP, esse erro é retornado para um encerramento intencional da sequência de backup externo.</span><span class="sxs-lookup"><span data-stu-id="655bf-127">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="655bf-128">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="655bf-128">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="655bf-129"><strong>Windows Server 2003:  </strong> Esse valor de retorno é introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="655bf-129"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="655bf-130">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="655bf-130">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="655bf-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="655bf-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="655bf-132">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="655bf-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="655bf-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="655bf-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="655bf-134"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="655bf-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="655bf-135">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="655bf-135">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="655bf-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="655bf-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="655bf-137">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="655bf-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="655bf-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="655bf-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="655bf-139">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="655bf-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="655bf-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="655bf-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="655bf-141">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="655bf-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="655bf-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="655bf-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="655bf-143">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="655bf-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="655bf-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="655bf-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="655bf-145">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="655bf-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="655bf-146">Se a função for bem-sucedida, o backup externo foi um sucesso.</span><span class="sxs-lookup"><span data-stu-id="655bf-146">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="655bf-147">Êxito indica que todos os arquivos (por exemplo, bancos de dados e logs) apropriados para o tipo de backup (especificado em [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) foram recuperados do mecanismo de backup.</span><span class="sxs-lookup"><span data-stu-id="655bf-147">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="655bf-148">Os arquivos de backup podem ser recuperados com a[JetExternalRestore](./jetexternalrestore-function.md)(recuperação de hardware).</span><span class="sxs-lookup"><span data-stu-id="655bf-148">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="655bf-149">Se essa função falhar, o backup externo geralmente termina.</span><span class="sxs-lookup"><span data-stu-id="655bf-149">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="655bf-150">Falha significa que o backup é inválido devido a um erro de uso do cliente ou do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="655bf-150">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="655bf-151">É importante verificar o código de retorno dessa API para verificar se a sequência de backup foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="655bf-151">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="655bf-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="655bf-152">Remarks</span></span>

<span data-ttu-id="655bf-153">Se o mecanismo estiver configurado para registrar eventos, um evento será registrado para indicar a resolução do backup externo.</span><span class="sxs-lookup"><span data-stu-id="655bf-153">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="655bf-154">Se a sequência de backup não for concluída na ordem e com uma chamada bem-sucedida para [JetEndExternalBackup](./jetendexternalbackup-function.md), os backups incrementais subsequentes poderão conter mais dados do que o aplicativo previsto.</span><span class="sxs-lookup"><span data-stu-id="655bf-154">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="655bf-155">Para obter mais informações sobre a sequência de API de backup externo, consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="655bf-155">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="655bf-156">Antes do Windows Vista, se o truncamento de log não foi feito, o mecanismo considerou que o backup era um backup de cópia.</span><span class="sxs-lookup"><span data-stu-id="655bf-156">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="655bf-157">No entanto, o backup pode ser um backup normal para o qual o truncamento não foi feito (por exemplo, se houver bancos de dados desanexados).</span><span class="sxs-lookup"><span data-stu-id="655bf-157">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="655bf-158">A opção JET_bitBackupTruncateDone pode ser usada para informar o mecanismo sobre isso e permitir modificações adequadas no cabeçalho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="655bf-158">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow proper database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="655bf-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="655bf-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="655bf-160"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="655bf-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="655bf-161">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="655bf-161">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="655bf-162"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="655bf-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="655bf-163">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="655bf-163">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="655bf-164"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="655bf-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="655bf-165">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="655bf-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="655bf-166"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="655bf-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="655bf-167">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="655bf-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="655bf-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="655bf-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="655bf-169">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="655bf-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="655bf-170">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="655bf-170">See Also</span></span>

[<span data-ttu-id="655bf-171">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="655bf-171">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="655bf-172">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="655bf-172">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="655bf-173">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="655bf-173">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="655bf-174">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="655bf-174">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="655bf-175">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="655bf-175">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="655bf-176">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="655bf-176">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="655bf-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="655bf-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="655bf-178">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="655bf-178">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="655bf-179">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="655bf-179">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="655bf-180">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="655bf-180">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="655bf-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="655bf-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="655bf-182">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="655bf-182">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="655bf-183">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="655bf-183">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="655bf-184">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="655bf-184">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="655bf-185">JetStopService</span><span class="sxs-lookup"><span data-stu-id="655bf-185">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="655bf-186">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="655bf-186">JetTruncateLog</span></span>](./jettruncatelog-function.md)
