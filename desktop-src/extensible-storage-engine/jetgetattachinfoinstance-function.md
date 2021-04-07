---
description: 'Saiba mais sobre: função JetGetAttachInfoInstance'
title: Função JetGetAttachInfoInstance
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828643"
---
# <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="a745a-103">Função JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="a745a-103">JetGetAttachInfoInstance Function</span></span>


<span data-ttu-id="a745a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a745a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="a745a-105">Função JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="a745a-105">JetGetAttachInfoInstance Function</span></span>

<span data-ttu-id="a745a-106">A função **JetGetAttachInfoInstance** é usada durante um backup iniciado pelo [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) para consultar uma instância para obter os nomes dos arquivos de banco de dados que devem se tornar parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="a745a-106">The **JetGetAttachInfoInstance** function is used during a backup initiated by [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="a745a-107">Somente os bancos de dados que estão conectados à instância no momento usando [JetAttachDatabase](./jetattachdatabase-function.md) serão considerados.</span><span class="sxs-lookup"><span data-stu-id="a745a-107">Only databases that are currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="a745a-108">Esses arquivos podem ser abertos subsequentemente usando [JetOpenFileInstance](./jetopenfileinstance-function.md) e lidos usando [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="a745a-108">These files may subsequently be opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) and read using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="a745a-109">**Windows XP: o JetGetAttachInfoInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a745a-109">**Windows XP:  JetGetAttachInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="a745a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a745a-110">Parameters</span></span>

<span data-ttu-id="a745a-111">*cópia*</span><span class="sxs-lookup"><span data-stu-id="a745a-111">*instance*</span></span>

<span data-ttu-id="a745a-112">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a745a-112">The instance to use for this call.</span></span>

<span data-ttu-id="a745a-113">Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="a745a-113">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="a745a-114">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="a745a-114">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="a745a-115">Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="a745a-115">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="a745a-116">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="a745a-116">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="a745a-117">*szz*</span><span class="sxs-lookup"><span data-stu-id="a745a-117">*szz*</span></span>

<span data-ttu-id="a745a-118">O buffer de saída que recebe a lista de cadeias de caracteres terminadas em nulo que descreve o conjunto de arquivos de banco de dados que deve ser parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="a745a-118">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="a745a-119">A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro.</span><span class="sxs-lookup"><span data-stu-id="a745a-119">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="a745a-120">Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="a745a-120">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="a745a-121">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="a745a-121">*cbMax*</span></span>

<span data-ttu-id="a745a-122">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a745a-122">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="a745a-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="a745a-123">*pcbActual*</span></span>

<span data-ttu-id="a745a-124">Ponteiro para o buffer de saída que recebe a quantidade real de dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a745a-124">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="a745a-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a745a-125">Return Value</span></span>

<span data-ttu-id="a745a-126">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a745a-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a745a-127">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a745a-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a745a-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a745a-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="a745a-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="a745a-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a745a-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a745a-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a745a-131">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a745a-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-132">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="a745a-132">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="a745a-133">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="a745a-133">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="a745a-134">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a745a-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a745a-135">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a745a-135">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a745a-136">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="a745a-136">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-137">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a745a-137">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a745a-138">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="a745a-138">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a745a-139">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a745a-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a745a-140">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="a745a-140">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="a745a-141">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="a745a-141">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="a745a-142"><strong>JetGetAttachInfoInstance</strong> retornará esse erro se o backup atual não for um backup completo.</span><span class="sxs-lookup"><span data-stu-id="a745a-142"><strong>JetGetAttachInfoInstance</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a745a-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a745a-144">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a745a-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a745a-145">Isso pode ocorrer para <strong>JetGetAttachInfoInstance</strong> quando o identificador de instância especificado é inválido (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="a745a-145">This can happen for <strong>JetGetAttachInfoInstance</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a745a-146">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a745a-146">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="a745a-147">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="a745a-147">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-148">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a745a-148">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a745a-149">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="a745a-149">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a745a-150">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a745a-150">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a745a-151">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="a745a-151">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-152">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a745a-152">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a745a-153">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="a745a-153">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a745a-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a745a-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a745a-155">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="a745a-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a745a-156">Em caso de sucesso, as informações solicitadas sobre o conjunto de arquivos de banco de dados que devem ser parte do conjunto de arquivos de backup serão colocadas nos buffers de saída onde forem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a745a-156">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="a745a-157">Em caso de falha, o estado dos buffers de saída é indefinido.</span><span class="sxs-lookup"><span data-stu-id="a745a-157">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="a745a-158">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="a745a-158">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a745a-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="a745a-159">Remarks</span></span>

<span data-ttu-id="a745a-160">É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="a745a-160">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="a745a-161">O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.</span><span class="sxs-lookup"><span data-stu-id="a745a-161">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a745a-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a745a-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a745a-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a745a-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a745a-164">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a745a-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-165"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a745a-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a745a-166">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a745a-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a745a-167"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a745a-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a745a-168">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a745a-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-169"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="a745a-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a745a-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a745a-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a745a-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a745a-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a745a-172">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a745a-172">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a745a-173"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a745a-173"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a745a-174">Implementado como <strong>JetGetAttachInfoInstanceW</strong> (Unicode) e <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a745a-174">Implemented as <strong>JetGetAttachInfoInstanceW</strong> (Unicode) and <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a745a-175">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a745a-175">See Also</span></span>

[<span data-ttu-id="a745a-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a745a-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a745a-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a745a-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a745a-178">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="a745a-178">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="a745a-179">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="a745a-179">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="a745a-180">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="a745a-180">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="a745a-181">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="a745a-181">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="a745a-182">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="a745a-182">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="a745a-183">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="a745a-183">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
