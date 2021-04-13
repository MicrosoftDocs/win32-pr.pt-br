---
description: 'Saiba mais sobre: função JetReadFileInstance'
title: Função JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501291"
---
# <a name="jetreadfileinstance-function"></a><span data-ttu-id="917c3-103">Função JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="917c3-103">JetReadFileInstance Function</span></span>


<span data-ttu-id="917c3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="917c3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfileinstance-function"></a><span data-ttu-id="917c3-105">Função JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="917c3-105">JetReadFileInstance Function</span></span>

<span data-ttu-id="917c3-106">A função **JetReadFileInstance** recupera o conteúdo de um arquivo aberto com a função [JetOpenFileInstance](./jetopenfileinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="917c3-106">The **JetReadFileInstance** function retrieves the contents of a file opened with the [JetOpenFileInstance](./jetopenfileinstance-function.md) function.</span></span>

<span data-ttu-id="917c3-107">**Windows XP**: o   **JetReadFileInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="917c3-107">**Windows XP**:   **JetReadFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a><span data-ttu-id="917c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="917c3-108">Parameters</span></span>

<span data-ttu-id="917c3-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="917c3-109">*instance*</span></span>

<span data-ttu-id="917c3-110">A instância a ser usada para uma chamada de API específica.</span><span class="sxs-lookup"><span data-stu-id="917c3-110">The instance to use for a particular API call.</span></span>

<span data-ttu-id="917c3-111">Observe que para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="917c3-111">Note that for Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="917c3-112">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="917c3-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="917c3-113">Para o Windows XP e versões posteriores, você pode chamar a variante de API que não aceita esse parâmetro somente quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000) nos casos em que há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="917c3-113">For Windows XP and later releases, you can call the API variant that does not accept this parameter only when the engine is in legacy mode (Windows 2000 compatibility mode) in cases where only one instance is supported.</span></span> <span data-ttu-id="917c3-114">Caso contrário, a operação falhará e retornará o erro de JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="917c3-114">Otherwise, the operation will fail and return the JET_errRunningInMultiInstanceMode error.</span></span>

<span data-ttu-id="917c3-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="917c3-115">*hfFile*</span></span>

<span data-ttu-id="917c3-116">O identificador do arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="917c3-116">The handle of the file to be read.</span></span>

<span data-ttu-id="917c3-117">*PV*</span><span class="sxs-lookup"><span data-stu-id="917c3-117">*pv*</span></span>

<span data-ttu-id="917c3-118">O buffer de saída que receberá os dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="917c3-118">The output buffer that will receive the file data.</span></span>

<span data-ttu-id="917c3-119">*CB*</span><span class="sxs-lookup"><span data-stu-id="917c3-119">*cb*</span></span>

<span data-ttu-id="917c3-120">O tamanho máximo, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="917c3-120">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="917c3-121">*pcb*</span><span class="sxs-lookup"><span data-stu-id="917c3-121">*pcb*</span></span>

<span data-ttu-id="917c3-122">A quantidade real de dados de arquivo recuperados.</span><span class="sxs-lookup"><span data-stu-id="917c3-122">The actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="917c3-123">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="917c3-123">Return Value</span></span>

<span data-ttu-id="917c3-124">Essa função facilita o retorno de quaisquer [JET_ERR](./jet-err.md) tipos de dados que são definidos na API do ESE (mecanismo de armazenamento extensível).</span><span class="sxs-lookup"><span data-stu-id="917c3-124">This function facilitates the return of any [JET_ERR](./jet-err.md) data types that are defined in the Extensible Storage Engine (ESE) API.</span></span> <span data-ttu-id="917c3-125">Para obter mais informações sobre erros do JET, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="917c3-125">For more information about JET errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="917c3-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="917c3-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="917c3-127">Significado</span><span class="sxs-lookup"><span data-stu-id="917c3-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="917c3-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="917c3-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="917c3-129">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="917c3-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="917c3-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="917c3-131">A operação falhou porque o backup externo atual foi anulado por uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="917c3-131">The operation failed because the current external backup has been aborted by a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span> <span data-ttu-id="917c3-132">Esse erro será retornado somente pelo Windows XP e por versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="917c3-132">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917c3-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="917c3-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="917c3-134">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="917c3-134">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="917c3-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="917c3-136">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="917c3-136">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error requiring that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="917c3-137">Esse erro será retornado somente pelo Windows XP e por versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="917c3-137">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917c3-138">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="917c3-138">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="917c3-139">Um dos parâmetros especificados continha um valor inesperado ou um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="917c3-139">One of the specified parameters contained either an unexpected value or a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="917c3-140">Isso pode acontecer para a função <strong>JetReadFileInstance</strong> quando ocorrer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="917c3-140">This can happen for the <strong>JetReadFileInstance</strong> function when any of the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="917c3-141">O identificador de instância especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="917c3-141">The specified instance handle is invalid.</span></span> <span data-ttu-id="917c3-142">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="917c3-142">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="917c3-143">O tamanho do buffer de saída não é um múltiplo do tamanho da página do banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="917c3-143">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="917c3-144">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="917c3-144">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="917c3-145">O tamanho do buffer de saída é menor do que três páginas de banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), e essa é a primeira chamada para a função <strong>JetReadFileInstance</strong> para o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="917c3-145">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), and this is the first call to the <strong>JetReadFileInstance</strong> function for the specified handle.</span></span> <span data-ttu-id="917c3-146">Windows XP e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="917c3-146">Windows XP and later Windows versions.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-147">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="917c3-147">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="917c3-148">A operação falhou porque o corrompimento de dados irrecuperáveis foi detectado durante a leitura de um arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="917c3-148">The operation failed because unrecoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="917c3-149">Esse erro será retornado somente pelo Windows XP e por versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="917c3-149">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917c3-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="917c3-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="917c3-151">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="917c3-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="917c3-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="917c3-153">Não é possível concluir a operação porque a instância associada a esta sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="917c3-153">It is not possible to complete the operation because the instance associated with this session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917c3-154">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="917c3-154">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="917c3-155">A operação falhou porque o corrompimento de dados irrecuperáveis foi detectado durante a leitura de uma página de banco de dado a partir de um arquivo de dados ou arquivo de patch de banco</span><span class="sxs-lookup"><span data-stu-id="917c3-155">The operation failed because unrecoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="917c3-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="917c3-157">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada a esta sessão.</span><span class="sxs-lookup"><span data-stu-id="917c3-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917c3-158">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="917c3-158">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="917c3-159">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em um caso em que apenas uma instância tem suporte, mas várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="917c3-159">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) in a case where only one instance is supported but multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="917c3-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="917c3-161">Não é possível concluir a operação porque a instância associada a esta sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="917c3-161">It is not possible to complete the operation because the instance associated with this session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="917c3-162">Em caso de sucesso, a próxima parte dos dados do arquivo será lida no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="917c3-162">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="917c3-163">O número real de bytes recuperados também será retornado.</span><span class="sxs-lookup"><span data-stu-id="917c3-163">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="917c3-164">O deslocamento do arquivo no qual a próxima leitura ocorrerá será avançado por esse valor.</span><span class="sxs-lookup"><span data-stu-id="917c3-164">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="917c3-165">Em caso de falha, o estado do buffer de saída é indefinido.</span><span class="sxs-lookup"><span data-stu-id="917c3-165">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="917c3-166">A falha resultará no cancelamento de todo o processo de backup para a instância atual.</span><span class="sxs-lookup"><span data-stu-id="917c3-166">The failure will result in the cancellation of the entire backup process for the current instance.</span></span> <span data-ttu-id="917c3-167">No Windows XP e versões posteriores do Windows, o backup não será cancelado se ocorrer um erro durante a leitura de um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="917c3-167">In Windows XP and later Windows versions, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="917c3-168">No entanto, o backup desse arquivo de banco de dados ainda será cancelado e o identificador correspondente será fechado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="917c3-168">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="917c3-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="917c3-169">Remarks</span></span>

<span data-ttu-id="917c3-170">Qualquer chamada para a função **JetReadFileInstance** feita usando um identificador que já retornou todos os dados no arquivo subjacente (por exemplo, se uma chamada anterior retornou menos bytes do que o tamanho do buffer de saída) sempre terá sucesso, mas retornará zero bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="917c3-170">Any call to the **JetReadFileInstance** function made by using a handle that has already returned all the data in the underlying file (such as if a previous call returned fewer bytes than the size of the output buffer) will always succeed but will return zero bytes of data.</span></span>

<span data-ttu-id="917c3-171">Você deve usar um buffer de saída grande para maximizar o desempenho do backup.</span><span class="sxs-lookup"><span data-stu-id="917c3-171">You should use a large output buffer to maximize backup performance.</span></span> <span data-ttu-id="917c3-172">Talvez seja necessário experimentar para encontrar a desvantagem ideal entre o consumo de recursos e a taxa de transferência para uma situação específica.</span><span class="sxs-lookup"><span data-stu-id="917c3-172">You might need to experiment to find the optimal tradeoff between resource consumption and throughput for a particular situation.</span></span> <span data-ttu-id="917c3-173">Em qualquer caso, o buffer de saída não deve ser menor que 64 KB.</span><span class="sxs-lookup"><span data-stu-id="917c3-173">In any case, the output buffer should be no smaller than 64 KB.</span></span> <span data-ttu-id="917c3-174">O ponteiro que você passa para **JetReadFileInstance** deve ser alinhado com um limite de página de memória (4 KB ou 8 KB).</span><span class="sxs-lookup"><span data-stu-id="917c3-174">The pointer that you pass to **JetReadFileInstance** must be aligned with a memory page boundary (either 4 KB or 8 KB).</span></span> <span data-ttu-id="917c3-175">Você pode fazer isso chamando a função do **VirtualAlloc** .</span><span class="sxs-lookup"><span data-stu-id="917c3-175">You can do this by calling the **VirtualAlloc** function.</span></span>

<span data-ttu-id="917c3-176">Várias chamadas simultâneas para **JetReadFileInstance** feitas usando o mesmo identificador de arquivo não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="917c3-176">Multiple concurrent calls to **JetReadFileInstance** made by using the same file handle are not supported.</span></span> <span data-ttu-id="917c3-177">Isso significa que não é possível enfileirar vários buffers para leitura simultânea no mesmo arquivo para obter uma alta taxa de transferência sequencial.</span><span class="sxs-lookup"><span data-stu-id="917c3-177">This means that it is not possible to queue several buffers for concurrent reading against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="917c3-178">Em vez disso, você deve usar um único buffer grande.</span><span class="sxs-lookup"><span data-stu-id="917c3-178">You should use a single large buffer instead.</span></span>

<span data-ttu-id="917c3-179">Se você tiver configurado uma instância específica, de modo que a depuração de página do banco de dados esteja habilitada (consulte o parâmetro [JET_paramCircularLog](./transaction-log-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md)), os dados excluídos serão removidos do banco de dado como um efeito colateral de uma chamada para **JetReadFileInstance** no arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="917c3-179">If you have configured a particular instance such that database page scrubbing is enabled (see the [JET_paramCircularLog](./transaction-log-parameters.md) parameter in [System Parameters](./extensible-storage-engine-system-parameters.md)), deleted data will be removed from the database as a side-effect of a call to **JetReadFileInstance** against the database file.</span></span>

<span data-ttu-id="917c3-180">É muito importante entender como o backup e a corrupção de dados interagem.</span><span class="sxs-lookup"><span data-stu-id="917c3-180">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="917c3-181">Se o mecanismo de banco de dados detectar corrupção de dado durante um backup, ele irá falhar o backup do banco de dados afetado ou da instância inteira.</span><span class="sxs-lookup"><span data-stu-id="917c3-181">If the database engine detects data corruption during a backup, it will fail the backup of either the affected database or the entire instance.</span></span> <span data-ttu-id="917c3-182">Essa é uma decisão de design consciente destinada a proteger contra perda de dados.</span><span class="sxs-lookup"><span data-stu-id="917c3-182">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="917c3-183">Se o mecanismo de banco de dados permitisse um backup para ter êxito onde os dados estão corrompidos, é possível que um backup mais antigo e não corrompido possa ser descartado como resultado.</span><span class="sxs-lookup"><span data-stu-id="917c3-183">If the database engine allowed a backup to succeed where data corruption was present, it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="917c3-184">Isso seria desnecessário, pois seria possível corrigir os dados corrompidos na instância dinâmica restaurando esse backup e reproduzindo todos os arquivos de log de transações nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="917c3-184">This would be unfortunate because then it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="917c3-185">Esse cenário de perda de dados sem zero pressupõe que o log circular não está habilitado (consulte [JET_paramCircularLog](./transaction-log-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="917c3-185">This zero-data-loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="917c3-186">Também é importante entender que os casos de corrupção de dados geralmente são detectados primeiro durante o backup de streaming.</span><span class="sxs-lookup"><span data-stu-id="917c3-186">It is also important to understand that cases of data corruption are usually first detected during streaming backup.</span></span> <span data-ttu-id="917c3-187">Isso ocorre porque o backup de streaming é o único processo que examina rotineiramente cada página única do arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="917c3-187">This is because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="917c3-188">Também é provável que o backup de streaming seja o primeiro processo para detectar os antigos sinais de falha de hardware, como manifestado por erros intermitentes de corrupção de dados, devido à quantidade de dados recuperados pelo backup e à velocidade em que esses dados são recuperados.</span><span class="sxs-lookup"><span data-stu-id="917c3-188">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors, because of both the amount of data retrieved by backup and the speed at which that data is retrieved.</span></span>

<span data-ttu-id="917c3-189">A corrupção de dados é detectada pelo mecanismo de banco de dados com o uso de somas de verificação de bloco.</span><span class="sxs-lookup"><span data-stu-id="917c3-189">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="917c3-190">Essas somas de verificação são definidas imediatamente antes da gravação de uma página de banco de dados e são verificados em uma página de banco de dados lida.</span><span class="sxs-lookup"><span data-stu-id="917c3-190">These checksums are set just before a database page write and are verified on a database page read.</span></span> <span data-ttu-id="917c3-191">Esse esquema permite que o mecanismo de banco de dados Determine que os dados foram corrompidos em algum momento, mas não habilita o mecanismo de banco de dados para determinar a origem desse dano.</span><span class="sxs-lookup"><span data-stu-id="917c3-191">This scheme enables the database engine to determine that data has been corrupted at some point, but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="917c3-192">Historicamente, as instâncias desse tipo de corrupção de dados se originaram de fontes diferentes do mecanismo de banco de dados em si.</span><span class="sxs-lookup"><span data-stu-id="917c3-192">Historically, instances of such data corruption have originated from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="917c3-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="917c3-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="917c3-194">Cliente</span><span class="sxs-lookup"><span data-stu-id="917c3-194">Client</span></span></p></td>
<td><p><span data-ttu-id="917c3-195">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="917c3-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-196">Servidor</span><span class="sxs-lookup"><span data-stu-id="917c3-196">Server</span></span></p></td>
<td><p><span data-ttu-id="917c3-197">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="917c3-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917c3-198">parâmetro</span><span class="sxs-lookup"><span data-stu-id="917c3-198">Header</span></span></p></td>
<td><p><span data-ttu-id="917c3-199">É declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="917c3-199">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917c3-200">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="917c3-200">Library</span></span></p></td>
<td><p><span data-ttu-id="917c3-201">Usa ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="917c3-201">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917c3-202">DLL</span><span class="sxs-lookup"><span data-stu-id="917c3-202">DLL</span></span></p></td>
<td><p><span data-ttu-id="917c3-203">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="917c3-203">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="917c3-204">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="917c3-204">See Also</span></span>

[<span data-ttu-id="917c3-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="917c3-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="917c3-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="917c3-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="917c3-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="917c3-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="917c3-208">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="917c3-208">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="917c3-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="917c3-209">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="917c3-210">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="917c3-210">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
