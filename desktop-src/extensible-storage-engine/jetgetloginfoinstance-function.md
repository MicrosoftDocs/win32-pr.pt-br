---
description: 'Saiba mais sobre: função JetGetLogInfoInstance'
title: Função JetGetLogInfoInstance
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2056859bdce13dfdc28d4cbbf8716925d5bc1cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782532"
---
# <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="e0642-103">Função JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="e0642-103">JetGetLogInfoInstance Function</span></span>


<span data-ttu-id="e0642-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0642-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="e0642-105">Função JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="e0642-105">JetGetLogInfoInstance Function</span></span>

<span data-ttu-id="e0642-106">A função **JetGetLogInfoInstance** é usada durante um backup iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar uma instância para obter os nomes dos arquivos de patch de banco de dados e dos arquivos de log de transações que devem se tornar parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="e0642-106">The **JetGetLogInfoInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="e0642-107">Esses arquivos podem ser abertos subsequentemente usando [JetOpenFile](./jetopenfile-function.md) e lidos usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="e0642-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="e0642-108">**Windows XP: o JetGetLogInfoInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0642-108">**Windows XP:  JetGetLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="e0642-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0642-109">Parameters</span></span>

<span data-ttu-id="e0642-110">*cópia*</span><span class="sxs-lookup"><span data-stu-id="e0642-110">*instance*</span></span>

<span data-ttu-id="e0642-111">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="e0642-111">The instance to use for this call.</span></span>

<span data-ttu-id="e0642-112">Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="e0642-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="e0642-113">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="e0642-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="e0642-114">Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e0642-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="e0642-115">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="e0642-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="e0642-116">*szz*</span><span class="sxs-lookup"><span data-stu-id="e0642-116">*szz*</span></span>

<span data-ttu-id="e0642-117">O buffer de saída que receberá a lista de cadeias de caracteres terminadas em nulo que descreve o conjunto de arquivos de patch de banco de dados e os arquivos de log de transações que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="e0642-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="e0642-118">A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="e0642-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="e0642-119">Cada cadeia de caracteres terminada em NULL é retornada em sequência seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="e0642-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="e0642-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="e0642-120">*cbMax*</span></span>

<span data-ttu-id="e0642-121">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="e0642-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="e0642-122">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="e0642-122">*pcbActual*</span></span>

<span data-ttu-id="e0642-123">Recebe a quantidade real de dados de cadeia de caracteres recebidos no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="e0642-123">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="e0642-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e0642-124">Return Value</span></span>

<span data-ttu-id="e0642-125">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0642-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e0642-126">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e0642-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0642-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0642-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="e0642-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0642-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0642-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e0642-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e0642-130">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e0642-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-131">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="e0642-131">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="e0642-132">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="e0642-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="e0642-133">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e0642-133">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0642-134">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e0642-134">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e0642-135">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e0642-135">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e0642-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e0642-137">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="e0642-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e0642-138">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e0642-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0642-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="e0642-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="e0642-140">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="e0642-140">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="e0642-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> retornará esse erro se houver algum identificador de arquivo pendente criado usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</span><span class="sxs-lookup"><span data-stu-id="e0642-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e0642-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e0642-143">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e0642-143">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="e0642-144">Isso pode ocorrer para <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> quando o identificador de instância especificado é inválido (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="e0642-144">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0642-145">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="e0642-145">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="e0642-146">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="e0642-146">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e0642-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e0642-148">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="e0642-148">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0642-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e0642-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e0642-150">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="e0642-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="e0642-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="e0642-152">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="e0642-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0642-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e0642-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e0642-154">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="e0642-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0642-155">Em caso de sucesso, as informações solicitadas sobre o conjunto de arquivos de patch de banco de dados e arquivos de log de transações que devem ser parte do conjunto de arquivos de backup serão colocadas nos buffers de saída, onde fornecido.</span><span class="sxs-lookup"><span data-stu-id="e0642-155">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="e0642-156">O computador de estado de backup será avançado de modo que o backup de arquivos de banco de dados não seja mais permitido.</span><span class="sxs-lookup"><span data-stu-id="e0642-156">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="e0642-157">Somente arquivos de patch de banco de dados e arquivos de log de transações podem ser abertos para backup além desse ponto.</span><span class="sxs-lookup"><span data-stu-id="e0642-157">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="e0642-158">Em caso de falha, o estado dos buffers de saída é indefinido.</span><span class="sxs-lookup"><span data-stu-id="e0642-158">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="e0642-159">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="e0642-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e0642-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0642-160">Remarks</span></span>

<span data-ttu-id="e0642-161">É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="e0642-161">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="e0642-162">O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="e0642-162">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e0642-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0642-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0642-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e0642-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0642-165">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0642-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-166"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e0642-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0642-167">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e0642-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0642-168"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e0642-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0642-169">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e0642-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-170"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e0642-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e0642-171">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e0642-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0642-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e0642-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e0642-173">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e0642-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0642-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e0642-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e0642-175">Implementado como <strong>JetGetLogInfoInstanceW</strong> (Unicode) e <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e0642-175">Implemented as <strong>JetGetLogInfoInstanceW</strong> (Unicode) and <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e0642-176">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e0642-176">See Also</span></span>

[<span data-ttu-id="e0642-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e0642-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e0642-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e0642-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e0642-179">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="e0642-179">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="e0642-180">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="e0642-180">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="e0642-181">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="e0642-181">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="e0642-182">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="e0642-182">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="e0642-183">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="e0642-183">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="e0642-184">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e0642-184">JetStopService</span></span>](./jetstopservice-function.md)
