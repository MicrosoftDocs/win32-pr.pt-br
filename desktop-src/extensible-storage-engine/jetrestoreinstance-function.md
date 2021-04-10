---
description: 'Saiba mais sobre: função JetRestoreInstance'
title: Função JetRestoreInstance
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb7af096a63880a88496631999ddbc26a975cac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171618"
---
# <a name="jetrestoreinstance-function"></a><span data-ttu-id="4c2d3-103">Função JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="4c2d3-103">JetRestoreInstance Function</span></span>


<span data-ttu-id="4c2d3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4c2d3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestoreinstance-function"></a><span data-ttu-id="4c2d3-105">Função JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="4c2d3-105">JetRestoreInstance Function</span></span>

<span data-ttu-id="4c2d3-106">A função **JetRestoreInstance** restaura e recupera um backup de streaming de uma instância do, incluindo todos os bancos de dados anexados.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-106">The **JetRestoreInstance** function restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="4c2d3-107">Ele foi projetado para funcionar com um backup criado com a função [JetBackupInstance](./jetbackupinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2d3-107">It is designed to work with a backup created with the [JetBackupInstance](./jetbackupinstance-function.md) function.</span></span> <span data-ttu-id="4c2d3-108">Essa é a função de restauração mais simples e encapsulada.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-108">This is the simplest and most encapsulated one restore function.</span></span>

<span data-ttu-id="4c2d3-109">**Windows XP:** o **JetRestoreInstance** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="4c2d3-109">**Windows XP:**  **JetRestoreInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="4c2d3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c2d3-110">Parameters</span></span>

<span data-ttu-id="4c2d3-111">*cópia*</span><span class="sxs-lookup"><span data-stu-id="4c2d3-111">*instance*</span></span>

<span data-ttu-id="4c2d3-112">Especifica a instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-112">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="4c2d3-113">Para o Windows XP e versões posteriores, o uso desse parâmetro depende do modo de operação do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="4c2d3-114">Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser nulo ou poderá ser definido como um buffer de saída válido contendo NULL ou JET_instanceNil que retornará o identificador de instância global criado como um efeito colateral da inicialização.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="4c2d3-115">Esse identificador de instância pode então ser passado para qualquer outra API que usa uma instância.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="4c2d3-116">Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser definido como um buffer de entrada válido que contenha o identificador de instância retornado por [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-116">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="4c2d3-117">*sz*</span><span class="sxs-lookup"><span data-stu-id="4c2d3-117">*sz*</span></span>

<span data-ttu-id="4c2d3-118">A pasta onde o backup está localizado.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-118">The folder where the backup is located.</span></span> <span data-ttu-id="4c2d3-119">O backup deve ter sido gerado usando as APIs [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2d3-119">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="4c2d3-120">*szDest*</span><span class="sxs-lookup"><span data-stu-id="4c2d3-120">*szDest*</span></span>

<span data-ttu-id="4c2d3-121">Nome da pasta em que os arquivos de banco de dados do conjunto de backup serão copiados e recuperados.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-121">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="4c2d3-122">Se isso for definido como NULL (que é o caso para o [JetRestore](./jetrestore-function.md)herdado), os arquivos de banco de dados serão copiados e recuperados em seu local original.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-122">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="4c2d3-123">*PFN*</span><span class="sxs-lookup"><span data-stu-id="4c2d3-123">*pfn*</span></span>

<span data-ttu-id="4c2d3-124">O ponteiro opcional para a função que será chamada como informações de notificação sobre o progresso da operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-124">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="4c2d3-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4c2d3-125">Return Value</span></span>

<span data-ttu-id="4c2d3-126">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4c2d3-127">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d3-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c2d3-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4c2d3-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="4c2d3-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c2d3-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c2d3-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4c2d3-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4c2d3-131">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c2d3-132">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="4c2d3-132">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="4c2d3-133">A operação falhou porque o mecanismo já foi inicializado para esta instância.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-133">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c2d3-134">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="4c2d3-134">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="4c2d3-135">O conjunto de arquivos de log do conjunto de backup e do caminho de log atual não coincidem.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-135">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c2d3-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4c2d3-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4c2d3-137">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4c2d3-138">Esse erro será retornado por <strong>JetRestoreInstance</strong> quando o mecanismo estiver no modo de várias instâncias e pinstance se referir a uma instância inválida do Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-138">This error will be returned by <strong>JetRestoreInstance</strong> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c2d3-139">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="4c2d3-139">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="4c2d3-140">A operação falhou porque alguns caminhos fornecidos são inválidos (o caminho de backup, o caminho de destino, o log ou o caminho do sistema para a instância).</span><span class="sxs-lookup"><span data-stu-id="4c2d3-140">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c2d3-141">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="4c2d3-141">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="4c2d3-142">A operação falhou porque o mecanismo está configurado para usar um tamanho de página de banco de dados (usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) que não corresponde ao tamanho da página do banco de dados usado para criar os arquivos de log de transações ou os bancos de dados associados aos arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-142">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c2d3-143">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="4c2d3-143">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="4c2d3-144">A operação falhou porque o modo de instância única implícito de parâmetros (modo de compatibilidade do Windows 2000) e o mecanismo já estão no modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-144">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c2d3-145">Em caso de êxito, os arquivos de banco de dados do conjunto de backup serão restaurados para seu local e a recuperação será executada de modo que os bancos estejam em um estado de consistência transacional limpo.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-145">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="4c2d3-146">A recuperação reproduzirá os arquivos de log do conjunto de backup e dos arquivos de log do caminho de log, se esses arquivos existirem.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-146">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="4c2d3-147">Essa recuperação resultará em alterações no arquivo de ponto de verificação, nos arquivos de log de transações e em qualquer banco de dados referenciado por esses arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-147">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="4c2d3-148">Em caso de falha, a instância permanece em um estado não inicializado.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-148">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="4c2d3-149">O estado dos arquivos de log de transações e quaisquer bancos de dados referenciados por esses arquivos de log de transações provavelmente serão alterados na tentativa de inicializar a restauração e recuperar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-149">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4c2d3-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c2d3-150">Remarks</span></span>

<span data-ttu-id="4c2d3-151">O processo de recuperação reconstruirá os bancos de dados anexados à instância durante o backup e salvará as alterações de volta nos arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-151">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="4c2d3-152">O resultado será os bancos de dados que são consistentes com a transação.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-152">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="4c2d3-153">Se possível, ele também será salvo no banco de dados as alterações feitas desde que o backup foi feito até a alteração mais recente encontrada nos logs de transações.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-153">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="4c2d3-154">Isso seria possível se os logs de transações gerados desde que o backup foi feito ainda estiverem presentes no diretório de log de transações.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-154">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="4c2d3-155">Observe que, se o log circular tiver sido habilitado para a instância, os logs de transação gerados serão reutilizados, de modo que a recuperação poderá salvar as alterações que foram realizadas até o momento do backup.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-155">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="4c2d3-156">Em qualquer caso, é possível que esse processo demore algum tempo se o número de arquivos de log de transações a serem reproduzidos em relação aos bancos de dados for grande.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-156">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="4c2d3-157">**JetRestoreInstance** deve ser chamado em uma instância que já foi criada usando [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d3-157">**JetRestoreInstance** must be called on an instance which was already created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="4c2d3-158">Como, durante a recuperação, um número significativo de páginas de banco de dados e logs de transações serão usados, há uma série completa de erros que podem ser retornados por essas funções.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-158">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="4c2d3-159">Esses erros podem ser de falhas temporárias de alocação de recursos, como Jet_errOutOfMemory a erros que representam as corrupções físicas, como JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-159">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="4c2d3-160">Esses erros são quase sempre causados por problemas de hardware e, portanto, não podem ser evitados.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-160">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="4c2d3-161">O ingerenciamento de arquivos será manifestado com mais frequência como JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-161">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="4c2d3-162">Esses erros são impedidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-162">These errors are preventable by the application.</span></span> <span data-ttu-id="4c2d3-163">O aplicativo deve ter cuidado para proteger o repositório desses arquivos contra a manipulação por forças externas, como o usuário ou outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-163">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="4c2d3-164">Se o aplicativo desejar destruir uma instância inteiramente, todos os arquivos associados à instância deverão ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-164">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="4c2d3-165">Isso inclui o arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-165">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="4c2d3-166">As diferentes etapas da recuperação terão entradas de log de eventos geradas, incluindo o progresso da reprodução do log de transações e o resultado final da restauração.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-166">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4c2d3-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c2d3-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c2d3-168"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4c2d3-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4c2d3-169">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-169">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c2d3-170"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="4c2d3-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4c2d3-171">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-171">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c2d3-172"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="4c2d3-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4c2d3-173">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c2d3-174"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="4c2d3-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4c2d3-175">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c2d3-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4c2d3-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4c2d3-177">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4c2d3-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c2d3-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4c2d3-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4c2d3-179">Implementado como <strong>JetRestoreInstanceW</strong> (Unicode) e <strong>JetRestoreInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4c2d3-179">Implemented as <strong>JetRestoreInstanceW</strong> (Unicode) and <strong>JetRestoreInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4c2d3-180">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4c2d3-180">See Also</span></span>

[<span data-ttu-id="4c2d3-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4c2d3-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4c2d3-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4c2d3-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4c2d3-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4c2d3-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4c2d3-184">JetBackup</span><span class="sxs-lookup"><span data-stu-id="4c2d3-184">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="4c2d3-185">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="4c2d3-185">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="4c2d3-186">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4c2d3-186">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4c2d3-187">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4c2d3-187">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
