---
description: 'Saiba mais sobre: função JetEndExternalBackup'
title: Função JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764553"
---
# <a name="jetendexternalbackup-function"></a><span data-ttu-id="08f9d-103">Função JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="08f9d-103">JetEndExternalBackup Function</span></span>


<span data-ttu-id="08f9d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="08f9d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackup-function"></a><span data-ttu-id="08f9d-105">Função JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="08f9d-105">JetEndExternalBackup Function</span></span>

<span data-ttu-id="08f9d-106">A função **JetEndExternalBackup** encerra uma sessão de backup externo.</span><span class="sxs-lookup"><span data-stu-id="08f9d-106">The **JetEndExternalBackup** function ends an external backup session.</span></span> <span data-ttu-id="08f9d-107">Essa função é o último elemento de API em uma série de elementos de API que devem ser chamados para executar um backup online (não baseado em VSS) com êxito.</span><span class="sxs-lookup"><span data-stu-id="08f9d-107">This function is the last API element in a series of API elements that must be called to execute a successful online (non-VSS based) backup.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="08f9d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08f9d-108">Parameters</span></span>

<span data-ttu-id="08f9d-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="08f9d-109">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="08f9d-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="08f9d-110">Return Value</span></span>

<span data-ttu-id="08f9d-111">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="08f9d-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="08f9d-112">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="08f9d-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08f9d-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="08f9d-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="08f9d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="08f9d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="08f9d-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="08f9d-116">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="08f9d-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f9d-117">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="08f9d-117">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="08f9d-118">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="08f9d-118">The operation cannot complete because the instance that is associated with the session has not been yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="08f9d-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="08f9d-120">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="08f9d-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f9d-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="08f9d-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="08f9d-122"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP</span><span class="sxs-lookup"><span data-stu-id="08f9d-122"><strong>Windows XP:  </strong>This return value is introduced in Windows XP</span></span></p>
<p><span data-ttu-id="08f9d-123">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer acesso a todos os dados revogados para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="08f9d-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-124">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="08f9d-124">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="08f9d-125">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="08f9d-125">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f9d-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="08f9d-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="08f9d-127">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="08f9d-127">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-128">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="08f9d-128">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="08f9d-129">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="08f9d-129">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f9d-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="08f9d-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="08f9d-131"><strong>Windows Server 2003:  </strong> Esse valor de retorno é introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="08f9d-131"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="08f9d-132">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="08f9d-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-133">errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="08f9d-133">errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="08f9d-134"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08f9d-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="08f9d-135">O chamador encerrou um backup no meio da sequência de backup sem sinalizar a intenção com <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="08f9d-135">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="08f9d-136">Esse erro é resultado de um bug no cliente de backup no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="08f9d-136">This error is a result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="08f9d-137">No Windows XP, esse erro é retornado para um encerramento intencional da sequência de backup externo.</span><span class="sxs-lookup"><span data-stu-id="08f9d-137">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f9d-138">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="08f9d-138">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="08f9d-139">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="08f9d-139">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="08f9d-140">Se essa função for bem-sucedida, o backup externo foi um sucesso.</span><span class="sxs-lookup"><span data-stu-id="08f9d-140">If this function succeeds, the external backup was a success.</span></span> <span data-ttu-id="08f9d-141">Êxito indica que todos os arquivos (por exemplo, bancos de dados e logs) apropriados para o tipo de backup (especificado em [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) foram recuperados do mecanismo de backup.</span><span class="sxs-lookup"><span data-stu-id="08f9d-141">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="08f9d-142">Os arquivos de backup podem ser recuperados com a[JetExternalRestore](./jetexternalrestore-function.md)(recuperação de hardware).</span><span class="sxs-lookup"><span data-stu-id="08f9d-142">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="08f9d-143">Se essa função falhar, o backup externo geralmente termina.</span><span class="sxs-lookup"><span data-stu-id="08f9d-143">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="08f9d-144">Falha significa que o backup é inválido devido a um erro de uso do cliente ou do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08f9d-144">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="08f9d-145">É importante verificar o código de retorno dessa API para verificar se a sequência de backup foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="08f9d-145">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="08f9d-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="08f9d-146">Remarks</span></span>

<span data-ttu-id="08f9d-147">Se o mecanismo estiver configurado para registrar eventos, um evento será registrado para indicar a resolução do backup externo.</span><span class="sxs-lookup"><span data-stu-id="08f9d-147">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="08f9d-148">Se a sequência de backup não for concluída na ordem e com uma chamada bem-sucedida para **JetEndExternalBackup**, os backups incrementais subsequentes poderão conter mais dados do que o aplicativo previsto.</span><span class="sxs-lookup"><span data-stu-id="08f9d-148">If the backup sequence is not completed in order and with a successful call to **JetEndExternalBackup**, subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="08f9d-149">Para obter mais informações sobre a sequência de API de backup externo, consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="08f9d-149">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="08f9d-150">Antes do Windows Vista, se o truncamento de log não foi feito, o mecanismo considerou que o backup era um backup de cópia.</span><span class="sxs-lookup"><span data-stu-id="08f9d-150">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="08f9d-151">No entanto, o backup pode ser um backup normal para o qual o truncamento não foi feito (por exemplo, se houver bancos de dados desanexados).</span><span class="sxs-lookup"><span data-stu-id="08f9d-151">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="08f9d-152">A opção JET_bitBackupTruncateDone pode ser usada para informar o mecanismo sobre isso e permitir modificações apropriadas no cabeçalho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08f9d-152">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="08f9d-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f9d-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-154"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="08f9d-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="08f9d-155">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="08f9d-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f9d-156"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="08f9d-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="08f9d-157">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="08f9d-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-158"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="08f9d-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="08f9d-159">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="08f9d-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08f9d-160"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="08f9d-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="08f9d-161">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="08f9d-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08f9d-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="08f9d-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="08f9d-163">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="08f9d-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="08f9d-164">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="08f9d-164">See Also</span></span>

[<span data-ttu-id="08f9d-165">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="08f9d-165">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="08f9d-166">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="08f9d-166">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="08f9d-167">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="08f9d-167">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="08f9d-168">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="08f9d-168">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="08f9d-169">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="08f9d-169">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="08f9d-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="08f9d-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="08f9d-171">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="08f9d-171">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="08f9d-172">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="08f9d-172">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="08f9d-173">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="08f9d-173">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="08f9d-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="08f9d-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="08f9d-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="08f9d-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="08f9d-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="08f9d-176">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="08f9d-177">JetStopService</span><span class="sxs-lookup"><span data-stu-id="08f9d-177">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="08f9d-178">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="08f9d-178">JetTruncateLog</span></span>](./jettruncatelog-function.md)
