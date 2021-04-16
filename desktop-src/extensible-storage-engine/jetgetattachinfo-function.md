---
description: 'Saiba mais sobre: função JetGetAttachInfo'
title: Função JetGetAttachInfo
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa1e51931c11e0fce0b18c0c102c4d54c0b47976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751120"
---
# <a name="jetgetattachinfo-function"></a><span data-ttu-id="12eb8-103">Função JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="12eb8-103">JetGetAttachInfo Function</span></span>


<span data-ttu-id="12eb8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="12eb8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfo-function"></a><span data-ttu-id="12eb8-105">Função JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="12eb8-105">JetGetAttachInfo Function</span></span>

<span data-ttu-id="12eb8-106">A função **JetGetAttachInfo** é usada durante um backup iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar uma instância para obter os nomes dos arquivos de banco de dados que devem se tornar parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="12eb8-106">The **JetGetAttachInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="12eb8-107">Somente os bancos de dados anexados atualmente à instância usando [JetAttachDatabase](./jetattachdatabase-function.md) serão considerados.</span><span class="sxs-lookup"><span data-stu-id="12eb8-107">Only databases currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="12eb8-108">Esses arquivos podem ser abertos subsequentemente usando [JetOpenFile](./jetopenfile-function.md) e lidos usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="12eb8-108">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="12eb8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12eb8-109">Parameters</span></span>

<span data-ttu-id="12eb8-110">*szz*</span><span class="sxs-lookup"><span data-stu-id="12eb8-110">*szz*</span></span>

<span data-ttu-id="12eb8-111">O buffer de saída que recebe a lista de cadeias de caracteres terminadas em nulo que descreve o conjunto de arquivos de banco de dados que deve ser parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="12eb8-111">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="12eb8-112">A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="12eb8-112">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="12eb8-113">Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="12eb8-113">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="12eb8-114">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="12eb8-114">*cbMax*</span></span>

<span data-ttu-id="12eb8-115">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="12eb8-115">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="12eb8-116">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="12eb8-116">*pcbActual*</span></span>

<span data-ttu-id="12eb8-117">Ponteiro para o buffer de saída que recebeu a quantidade real de dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="12eb8-117">Pointer to the output buffer that received the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="12eb8-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="12eb8-118">Return Value</span></span>

<span data-ttu-id="12eb8-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="12eb8-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="12eb8-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="12eb8-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12eb8-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="12eb8-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="12eb8-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="12eb8-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="12eb8-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="12eb8-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="12eb8-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-125">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="12eb8-125">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="12eb8-126">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="12eb8-126">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="12eb8-127">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="12eb8-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="12eb8-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="12eb8-129">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="12eb8-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="12eb8-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="12eb8-131">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="12eb8-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="12eb8-132">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="12eb8-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-133">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="12eb8-133">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="12eb8-134">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="12eb8-134">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="12eb8-135"><strong>JetGetAttachInfo</strong> retornará esse erro se o backup atual não for um backup completo.</span><span class="sxs-lookup"><span data-stu-id="12eb8-135"><strong>JetGetAttachInfo</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="12eb8-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="12eb8-137">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="12eb8-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="12eb8-138">Isso pode ocorrer para <strong>JetGetAttachInfo</strong> quando o identificador de instância especificado é inválido (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="12eb8-138">This can happen for <strong>JetGetAttachInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-139">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="12eb8-139">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="12eb8-140">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="12eb8-140">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="12eb8-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="12eb8-142">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="12eb8-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="12eb8-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="12eb8-144">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="12eb8-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-145">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="12eb8-145">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="12eb8-146">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="12eb8-146">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-147">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="12eb8-147">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="12eb8-148">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="12eb8-148">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="12eb8-149">Em caso de sucesso, as informações solicitadas sobre o conjunto de arquivos de banco de dados que devem ser parte do conjunto de arquivos de backup serão colocadas nos buffers de saída onde forem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="12eb8-149">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="12eb8-150">Em caso de falha, o estado dos buffers de saída é indefinido.</span><span class="sxs-lookup"><span data-stu-id="12eb8-150">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="12eb8-151">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="12eb8-151">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="12eb8-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="12eb8-152">Remarks</span></span>

<span data-ttu-id="12eb8-153">É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="12eb8-153">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="12eb8-154">O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="12eb8-154">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="12eb8-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12eb8-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-156"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="12eb8-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="12eb8-157">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="12eb8-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-158"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="12eb8-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="12eb8-159">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="12eb8-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-160"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="12eb8-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="12eb8-161">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="12eb8-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-162"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="12eb8-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="12eb8-163">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="12eb8-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12eb8-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="12eb8-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="12eb8-165">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="12eb8-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12eb8-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="12eb8-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="12eb8-167">Implementado como <strong>JetGetAttachInfoW</strong> (Unicode) e <strong>JetGetAttachInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="12eb8-167">Implemented as <strong>JetGetAttachInfoW</strong> (Unicode) and <strong>JetGetAttachInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="12eb8-168">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="12eb8-168">See Also</span></span>

[<span data-ttu-id="12eb8-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="12eb8-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="12eb8-170">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="12eb8-170">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="12eb8-171">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="12eb8-171">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="12eb8-172">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="12eb8-172">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="12eb8-173">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="12eb8-173">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="12eb8-174">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="12eb8-174">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="12eb8-175">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="12eb8-175">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="12eb8-176">JetStopService</span><span class="sxs-lookup"><span data-stu-id="12eb8-176">JetStopService</span></span>](./jetstopservice-function.md)
