---
description: 'Saiba mais sobre: função JetGetLogInfo'
title: Função JetGetLogInfo
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c96827be0ac62502e7545a9acb1fe157f3b28fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662817"
---
# <a name="jetgetloginfo-function"></a><span data-ttu-id="f5b3f-103">Função JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="f5b3f-103">JetGetLogInfo Function</span></span>


<span data-ttu-id="f5b3f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f5b3f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfo-function"></a><span data-ttu-id="f5b3f-105">Função JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="f5b3f-105">JetGetLogInfo Function</span></span>

<span data-ttu-id="f5b3f-106">A função **JetGetLogInfo** é usada durante um backup iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar uma instância para obter os nomes dos arquivos de patch de banco de dados e dos arquivos de log de transações que devem se tornar parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-106">The **JetGetLogInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="f5b3f-107">Esses arquivos podem ser abertos subsequentemente usando [JetOpenFile](./jetopenfile-function.md) e lidos usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="f5b3f-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="f5b3f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5b3f-108">Parameters</span></span>

<span data-ttu-id="f5b3f-109">*szz*</span><span class="sxs-lookup"><span data-stu-id="f5b3f-109">*szz*</span></span>

<span data-ttu-id="f5b3f-110">O buffer de saída que receberá a lista de cadeias de caracteres terminadas em nulo que descreve o conjunto de arquivos de patch de banco de dados e os arquivos de log de transações que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-110">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="f5b3f-111">A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-111">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="f5b3f-112">Cada cadeia de caracteres terminada em NULL é retornada em sequência seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-112">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="f5b3f-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="f5b3f-113">*cbMax*</span></span>

<span data-ttu-id="f5b3f-114">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-114">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="f5b3f-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="f5b3f-115">*pcbActual*</span></span>

<span data-ttu-id="f5b3f-116">Recebe a quantidade real de dados de cadeia de caracteres recebidos no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-116">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="f5b3f-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f5b3f-117">Return Value</span></span>

<span data-ttu-id="f5b3f-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f5b3f-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f5b3f-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5b3f-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f5b3f-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="f5b3f-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5b3f-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f5b3f-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-124">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="f5b3f-124">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-125">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-125">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="f5b3f-126">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f5b3f-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-128">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f5b3f-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-130">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f5b3f-131">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-132">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="f5b3f-132">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-133">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-133">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="f5b3f-134"><strong>JetGetLogInfo</strong> retornará esse erro se houver algum identificador de arquivo pendente criado usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-134"><strong>JetGetLogInfo</strong> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f5b3f-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-136">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="f5b3f-137">Isso pode ocorrer para <strong>JetGetLogInfo</strong> quando o identificador de instância especificado é inválido (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="f5b3f-137">This can happen for <strong>JetGetLogInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-138">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="f5b3f-138">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-139">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-139">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-140">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f5b3f-140">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-141">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-141">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f5b3f-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-143">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-144">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f5b3f-144">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-145">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-145">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f5b3f-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f5b3f-147">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f5b3f-148">Em caso de sucesso, as informações solicitadas sobre o conjunto de arquivos de patch de banco de dados e arquivos de log de transações que devem ser parte do conjunto de arquivos de backup serão colocadas nos buffers de saída, onde fornecido.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-148">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="f5b3f-149">O computador de estado de backup será avançado de modo que o backup de arquivos de banco de dados não seja mais permitido.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-149">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="f5b3f-150">Somente arquivos de patch de banco de dados e arquivos de log de transações podem ser abertos para backup além desse ponto.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-150">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="f5b3f-151">Em caso de falha, o estado dos buffers de saída é indefinido.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-151">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="f5b3f-152">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-152">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f5b3f-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5b3f-153">Remarks</span></span>

<span data-ttu-id="f5b3f-154">É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-154">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="f5b3f-155">O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-155">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f5b3f-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5b3f-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-157"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f5b3f-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f5b3f-158">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-159"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="f5b3f-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f5b3f-160">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-161"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="f5b3f-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f5b3f-162">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-163"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="f5b3f-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f5b3f-164">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b3f-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f5b3f-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f5b3f-166">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f5b3f-166">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b3f-167"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f5b3f-167"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f5b3f-168">Implementado como <strong>JetGetLogInfoW</strong> (Unicode) e <strong>JetGetLogInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f5b3f-168">Implemented as <strong>JetGetLogInfoW</strong> (Unicode) and <strong>JetGetLogInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f5b3f-169">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f5b3f-169">See Also</span></span>

[<span data-ttu-id="f5b3f-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f5b3f-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f5b3f-171">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f5b3f-171">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f5b3f-172">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="f5b3f-172">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="f5b3f-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="f5b3f-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="f5b3f-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="f5b3f-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="f5b3f-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="f5b3f-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="f5b3f-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="f5b3f-176">JetStopBackup</span></span>](./jetstopbackup-function.md)
