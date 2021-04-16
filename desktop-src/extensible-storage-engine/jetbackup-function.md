---
description: 'Saiba mais sobre: função JetBackup'
title: Função JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765061"
---
# <a name="jetbackup-function"></a><span data-ttu-id="8bd1c-103">Função JetBackup</span><span class="sxs-lookup"><span data-stu-id="8bd1c-103">JetBackup Function</span></span>


<span data-ttu-id="8bd1c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8bd1c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackup-function"></a><span data-ttu-id="8bd1c-105">Função JetBackup</span><span class="sxs-lookup"><span data-stu-id="8bd1c-105">JetBackup Function</span></span>

<span data-ttu-id="8bd1c-106">A função **JetBackup** cria um backup do banco de dados enquanto o banco de dados está online.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-106">The **JetBackup** function creates a backup of the database while the database is online.</span></span> <span data-ttu-id="8bd1c-107">Essa função é usada principalmente para compatibilidade com versões anteriores com o Windows 2000 e com mecanismos de banco de dados anterior, em que apenas uma instância de um banco de dados é permitida.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="8bd1c-108">Nesse caso, a instância ativa é a instância que é submetida a backup.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-108">In this case, the active instance is the instance that is backed up.</span></span>

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="8bd1c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bd1c-109">Parameters</span></span>

<span data-ttu-id="8bd1c-110">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="8bd1c-110">*szBackupPath*</span></span>

<span data-ttu-id="8bd1c-111">O diretório em que o backup está armazenado.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-111">The directory where the backup is stored.</span></span> <span data-ttu-id="8bd1c-112">Se o caminho de backup for nulo, a função truncará os logs, se possível.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-112">If the backup path is NULL, the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="8bd1c-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8bd1c-113">*grbit*</span></span>

<span data-ttu-id="8bd1c-114">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-114">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bd1c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8bd1c-115">Value</span></span></p></th>
<th><p><span data-ttu-id="8bd1c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8bd1c-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-117">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="8bd1c-117">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-118">Cria um backup completo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-118">Creates a full backup of the database.</span></span> <span data-ttu-id="8bd1c-119">Isso permite a preservação de um backup existente no mesmo diretório se o novo backup falhar.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-120">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="8bd1c-120">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-121">Cria um backup incremental em oposição a um backup completo.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-121">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="8bd1c-122">Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-122">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8bd1c-123">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="8bd1c-123">*pfnStatus*</span></span>

<span data-ttu-id="8bd1c-124">Aponta para a função de retorno de chamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que fornece informações de notificação sobre o progresso da operação de backup.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-124">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="8bd1c-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8bd1c-125">Return Value</span></span>

<span data-ttu-id="8bd1c-126">A função retorna um dos [JET_ERR](./jet-err.md) códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-126">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="8bd1c-127">Veja a seguir as mais comumente retornadas.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-127">The following are the most commonly returned.</span></span> <span data-ttu-id="8bd1c-128">(Para obter uma lista completa de erros para essa API, consulte [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="8bd1c-128">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bd1c-129">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8bd1c-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="8bd1c-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bd1c-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8bd1c-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-132">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-133">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="8bd1c-133">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-134">Um backup já está em andamento para a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-134">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="8bd1c-135">Não são permitidos vários backups ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-135">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-136">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="8bd1c-136">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-137">A instância ainda não está pronta para backup durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-137">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-138">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8bd1c-138">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-139">A operação não pode ser concluída porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-139">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8bd1c-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-141">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-141">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8bd1c-142"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-142"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-143">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="8bd1c-143">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-144">Um backup incremental não será permitido se o log circular estiver ativado.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-144">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-145">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="8bd1c-145">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-146">As opções especificadas são inválidas.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-146">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-147">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8bd1c-147">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-148">Um parâmetro inválido foi passado para a API.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-148">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-149">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="8bd1c-149">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-150">O caminho de destino não existe.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-150">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-151">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="8bd1c-151">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-152">A instância está sendo executada sem registro em log.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-152">The instance is running without logging.</span></span> <span data-ttu-id="8bd1c-153">Nenhum backup é permitido.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-153">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-154">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="8bd1c-154">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-155">Erro de verificação de checksum em um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-155">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-156">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="8bd1c-156">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-157">O log da instância é temporário ou permanentemente desabilitado devido a um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-157">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8bd1c-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-159">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-159">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-160">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="8bd1c-160">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-161">Ocorreu um erro de verificação de checksum em uma página de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-161">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8bd1c-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-163">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8bd1c-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-165">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="8bd1c-166"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-166"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8bd1c-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8bd1c-168">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-168">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8bd1c-169">Se a função for realizada com sucesso, todos os arquivos necessários para uma restauração até o momento do backup estarão contidos no diretório de backup.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-169">If the function succeeds, all the files needed for a restore up to the moment of the backup will be contained in the backup directory.</span></span> <span data-ttu-id="8bd1c-170">Se esse for um backup completo, os arquivos serão os arquivos de banco de dados e os arquivos de log necessários para colocar o banco de dados em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-170">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="8bd1c-171">Se esse for um backup incremental, somente os arquivos de log serão adicionados aos diretórios, mas os arquivos já existentes (bancos de dados e arquivos de log), juntamente com os novos arquivos de log, poderão ser restaurados para colocar o banco de dados novamente no estado em que ele estava no momento em que o backup começou.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-171">If this is an incremental backup, only log files will be added to the directories, but the already existing files (databases and log files), together with the new log files, will be able to be restored to bring the database back to the state it was in at the moment that the backup began.</span></span>

<span data-ttu-id="8bd1c-172">Como um efeito colateral do backup, os arquivos de log que não são mais necessários serão truncados.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-172">As a side effect of the backup, the log files which are no longer needed will be truncated.</span></span>

<span data-ttu-id="8bd1c-173">Ao mesmo tempo, os cabeçalhos de banco de dados serão atualizados com as informações quando o último backup tiver ocorrido.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-173">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="8bd1c-174">Se a função falhar, não haverá nenhum arquivo no destino do diretório de backup, portanto, nenhuma restauração será possível.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-174">If the function fails, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="8bd1c-175">Ao mesmo tempo, os arquivos de log atuais não serão truncados.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-175">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8bd1c-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bd1c-176">Remarks</span></span>

<span data-ttu-id="8bd1c-177">As diferentes etapas do backup terão entradas de log de eventos geradas, incluindo os nomes de arquivo, o truncamento de log e o resultado final do backup.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-177">The different steps of the backup will have Event Log entries generated, including the file names, the log truncation, and the final result of the backup.</span></span>

<span data-ttu-id="8bd1c-178">Os backups incrementais são possíveis somente após a tomada de um backup completo.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-178">Incremental backups are possible only after a full backup was taken.</span></span> <span data-ttu-id="8bd1c-179">Além disso, os backups incrementais só serão possíveis se o log circular estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-179">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="8bd1c-180">É recomendável que o diretório de backup não contenha nenhum arquivo que não seja o usado no backup ou adicionado por um backup bem-sucedido anterior.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-180">It is recommended that the backup directory should not contain any files other than the one used in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="8bd1c-181">O diretório de backup deve existir, a menos que o parâmetro *JET_paramCreatePathIfNotExist* esteja definido para a instância.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-181">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="8bd1c-182">Para obter informações, consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8bd1c-182">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="8bd1c-183">O backup fará uma verificação de checksum em todas as páginas de banco de dados usadas e, a partir do Windows Server 2003, nos arquivos de log também.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-183">The backup will do a checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="8bd1c-184">Isso dá a oportunidade de estimar a integridade do banco de dados, mesmo para páginas que não são lidas durante operações normais.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-184">This gives an opportunity to estimate the health of the database, even for pages which are not read during normal operations.</span></span> <span data-ttu-id="8bd1c-185">Se algum dano for encontrado, o backup falhará.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-185">If any such corruption is encountered, the backup will fail.</span></span>

<span data-ttu-id="8bd1c-186">Durante o backup, o arquivo de log atual será concluído e um novo log será gerado.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-186">During the backup, the current log file will be finished and a new log will be generated.</span></span> <span data-ttu-id="8bd1c-187">Dessa forma, todos os arquivos de log necessários podem ser copiados, porque o log atual não estará mais em uso.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-187">This way, all of the necessary log files can be copies, because the current log will not be in use anymore.</span></span>

<span data-ttu-id="8bd1c-188">É altamente recomendável que o backup não seja usado para nenhuma finalidade diferente do backup e da restauração no nível do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-188">It is strongly recommended that the backup not be used for any purpose other than the backup and restore at the engine level.</span></span> <span data-ttu-id="8bd1c-189">Isso minimizará a possibilidade de obter erros durante as operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-189">This will minimize the chance of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8bd1c-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bd1c-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-191"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8bd1c-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8bd1c-192">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-193"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="8bd1c-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8bd1c-194">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-195"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="8bd1c-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8bd1c-196">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-197"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="8bd1c-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8bd1c-198">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bd1c-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8bd1c-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8bd1c-200">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-200">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bd1c-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8bd1c-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8bd1c-202">Implementado como <strong>JetBackupW</strong> (Unicode) e <strong>JetBackupA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8bd1c-202">Implemented as <strong>JetBackupW</strong> (Unicode) and <strong>JetBackupA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8bd1c-203">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8bd1c-203">See Also</span></span>

[<span data-ttu-id="8bd1c-204">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="8bd1c-204">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="8bd1c-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8bd1c-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8bd1c-206">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8bd1c-206">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8bd1c-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8bd1c-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8bd1c-208">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="8bd1c-208">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="8bd1c-209">JetRestore</span><span class="sxs-lookup"><span data-stu-id="8bd1c-209">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="8bd1c-210">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="8bd1c-210">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="8bd1c-211">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="8bd1c-211">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="8bd1c-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8bd1c-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="8bd1c-213">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="8bd1c-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
