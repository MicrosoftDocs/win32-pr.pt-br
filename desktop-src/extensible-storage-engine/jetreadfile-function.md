---
description: 'Saiba mais sobre: função JetReadFile'
title: Função JetReadFile
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170539"
---
# <a name="jetreadfile-function"></a><span data-ttu-id="e959c-103">Função JetReadFile</span><span class="sxs-lookup"><span data-stu-id="e959c-103">JetReadFile Function</span></span>


<span data-ttu-id="e959c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e959c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfile-function"></a><span data-ttu-id="e959c-105">Função JetReadFile</span><span class="sxs-lookup"><span data-stu-id="e959c-105">JetReadFile Function</span></span>

<span data-ttu-id="e959c-106">A função **JetReadFile** recupera o conteúdo de um arquivo aberto com [JetOpenFile](./jetopenfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="e959c-106">The **JetReadFile** function retrieves the contents of a file opened with [JetOpenFile](./jetopenfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="e959c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e959c-107">Parameters</span></span>

<span data-ttu-id="e959c-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="e959c-108">*hfFile*</span></span>

<span data-ttu-id="e959c-109">O identificador do arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="e959c-109">The handle of the file to be read.</span></span>

<span data-ttu-id="e959c-110">*PV*</span><span class="sxs-lookup"><span data-stu-id="e959c-110">*pv*</span></span>

<span data-ttu-id="e959c-111">Buffer de saída que receberá os dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e959c-111">Output buffer that will receive the file data.</span></span>

<span data-ttu-id="e959c-112">*CB*</span><span class="sxs-lookup"><span data-stu-id="e959c-112">*cb*</span></span>

<span data-ttu-id="e959c-113">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="e959c-113">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="e959c-114">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="e959c-114">*pcbActual*</span></span>

<span data-ttu-id="e959c-115">Recebe a quantidade real de dados de arquivo recuperados.</span><span class="sxs-lookup"><span data-stu-id="e959c-115">Receives the actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="e959c-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e959c-116">Return Value</span></span>

<span data-ttu-id="e959c-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e959c-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e959c-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e959c-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e959c-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e959c-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="e959c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e959c-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e959c-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e959c-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e959c-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e959c-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-123">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="e959c-123">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="e959c-124">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e959c-124">The operation failed because the current external backup has been aborted by a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span> <span data-ttu-id="e959c-125">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e959c-125">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e959c-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e959c-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e959c-127">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e959c-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e959c-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e959c-129">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e959c-130">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e959c-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e959c-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e959c-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e959c-132">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e959c-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="e959c-133">Isso pode ocorrer para <strong>JetReadFile</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="e959c-133">This can happen for <strong>JetReadFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="e959c-134">O identificador de instância especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e959c-134">The specified instance handle is invalid.</span></span> <span data-ttu-id="e959c-135">Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e959c-135">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="e959c-136">O tamanho do buffer de saída não é um múltiplo do tamanho da página do banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="e959c-136">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="e959c-137">Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e959c-137">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="e959c-138">O tamanho do buffer de saída é menor do que três páginas de banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) e essa é a primeira chamada para <strong>JetReadFile</strong> para o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="e959c-138">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) and this is the first call to <strong>JetReadFile</strong> for the specified handle.</span></span> <span data-ttu-id="e959c-139">Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e959c-139">Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-140">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="e959c-140">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="e959c-141">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="e959c-141">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e959c-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e959c-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e959c-143">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="e959c-143">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-144">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="e959c-144">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="e959c-145">A operação falhou porque a corrupção de dados não recuperável foi detectada durante a leitura de uma página de banco de dado de um arquivo de banco de dados ou arquivo de patch de banco</span><span class="sxs-lookup"><span data-stu-id="e959c-145">The operation failed because non-recoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e959c-146">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="e959c-146">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="e959c-147">A operação falhou porque a corrupção de dados não recuperável foi detectada durante a leitura de um arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="e959c-147">The operation failed because non-recoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="e959c-148">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e959c-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e959c-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e959c-150">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="e959c-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e959c-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="e959c-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="e959c-152">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="e959c-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e959c-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e959c-154">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="e959c-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e959c-155">Em caso de sucesso, a próxima parte dos dados do arquivo será lida no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="e959c-155">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="e959c-156">O número real de bytes recuperados também será retornado.</span><span class="sxs-lookup"><span data-stu-id="e959c-156">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="e959c-157">O deslocamento do arquivo no qual a próxima leitura ocorrerá será avançado por esse valor.</span><span class="sxs-lookup"><span data-stu-id="e959c-157">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="e959c-158">Em caso de falha, o estado do buffer de saída é indefinido.</span><span class="sxs-lookup"><span data-stu-id="e959c-158">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="e959c-159">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="e959c-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="e959c-160">No Windows XP e versões posteriores, o backup não será cancelado se ocorrer um erro durante a leitura de um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-160">On Windows XP and later releases, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="e959c-161">No entanto, o backup desse arquivo de banco de dados ainda será cancelado e o identificador correspondente será fechado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e959c-161">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e959c-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="e959c-162">Remarks</span></span>

<span data-ttu-id="e959c-163">Qualquer chamada para **JetReadFile** usando um identificador que já tenha retornado todos os dados no arquivo subjacente (como uma chamada anterior retornou menos bytes do que o tamanho do buffer de saída) sempre terá sucesso, mas retornará zero bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-163">Any call to **JetReadFile** using a handle that has already returned all the data in the underlying file (such as a previous call returned less bytes than the size of the output buffer) will always succeed but return zero bytes of data.</span></span>

<span data-ttu-id="e959c-164">Um buffer de saída grande deve ser usado para maximizar o desempenho do backup.</span><span class="sxs-lookup"><span data-stu-id="e959c-164">A large output buffer should be used to maximize backup performance.</span></span> <span data-ttu-id="e959c-165">Pode ser necessário algum experimento para encontrar a compensação certa entre o consumo de recursos e a taxa de transferência para uma determinada situação.</span><span class="sxs-lookup"><span data-stu-id="e959c-165">Some experimentation may be required to find the right tradeoff between resource consumption and throughput for a given situation.</span></span> <span data-ttu-id="e959c-166">O buffer de saída não deve ser menor que 64 KB em nenhum caso.</span><span class="sxs-lookup"><span data-stu-id="e959c-166">The output buffer should be no smaller than 64KB in any case.</span></span>

<span data-ttu-id="e959c-167">Várias chamadas simultâneas para **JetReadFile** usando o mesmo identificador de arquivo não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="e959c-167">Multiple concurrent calls to **JetReadFile** using the same file handle are not supported.</span></span> <span data-ttu-id="e959c-168">Isso significa que não é possível enfileirar vários buffers para leitura simultânea no mesmo arquivo para obter uma alta taxa de transferência sequencial.</span><span class="sxs-lookup"><span data-stu-id="e959c-168">This means that it is not possible to queue several buffers for read concurrently against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="e959c-169">Um único buffer grande deve ser usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e959c-169">A single large buffer should be used instead.</span></span>

<span data-ttu-id="e959c-170">Se a instância estiver configurada de modo que a depuração de página do banco de dados esteja habilitada (Confira JET_paramZeroDatabaseDuringBackup em parâmetros do sistema), as páginas excluídas serão removidas do banco de dado como um efeito colateral de uma chamada para **JetReadFile** no arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-170">If the instance is configured such that database page scrubbing is enabled (see JET_paramZeroDatabaseDuringBackup in System Parameters) then deleted data will be removed from the database as a side effect of a call to **JetReadFile** against the database file.</span></span>

<span data-ttu-id="e959c-171">É muito importante entender como o backup e a corrupção de dados interagem.</span><span class="sxs-lookup"><span data-stu-id="e959c-171">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="e959c-172">Caso o mecanismo de banco de dados detecte corrupção de dado durante um backup, ele irá falhar o backup do banco de dados afetado ou da instância inteira.</span><span class="sxs-lookup"><span data-stu-id="e959c-172">If the database engine detects data corruption during a backup then it will either fail the backup of the affected database or of the entire instance.</span></span> <span data-ttu-id="e959c-173">Essa é uma decisão de design consciente destinada a proteger contra perda de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-173">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="e959c-174">Se o mecanismo de banco de dados permitisse um backup para ser bem sucedido onde dados corrompidos estavam presentes, é possível que um backup mais antigo e não corrompido possa ser descartado como resultado.</span><span class="sxs-lookup"><span data-stu-id="e959c-174">If the database engine allowed a backup to succeed where data corruption was present then it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="e959c-175">Isso seria desnecessário porque seria possível corrigir os dados corrompidos na instância ao vivo restaurando esse backup e reproduzindo todos os arquivos de log de transações nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-175">This would be unfortunate because it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="e959c-176">Esse cenário de perda de dados zero pressupõe que o log circular não está habilitado (consulte [JET_paramCircularLog](./transaction-log-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="e959c-176">This zero data loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="e959c-177">Também é importante entender que, quando a corrupção de dados está presente, o backup de streaming será o local mais provável que será detectado primeiro.</span><span class="sxs-lookup"><span data-stu-id="e959c-177">It is also important to understand that when data corruption is present streaming backup will be the most likely place that it will first be detected.</span></span> <span data-ttu-id="e959c-178">Esse é o caso porque o backup de streaming é o único processo que examina rotineiramente cada página única do arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-178">This is the case because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="e959c-179">Também é provável que o backup de streaming seja o primeiro processo para detectar os antigos sinais de falha de hardware, como manifestado por erros intermitentes de corrupção de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-179">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors.</span></span> <span data-ttu-id="e959c-180">Isso ocorre devido à quantidade de dados recuperados pelo backup, bem como à velocidade na qual ele é recuperado.</span><span class="sxs-lookup"><span data-stu-id="e959c-180">This is due to the amount of data retrieved by backup as well as the speed at which it is retrieved.</span></span>

<span data-ttu-id="e959c-181">A corrupção de dados é detectada pelo mecanismo de banco de dados com o uso de somas de verificação de bloco.</span><span class="sxs-lookup"><span data-stu-id="e959c-181">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="e959c-182">Essas somas de verificação são definidas imediatamente antes de uma gravação de página de banco de dados e são verificadas em uma página de banco de dados lida.</span><span class="sxs-lookup"><span data-stu-id="e959c-182">These checksums are set just prior to a database page write and are verified on a database page read.</span></span> <span data-ttu-id="e959c-183">Esse esquema permite que o mecanismo de banco de dados Determine que os dados foram corrompidos em algum momento, mas não habilita o mecanismo de banco de dados a determinar a origem desse dano.</span><span class="sxs-lookup"><span data-stu-id="e959c-183">This scheme enables the database engine to determine that data has been corrupted at some point but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="e959c-184">Historicamente, a causa mais predominante desse dano foi Obtida de fontes diferentes do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e959c-184">Historically, the predominant cause of such corruption has been found to come from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e959c-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e959c-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e959c-186"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e959c-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e959c-187">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e959c-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-188"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e959c-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e959c-189">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e959c-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e959c-190"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e959c-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e959c-191">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e959c-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e959c-192"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e959c-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e959c-193">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e959c-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e959c-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e959c-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e959c-195">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e959c-195">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e959c-196">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e959c-196">See Also</span></span>

[<span data-ttu-id="e959c-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e959c-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e959c-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="e959c-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="e959c-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e959c-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e959c-200">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="e959c-200">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="e959c-201">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e959c-201">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="e959c-202">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="e959c-202">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
