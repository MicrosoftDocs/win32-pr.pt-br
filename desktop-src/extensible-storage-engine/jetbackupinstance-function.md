---
description: 'Saiba mais sobre: função JetBackupInstance'
title: Função JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089884"
---
# <a name="jetbackupinstance-function"></a><span data-ttu-id="e03b4-103">Função JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="e03b4-103">JetBackupInstance Function</span></span>


<span data-ttu-id="e03b4-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e03b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackupinstance-function"></a><span data-ttu-id="e03b4-105">Função JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="e03b4-105">JetBackupInstance Function</span></span>

<span data-ttu-id="e03b4-106">A função **JetBackupInstance** executa um backup de streaming de uma instância, incluindo todos os bancos de dados anexados, em um diretório.</span><span class="sxs-lookup"><span data-stu-id="e03b4-106">The **JetBackupInstance** function performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="e03b4-107">Com vários métodos de backup com suporte no mecanismo, essa é a função mais simples e encapsulada.</span><span class="sxs-lookup"><span data-stu-id="e03b4-107">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="e03b4-108">**Windows XP: o JetBackupInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e03b4-108">**Windows XP:  JetBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="e03b4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e03b4-109">Parameters</span></span>

<span data-ttu-id="e03b4-110">*cópia*</span><span class="sxs-lookup"><span data-stu-id="e03b4-110">*instance*</span></span>

<span data-ttu-id="e03b4-111">A instância do banco de dados para backup.</span><span class="sxs-lookup"><span data-stu-id="e03b4-111">The instance of the database to backup.</span></span>

<span data-ttu-id="e03b4-112">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="e03b4-112">*szBackupPath*</span></span>

<span data-ttu-id="e03b4-113">O diretório em que o backup está armazenado.</span><span class="sxs-lookup"><span data-stu-id="e03b4-113">The directory where the backup is stored.</span></span> <span data-ttu-id="e03b4-114">Se o caminho de backup for nulo para usar a função, o truncará os logs, se possível.</span><span class="sxs-lookup"><span data-stu-id="e03b4-114">If the backup path is NULL to use the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="e03b4-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e03b4-115">*grbit*</span></span>

<span data-ttu-id="e03b4-116">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e03b4-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e03b4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e03b4-117">Value</span></span></p></th>
<th><p><span data-ttu-id="e03b4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e03b4-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="e03b4-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="e03b4-120">Cria um backup completo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e03b4-120">Creates a full backup of the database.</span></span> <span data-ttu-id="e03b4-121">Isso permite a preservação de um backup existente no mesmo diretório se o novo backup falhar.</span><span class="sxs-lookup"><span data-stu-id="e03b4-121">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="e03b4-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="e03b4-123">Cria um backup incremental em oposição a um backup completo.</span><span class="sxs-lookup"><span data-stu-id="e03b4-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="e03b4-124">Isso significa que somente os arquivos de log criados desde o último backup completo ou incremental serão submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="e03b4-124">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="e03b4-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="e03b4-126">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e03b4-126">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e03b4-127">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="e03b4-127">*pfnStatus*</span></span>

<span data-ttu-id="e03b4-128">Aponta para a função de retorno de chamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que fornece informações de notificação sobre o progresso da operação de backup.</span><span class="sxs-lookup"><span data-stu-id="e03b4-128">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="e03b4-129">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e03b4-129">Return Value</span></span>

<span data-ttu-id="e03b4-130">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e03b4-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e03b4-131">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e03b4-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e03b4-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e03b4-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="e03b4-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="e03b4-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e03b4-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e03b4-135">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e03b4-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-136">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="e03b4-136">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="e03b4-137">Um backup já está em andamento para a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="e03b4-137">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="e03b4-138">Não são permitidos vários backups ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e03b4-138">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-139">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="e03b4-139">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="e03b4-140">A instância ainda não está pronta para backup durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="e03b4-140">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e03b4-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e03b4-142">A operação não pode ser concluída porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="e03b4-142">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e03b4-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e03b4-144">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="e03b4-144">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e03b4-145"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e03b4-145"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-146">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="e03b4-146">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="e03b4-147">Um backup incremental não será permitido se o log circular estiver ativado.</span><span class="sxs-lookup"><span data-stu-id="e03b4-147">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-148">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="e03b4-148">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="e03b4-149">As opções especificadas são inválidas.</span><span class="sxs-lookup"><span data-stu-id="e03b4-149">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e03b4-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e03b4-151">Um parâmetro inválido foi passado para a API.</span><span class="sxs-lookup"><span data-stu-id="e03b4-151">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="e03b4-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="e03b4-153">O caminho de destino não existe.</span><span class="sxs-lookup"><span data-stu-id="e03b4-153">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-154">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="e03b4-154">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="e03b4-155">A instância está sendo executada sem registro em log.</span><span class="sxs-lookup"><span data-stu-id="e03b4-155">The instance is running without logging.</span></span> <span data-ttu-id="e03b4-156">Nenhum backup é permitido.</span><span class="sxs-lookup"><span data-stu-id="e03b4-156">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-157">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="e03b4-157">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="e03b4-158">Erro de verificação de checksum em um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="e03b4-158">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-159">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="e03b4-159">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="e03b4-160">O log da instância é temporário ou permanentemente desabilitado devido a um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e03b4-160">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-161">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e03b4-161">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e03b4-162">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="e03b4-162">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-163">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="e03b4-163">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="e03b4-164">Ocorreu um erro de verificação de checksum em uma página de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e03b4-164">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e03b4-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e03b4-166">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="e03b4-166">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e03b4-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e03b4-168">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e03b4-168">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e03b4-169"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e03b4-169"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e03b4-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e03b4-171">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="e03b4-171">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e03b4-172">Depois que a função retornar êxito, no diretório de backup, todos os arquivos necessários para uma restauração até o momento do backup estarão presentes.</span><span class="sxs-lookup"><span data-stu-id="e03b4-172">After the function returns success, in the backup directory all the files needed for a restore up to the moment of the backup will be present.</span></span> <span data-ttu-id="e03b4-173">Se esse for um backup completo, os arquivos serão os arquivos de banco de dados e os arquivos de log necessários para colocar o banco de dados em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="e03b4-173">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="e03b4-174">Se esse for um backup incremental, somente os arquivos de log serão adicionados aos diretórios, mas os arquivos já existentes (bancos de dados e arquivos de log) junto com os novos arquivos de log poderão ser restaurados e trazer o banco de dados de volta para o estado no momento do backup.</span><span class="sxs-lookup"><span data-stu-id="e03b4-174">If this is an incremental backup, only log files will be added to the directories but the already existing files (databases and log files) together with the new log files will be able to be restored and bring the database back to the state at the moment of the backup.</span></span>

<span data-ttu-id="e03b4-175">Como um efeito colateral do backup, os arquivos de log que não são mais necessários serão truncados.</span><span class="sxs-lookup"><span data-stu-id="e03b4-175">As a side effect of the backup, the log files which are not longer needed will be truncated.</span></span>

<span data-ttu-id="e03b4-176">Ao mesmo tempo, os cabeçalhos de banco de dados serão atualizados com as informações quando o último backup tiver ocorrido.</span><span class="sxs-lookup"><span data-stu-id="e03b4-176">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="e03b4-177">Em caso de falha, não haverá nenhum arquivo no destino do diretório de backup, portanto, nenhuma restauração será possível.</span><span class="sxs-lookup"><span data-stu-id="e03b4-177">On failure, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="e03b4-178">Ao mesmo tempo, os arquivos de log atuais não serão truncados.</span><span class="sxs-lookup"><span data-stu-id="e03b4-178">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e03b4-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="e03b4-179">Remarks</span></span>

<span data-ttu-id="e03b4-180">As diferentes etapas do backup terão entradas de log de eventos geradas, incluindo os nomes de arquivo, o truncamento de log e o resultado final do backup.</span><span class="sxs-lookup"><span data-stu-id="e03b4-180">The different steps of the backup will have Event Log entries generated including the file names, the log truncation and the final result of the backup.</span></span>

<span data-ttu-id="e03b4-181">O backup incremental só é possível depois que um backup completo foi feito.</span><span class="sxs-lookup"><span data-stu-id="e03b4-181">Incremental backup are possible only after a full backup was taken.</span></span> <span data-ttu-id="e03b4-182">Além disso, os backups incrementais só serão possíveis se o log circular estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="e03b4-182">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="e03b4-183">É recomendável que o diretório de backup não contenha outros arquivos, o que está envolvido no backup ou adicionado por um backup bem-sucedido anterior.</span><span class="sxs-lookup"><span data-stu-id="e03b4-183">It is recommended that the backup directory should not contain other files then the one involved in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="e03b4-184">O diretório de backup deve existir, a menos que o parâmetro *JET_paramCreatePathIfNotExist* esteja definido para a instância.</span><span class="sxs-lookup"><span data-stu-id="e03b4-184">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="e03b4-185">Para obter informações, consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e03b4-185">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="e03b4-186">O backup fará a verificação de checksum em todas as páginas de banco de dados usadas e a partir do Windows Server 2003, nos arquivos de log também.</span><span class="sxs-lookup"><span data-stu-id="e03b4-186">The backup will do checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="e03b4-187">Isso dá a oportunidade de estimar a integridade do banco de dados mesmo para páginas que não são lidas durante operações normais.</span><span class="sxs-lookup"><span data-stu-id="e03b4-187">This gives an opportunity to estimate the health of the database even for pages which are not read during normal operations.</span></span> <span data-ttu-id="e03b4-188">Se qualquer dano for encontrado, o backup falhará.</span><span class="sxs-lookup"><span data-stu-id="e03b4-188">If any such corruption will be encountered, the backup will fail.</span></span>

<span data-ttu-id="e03b4-189">Durante o backup, o arquivo de log atual será concluído e começaremos uma nova geração de log.</span><span class="sxs-lookup"><span data-stu-id="e03b4-189">During the backup, the current log file will be finished and we will start a new log generation.</span></span> <span data-ttu-id="e03b4-190">Isso permitirá copiar os arquivos de log necessários porque o último necessário não estará mais em uso.</span><span class="sxs-lookup"><span data-stu-id="e03b4-190">This will allow copying the needed log files because the last needed one will not be in use anymore.</span></span>

<span data-ttu-id="e03b4-191">É altamente recomendável que o backup não seja usado para outros fins, o backup e restaurado no nível do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="e03b4-191">It is strongly recommended that the backup should not be used for other purposed other then the backup and restored at the engine level.</span></span> <span data-ttu-id="e03b4-192">Isso minimizará a alteração da obtenção de erros durante as operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="e03b4-192">This will minimize the change of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e03b4-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e03b4-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-194"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e03b4-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e03b4-195">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e03b4-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-196"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e03b4-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e03b4-197">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e03b4-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-198"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e03b4-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e03b4-199">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e03b4-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-200"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e03b4-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e03b4-201">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e03b4-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03b4-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e03b4-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e03b4-203">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e03b4-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03b4-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e03b4-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e03b4-205">Implementado como <strong>JetBackupInstanceW</strong> (Unicode) e <strong>JetBackupInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e03b4-205">Implemented as <strong>JetBackupInstanceW</strong> (Unicode) and <strong>JetBackupInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e03b4-206">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e03b4-206">See Also</span></span>

[<span data-ttu-id="e03b4-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e03b4-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e03b4-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e03b4-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e03b4-209">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e03b4-209">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e03b4-210">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="e03b4-210">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="e03b4-211">JetRestore</span><span class="sxs-lookup"><span data-stu-id="e03b4-211">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="e03b4-212">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="e03b4-212">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="e03b4-213">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="e03b4-213">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="e03b4-214">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="e03b4-214">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)  
[<span data-ttu-id="e03b4-215">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="e03b4-215">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
