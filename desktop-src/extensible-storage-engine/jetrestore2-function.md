---
description: 'Saiba mais sobre: função JetRestore2'
title: Função JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790589"
---
# <a name="jetrestore2-function"></a><span data-ttu-id="a44f0-103">Função JetRestore2</span><span class="sxs-lookup"><span data-stu-id="a44f0-103">JetRestore2 Function</span></span>


<span data-ttu-id="a44f0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a44f0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore2-function"></a><span data-ttu-id="a44f0-105">Função JetRestore2</span><span class="sxs-lookup"><span data-stu-id="a44f0-105">JetRestore2 Function</span></span>

<span data-ttu-id="a44f0-106">O **JetRestore2** restaura e recupera um backup de streaming de uma instância, incluindo todos os bancos de dados anexados.</span><span class="sxs-lookup"><span data-stu-id="a44f0-106">The **JetRestore2** restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="a44f0-107">Essa função é usada principalmente para compatibilidade com versões anteriores com o Windows 2000 e com mecanismos de banco de dados anterior, em que apenas uma instância de um banco de dados é permitida.</span><span class="sxs-lookup"><span data-stu-id="a44f0-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="a44f0-108">Nesse caso, a instância ativa é a instância que é restaurada.</span><span class="sxs-lookup"><span data-stu-id="a44f0-108">In this case, the active instance is the instance that is restored.</span></span>

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="a44f0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a44f0-109">Parameters</span></span>

<span data-ttu-id="a44f0-110">*sz*</span><span class="sxs-lookup"><span data-stu-id="a44f0-110">*sz*</span></span>

<span data-ttu-id="a44f0-111">A pasta onde o backup está localizado.</span><span class="sxs-lookup"><span data-stu-id="a44f0-111">The folder where the backup is located.</span></span> <span data-ttu-id="a44f0-112">O backup deve ter sido gerado usando as APIs [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a44f0-112">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="a44f0-113">*szDest*</span><span class="sxs-lookup"><span data-stu-id="a44f0-113">*szDest*</span></span>

<span data-ttu-id="a44f0-114">Nome da pasta em que os arquivos de banco de dados do conjunto de backup serão copiados e recuperados.</span><span class="sxs-lookup"><span data-stu-id="a44f0-114">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="a44f0-115">Se isso for definido como NULL (que é o caso para o [JetRestore](./jetrestore-function.md)herdado), os arquivos de banco de dados serão copiados e recuperados em seu local original.</span><span class="sxs-lookup"><span data-stu-id="a44f0-115">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="a44f0-116">*PFN*</span><span class="sxs-lookup"><span data-stu-id="a44f0-116">*pfn*</span></span>

<span data-ttu-id="a44f0-117">O ponteiro opcional para a função que será chamada como informações de notificação sobre o progresso da operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="a44f0-117">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="a44f0-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a44f0-118">Return Value</span></span>

<span data-ttu-id="a44f0-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a44f0-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a44f0-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a44f0-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a44f0-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a44f0-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="a44f0-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="a44f0-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44f0-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a44f0-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a44f0-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a44f0-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44f0-125">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="a44f0-125">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="a44f0-126">A operação falhou porque o mecanismo já foi inicializado para esta instância.</span><span class="sxs-lookup"><span data-stu-id="a44f0-126">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44f0-127">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="a44f0-127">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="a44f0-128">O conjunto de arquivos de log do conjunto de backup e do caminho de log atual não coincidem.</span><span class="sxs-lookup"><span data-stu-id="a44f0-128">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44f0-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a44f0-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a44f0-130">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a44f0-130">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a44f0-131">Esse erro será retornado por <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> quando o mecanismo estiver no modo de várias instâncias e pinstance se referir a uma instância inválida do Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a44f0-131">This error will be returned by <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44f0-132">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="a44f0-132">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="a44f0-133">A operação falhou porque alguns caminhos fornecidos são inválidos (o caminho de backup, o caminho de destino, o log ou o caminho do sistema para a instância).</span><span class="sxs-lookup"><span data-stu-id="a44f0-133">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44f0-134">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="a44f0-134">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="a44f0-135">A operação falhou porque o mecanismo está configurado para usar um tamanho de página de banco de dados (usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) que não corresponde ao tamanho da página do banco de dados usado para criar os arquivos de log de transações ou os bancos de dados associados aos arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="a44f0-135">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44f0-136">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a44f0-136">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a44f0-137">A operação falhou porque o modo de instância única implícito de parâmetros (modo de compatibilidade do Windows 2000) e o mecanismo já estão no modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="a44f0-137">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a44f0-138">Em caso de êxito, os arquivos de banco de dados do conjunto de backup serão restaurados para seu local e a recuperação será executada de modo que os bancos estejam em um estado de consistência transacional limpo.</span><span class="sxs-lookup"><span data-stu-id="a44f0-138">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="a44f0-139">A recuperação reproduzirá os arquivos de log do conjunto de backup e dos arquivos de log do caminho de log, se esses arquivos existirem.</span><span class="sxs-lookup"><span data-stu-id="a44f0-139">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="a44f0-140">Essa recuperação resultará em alterações no arquivo de ponto de verificação, nos arquivos de log de transações e em qualquer banco de dados referenciado por esses arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="a44f0-140">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="a44f0-141">Em caso de falha, a instância permanece em um estado não inicializado.</span><span class="sxs-lookup"><span data-stu-id="a44f0-141">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="a44f0-142">O estado dos arquivos de log de transações e quaisquer bancos de dados referenciados por esses arquivos de log de transações provavelmente serão alterados na tentativa de inicializar a restauração e recuperar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="a44f0-142">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a44f0-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="a44f0-143">Remarks</span></span>

<span data-ttu-id="a44f0-144">O processo de recuperação reconstruirá os bancos de dados anexados à instância durante o backup e salvará as alterações de volta nos arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a44f0-144">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="a44f0-145">O resultado será os bancos de dados que são consistentes com a transação.</span><span class="sxs-lookup"><span data-stu-id="a44f0-145">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="a44f0-146">Se possível, ele também será salvo no banco de dados as alterações feitas desde que o backup foi feito até a alteração mais recente encontrada nos logs de transações.</span><span class="sxs-lookup"><span data-stu-id="a44f0-146">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="a44f0-147">Isso seria possível se os logs de transações gerados desde que o backup foi feito ainda estiverem presentes no diretório de log de transações.</span><span class="sxs-lookup"><span data-stu-id="a44f0-147">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="a44f0-148">Observe que, se o log circular tiver sido habilitado para a instância, os logs de transação gerados serão reutilizados, de modo que a recuperação poderá salvar as alterações que foram realizadas até o momento do backup.</span><span class="sxs-lookup"><span data-stu-id="a44f0-148">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="a44f0-149">Em qualquer caso, é possível que esse processo demore algum tempo se o número de arquivos de log de transações a serem reproduzidos em relação aos bancos de dados for grande.</span><span class="sxs-lookup"><span data-stu-id="a44f0-149">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="a44f0-150">As funções [JetRestore](./jetrestore-function.md) devem ser chamadas em uma instância antes que [JetInit](./jetinit-function.md) seja chamado para essa instância.</span><span class="sxs-lookup"><span data-stu-id="a44f0-150">[JetRestore](./jetrestore-function.md) functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="a44f0-151">Como, durante a recuperação, um número significativo de páginas de banco de dados e logs de transações serão usados, há uma série completa de erros que podem ser retornados por essas funções.</span><span class="sxs-lookup"><span data-stu-id="a44f0-151">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="a44f0-152">Esses erros podem ser de falhas temporárias de alocação de recursos, como Jet_errOutOfMemory a erros que representam as corrupções físicas, como JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="a44f0-152">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="a44f0-153">Esses erros são quase sempre causados por problemas de hardware e, portanto, não podem ser evitados.</span><span class="sxs-lookup"><span data-stu-id="a44f0-153">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="a44f0-154">O ingerenciamento de arquivos será manifestado com mais frequência como JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="a44f0-154">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="a44f0-155">Esses erros são impedidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a44f0-155">These errors are preventable by the application.</span></span> <span data-ttu-id="a44f0-156">O aplicativo deve ter cuidado para proteger o repositório desses arquivos contra a manipulação por forças externas, como o usuário ou outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a44f0-156">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="a44f0-157">Se o aplicativo desejar destruir uma instância inteiramente, todos os arquivos associados à instância deverão ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="a44f0-157">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="a44f0-158">Isso inclui o arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância.</span><span class="sxs-lookup"><span data-stu-id="a44f0-158">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="a44f0-159">As diferentes etapas da recuperação terão entradas de log de eventos geradas, incluindo o progresso da reprodução do log de transações e o resultado final da restauração.</span><span class="sxs-lookup"><span data-stu-id="a44f0-159">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a44f0-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a44f0-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44f0-161"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a44f0-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a44f0-162">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a44f0-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44f0-163"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a44f0-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a44f0-164">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a44f0-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44f0-165"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a44f0-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a44f0-166">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a44f0-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44f0-167"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="a44f0-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a44f0-168">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a44f0-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44f0-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a44f0-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a44f0-170">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a44f0-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44f0-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a44f0-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a44f0-172">Implementado como <strong>JetRestore2W</strong> (Unicode) e <strong>JetRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a44f0-172">Implemented as <strong>JetRestore2W</strong> (Unicode) and <strong>JetRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a44f0-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a44f0-173">See Also</span></span>

[<span data-ttu-id="a44f0-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a44f0-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a44f0-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a44f0-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a44f0-176">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a44f0-176">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a44f0-177">JetBackup</span><span class="sxs-lookup"><span data-stu-id="a44f0-177">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="a44f0-178">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="a44f0-178">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="a44f0-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="a44f0-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a44f0-180">JetInit</span><span class="sxs-lookup"><span data-stu-id="a44f0-180">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="a44f0-181">JetRestore</span><span class="sxs-lookup"><span data-stu-id="a44f0-181">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="a44f0-182">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="a44f0-182">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="a44f0-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a44f0-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
