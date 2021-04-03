---
description: 'Saiba mais sobre: função JetRestore'
title: Função JetRestore
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ed164bb6775150f9745cb0e6d9b158a5f03f146
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930781"
---
# <a name="jetrestore-function"></a><span data-ttu-id="6c195-103">Função JetRestore</span><span class="sxs-lookup"><span data-stu-id="6c195-103">JetRestore Function</span></span>


<span data-ttu-id="6c195-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6c195-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore-function"></a><span data-ttu-id="6c195-105">Função JetRestore</span><span class="sxs-lookup"><span data-stu-id="6c195-105">JetRestore Function</span></span>

<span data-ttu-id="6c195-106">A função **JetRestore** restaura e recupera um backup de streaming de uma instância, incluindo todos os bancos de dados anexados.</span><span class="sxs-lookup"><span data-stu-id="6c195-106">The **JetRestore** function restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="6c195-107">Essa função é usada principalmente para compatibilidade com versões anteriores com o Windows 2000 e com mecanismos de banco de dados anterior, em que apenas uma instância de um banco de dados é permitida.</span><span class="sxs-lookup"><span data-stu-id="6c195-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="6c195-108">Nesse caso, a instância ativa é a instância que é restaurada.</span><span class="sxs-lookup"><span data-stu-id="6c195-108">In this case, the active instance is the instance that is restored.</span></span> <span data-ttu-id="6c195-109">Com **JetRestore**, o local dos bancos de dados restaurados não pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="6c195-109">With **JetRestore**, the location for the restored databases cannot be specified.</span></span>

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="6c195-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c195-110">Parameters</span></span>

<span data-ttu-id="6c195-111">*sz*</span><span class="sxs-lookup"><span data-stu-id="6c195-111">*sz*</span></span>

<span data-ttu-id="6c195-112">A pasta onde o backup está localizado.</span><span class="sxs-lookup"><span data-stu-id="6c195-112">The folder where the backup is located.</span></span> <span data-ttu-id="6c195-113">O backup deve ter sido gerado usando a função [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6c195-113">The backup should have been generated using the [JetBackup](./jetbackup-function.md) function.</span></span>

<span data-ttu-id="6c195-114">*PFN*</span><span class="sxs-lookup"><span data-stu-id="6c195-114">*pfn*</span></span>

<span data-ttu-id="6c195-115">O ponteiro opcional para a função que será chamada como informações de notificação sobre o progresso da operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="6c195-115">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="6c195-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6c195-116">Return Value</span></span>

<span data-ttu-id="6c195-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c195-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6c195-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6c195-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c195-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6c195-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="6c195-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c195-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c195-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6c195-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6c195-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6c195-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c195-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="6c195-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="6c195-124">A operação falhou porque o mecanismo já foi inicializado para esta instância.</span><span class="sxs-lookup"><span data-stu-id="6c195-124">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c195-125">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="6c195-125">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="6c195-126">O conjunto de arquivos de log do conjunto de backup e do caminho de log atual não coincidem.</span><span class="sxs-lookup"><span data-stu-id="6c195-126">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c195-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6c195-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6c195-128">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6c195-128">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c195-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6c195-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="6c195-130">A operação falhou porque alguns caminhos fornecidos são inválidos (o caminho de backup, o caminho de destino, o log ou o caminho do sistema para a instância).</span><span class="sxs-lookup"><span data-stu-id="6c195-130">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c195-131">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="6c195-131">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="6c195-132">A operação falhou porque o mecanismo está configurado para usar um tamanho de página de banco de dados (usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) que não corresponde ao tamanho da página do banco de dados usado para criar os arquivos de log de transações ou os bancos de dados associados aos arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="6c195-132">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c195-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6c195-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="6c195-134">A operação falhou porque o modo de instância única implícito de parâmetros (modo de compatibilidade do Windows 2000) e o mecanismo já estão no modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="6c195-134">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c195-135">Em caso de êxito, os arquivos de banco de dados do conjunto de backup serão restaurados para seu local e a recuperação será executada de modo que os bancos estejam em um estado de consistência transacional limpo.</span><span class="sxs-lookup"><span data-stu-id="6c195-135">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="6c195-136">A recuperação reproduzirá os arquivos de log do conjunto de backup e dos arquivos de log do caminho de log, se esses arquivos existirem.</span><span class="sxs-lookup"><span data-stu-id="6c195-136">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="6c195-137">Essa recuperação resultará em alterações no arquivo de ponto de verificação, nos arquivos de log de transações e em qualquer banco de dados referenciado por esses arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="6c195-137">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="6c195-138">Em caso de falha, a instância permanece em um estado não inicializado.</span><span class="sxs-lookup"><span data-stu-id="6c195-138">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="6c195-139">O estado dos arquivos de log de transações e quaisquer bancos de dados referenciados por esses arquivos de log de transações provavelmente serão alterados na tentativa de inicializar a restauração e recuperar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="6c195-139">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6c195-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c195-140">Remarks</span></span>

<span data-ttu-id="6c195-141">O processo de recuperação reconstruirá os bancos de dados anexados à instância durante o backup e salvará as alterações de volta nos arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6c195-141">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="6c195-142">O resultado será os bancos de dados que são consistentes com a transação.</span><span class="sxs-lookup"><span data-stu-id="6c195-142">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="6c195-143">Se possível, ele também será salvo no banco de dados as alterações feitas desde que o backup foi feito até a alteração mais recente encontrada nos logs de transações.</span><span class="sxs-lookup"><span data-stu-id="6c195-143">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="6c195-144">Isso seria possível se os logs de transações gerados desde que o backup foi feito ainda estiverem presentes no diretório de log de transações.</span><span class="sxs-lookup"><span data-stu-id="6c195-144">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="6c195-145">Observe que, se o log circular tiver sido habilitado para a instância, os logs de transação gerados serão reutilizados, de modo que a recuperação poderá salvar as alterações que foram realizadas até o momento do backup.</span><span class="sxs-lookup"><span data-stu-id="6c195-145">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="6c195-146">Em qualquer caso, é possível que esse processo demore algum tempo se o número de arquivos de log de transações a serem reproduzidos em relação aos bancos de dados for grande.</span><span class="sxs-lookup"><span data-stu-id="6c195-146">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="6c195-147">As funções **JetRestore** devem ser chamadas em uma instância antes que [JetInit](./jetinit-function.md) seja chamado para essa instância.</span><span class="sxs-lookup"><span data-stu-id="6c195-147">**JetRestore** functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="6c195-148">Como, durante a recuperação, um número significativo de páginas de banco de dados e logs de transações serão usados, há uma série completa de erros que podem ser retornados por essas funções.</span><span class="sxs-lookup"><span data-stu-id="6c195-148">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="6c195-149">Esses erros podem ser de falhas temporárias de alocação de recursos, como Jet_errOutOfMemory a erros que representam as corrupções físicas, como JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="6c195-149">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="6c195-150">Esses erros são quase sempre causados por problemas de hardware e, portanto, não podem ser evitados.</span><span class="sxs-lookup"><span data-stu-id="6c195-150">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="6c195-151">O ingerenciamento de arquivos será manifestado com mais frequência como JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="6c195-151">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="6c195-152">Esses erros são impedidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c195-152">These errors are preventable by the application.</span></span> <span data-ttu-id="6c195-153">O aplicativo deve ter cuidado para proteger o repositório desses arquivos contra a manipulação por forças externas, como o usuário ou outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6c195-153">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="6c195-154">Se o aplicativo desejar destruir uma instância inteiramente, todos os arquivos associados à instância deverão ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="6c195-154">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="6c195-155">Isso inclui o arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância.</span><span class="sxs-lookup"><span data-stu-id="6c195-155">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="6c195-156">As diferentes etapas da recuperação terão entradas de log de eventos geradas, incluindo o progresso da reprodução do log de transações e o resultado final da restauração.</span><span class="sxs-lookup"><span data-stu-id="6c195-156">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6c195-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c195-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c195-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6c195-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6c195-159">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6c195-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c195-160"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6c195-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c195-161">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6c195-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c195-162"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6c195-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6c195-163">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6c195-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c195-164"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6c195-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6c195-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6c195-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c195-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6c195-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6c195-167">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6c195-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c195-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6c195-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6c195-169">Implementado como <strong>JetRestoreW</strong> (Unicode) e <strong>JetRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6c195-169">Implemented as <strong>JetRestoreW</strong> (Unicode) and <strong>JetRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6c195-170">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6c195-170">See Also</span></span>

[<span data-ttu-id="6c195-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6c195-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6c195-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6c195-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6c195-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6c195-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="6c195-174">JetBackup</span><span class="sxs-lookup"><span data-stu-id="6c195-174">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="6c195-175">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="6c195-175">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="6c195-176">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="6c195-176">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="6c195-177">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6c195-177">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
