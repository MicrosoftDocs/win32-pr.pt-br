---
description: 'Saiba mais sobre: função JetEndExternalBackupInstance2'
title: Função JetEndExternalBackupInstance2
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e719885cc61ff3f3193046b632e9969b8d660f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765292"
---
# <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="d6bf6-103">Função JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="d6bf6-103">JetEndExternalBackupInstance2 Function</span></span>


<span data-ttu-id="d6bf6-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d6bf6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="d6bf6-105">Função JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="d6bf6-105">JetEndExternalBackupInstance2 Function</span></span>

<span data-ttu-id="d6bf6-106">A função **JetEndExternalBackupInstance2** encerra uma sessão de backup externo.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-106">The **JetEndExternalBackupInstance2** function ends an external backup session.</span></span> <span data-ttu-id="d6bf6-107">Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="d6bf6-108">**Windows XP: o JetEndExternalBackupInstance2** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-108">**Windows XP:  JetEndExternalBackupInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d6bf6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6bf6-109">Parameters</span></span>

<span data-ttu-id="d6bf6-110">*cópia*</span><span class="sxs-lookup"><span data-stu-id="d6bf6-110">*instance*</span></span>

<span data-ttu-id="d6bf6-111">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-111">The instance to use for this call.</span></span>

<span data-ttu-id="d6bf6-112">**Windows 2000:** Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="d6bf6-113">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="d6bf6-114">**Windows XP:** Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="d6bf6-115">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="d6bf6-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d6bf6-116">*grbit*</span></span>

<span data-ttu-id="d6bf6-117">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-117">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6bf6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d6bf6-118">Value</span></span></p></th>
<th><p><span data-ttu-id="d6bf6-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d6bf6-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-120">JET_bitBackupEndAbort</span><span class="sxs-lookup"><span data-stu-id="d6bf6-120">JET_bitBackupEndAbort</span></span><br />
<span data-ttu-id="d6bf6-121">0x0002</span><span class="sxs-lookup"><span data-stu-id="d6bf6-121">0x0002</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-122">O aplicativo cliente está anulando o backup.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-122">The client application is aborting the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-123">JET_bitBackupEndNormal</span><span class="sxs-lookup"><span data-stu-id="d6bf6-123">JET_bitBackupEndNormal</span></span><br />
<span data-ttu-id="d6bf6-124">0x0001</span><span class="sxs-lookup"><span data-stu-id="d6bf6-124">0x0001</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-125">O aplicativo cliente concluiu o backup completamente e está terminando normalmente.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-125">The client application finished the backup completely, and is ending normally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-126">JET_bitBackupTruncateDone</span><span class="sxs-lookup"><span data-stu-id="d6bf6-126">JET_bitBackupTruncateDone</span></span><br />
<span data-ttu-id="d6bf6-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="d6bf6-127">0x0100</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-128"><strong>Windows Vista:  </strong> O JET_bitBackupTruncateDone é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-128"><strong>Windows Vista:  </strong>JET_bitBackupTruncateDone is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="d6bf6-129">O mecanismo pode marcar os cabeçalhos do banco de dados conforme apropriado (por exemplo, um backup completo concluído), mesmo que a chamada para truncar não tenha sido concluída.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-129">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d6bf6-130">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d6bf6-130">Return Value</span></span>

<span data-ttu-id="d6bf6-131">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d6bf6-132">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d6bf6-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6bf6-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d6bf6-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="d6bf6-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6bf6-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d6bf6-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-136">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-137">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="d6bf6-137">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-138"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-138"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="d6bf6-139">O chamador encerrou um backup no meio da sequência de backup sem sinalizar a intenção com <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-139">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="d6bf6-140">Esse erro é resultado de um bug no cliente de backup no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-140">This error is result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="d6bf6-141">No Windows XP, esse erro é retornado para um encerramento intencional da sequência de backup externo.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-141">In Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-142">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="d6bf6-142">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-143"><strong>Windows Server 2003:  </strong> Esse valor de retorno é introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-143"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="d6bf6-144">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-144">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d6bf6-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-146">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-146">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d6bf6-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-148"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="d6bf6-149">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-149">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="d6bf6-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-151">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d6bf6-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-153">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d6bf6-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-155">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-155">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-156">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="d6bf6-156">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-157">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-157">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d6bf6-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d6bf6-159">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-159">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6bf6-160">Se a função for bem-sucedida, o backup externo foi um sucesso.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-160">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="d6bf6-161">Êxito indica que todos os arquivos (por exemplo, bancos de dados e logs) apropriados para o tipo de backup (especificado em [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) foram recuperados do mecanismo de backup.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-161">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="d6bf6-162">Os arquivos de backup podem ser recuperados com a[JetExternalRestore](./jetexternalrestore-function.md)(recuperação de hardware).</span><span class="sxs-lookup"><span data-stu-id="d6bf6-162">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="d6bf6-163">Se essa função falhar, o backup externo geralmente termina.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-163">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="d6bf6-164">Falha significa que o backup é inválido devido a um erro de uso do cliente ou do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-164">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="d6bf6-165">É importante verificar o código de retorno dessa API para verificar se a sequência de backup foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-165">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d6bf6-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6bf6-166">Remarks</span></span>

<span data-ttu-id="d6bf6-167">Se o mecanismo estiver configurado para registrar eventos, um evento será registrado para indicar a resolução do backup externo.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-167">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="d6bf6-168">Se a sequência de backup não for concluída na ordem e com uma chamada bem-sucedida para [JetEndExternalBackup](./jetendexternalbackup-function.md), os backups incrementais subsequentes poderão conter mais dados do que o aplicativo previsto.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-168">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="d6bf6-169">Para obter mais informações sobre a sequência de API de backup externo, consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="d6bf6-169">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="d6bf6-170">Antes do Windows Vista, se o truncamento de log não foi feito, o mecanismo considerou que o backup era um backup de cópia.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-170">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="d6bf6-171">No entanto, o backup pode ser um backup normal para o qual o truncamento não foi feito (por exemplo, se houver bancos de dados desanexados).</span><span class="sxs-lookup"><span data-stu-id="d6bf6-171">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="d6bf6-172">A opção JET_bitBackupTruncateDone pode ser usada para informar o mecanismo sobre isso e permitir modificações apropriadas no cabeçalho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-172">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d6bf6-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6bf6-173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-174"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d6bf6-174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d6bf6-175">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-175">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-176"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d6bf6-176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d6bf6-177">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-177">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-178"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d6bf6-178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d6bf6-179">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-179">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6bf6-180"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d6bf6-180"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d6bf6-181">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-181">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6bf6-182"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d6bf6-182"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d6bf6-183">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-183">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d6bf6-184">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d6bf6-184">See Also</span></span>

[<span data-ttu-id="d6bf6-185">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="d6bf6-185">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="d6bf6-186">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="d6bf6-186">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="d6bf6-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d6bf6-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d6bf6-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d6bf6-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d6bf6-189">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="d6bf6-189">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="d6bf6-190">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="d6bf6-190">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="d6bf6-191">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="d6bf6-191">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="d6bf6-192">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="d6bf6-192">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="d6bf6-193">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="d6bf6-193">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="d6bf6-194">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="d6bf6-194">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="d6bf6-195">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="d6bf6-195">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="d6bf6-196">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d6bf6-196">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="d6bf6-197">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="d6bf6-197">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="d6bf6-198">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="d6bf6-198">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="d6bf6-199">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="d6bf6-199">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="d6bf6-200">JetStopService</span><span class="sxs-lookup"><span data-stu-id="d6bf6-200">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="d6bf6-201">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="d6bf6-201">JetTruncateLog</span></span>](./jettruncatelog-function.md)
