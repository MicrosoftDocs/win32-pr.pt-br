---
description: 'Saiba mais sobre: função JetBeginExternalBackup'
title: Função JetBeginExternalBackup
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766933"
---
# <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="4c6c7-103">Função JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="4c6c7-103">JetBeginExternalBackup Function</span></span>


<span data-ttu-id="4c6c7-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4c6c7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="4c6c7-105">Função JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="4c6c7-105">JetBeginExternalBackup Function</span></span>

<span data-ttu-id="4c6c7-106">A função **JetBeginExternalBackup** inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-106">The **JetBeginExternalBackup** function initiates an external backup while the engine and database is online and active.</span></span> <span data-ttu-id="4c6c7-107">**JetBeginExternalBackup** é o primeiro de uma série de funções que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-107">**JetBeginExternalBackup** is the first in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="4c6c7-108">Um backup externo pode ser usado para implementar backups completos, incrementais ou diferenciais.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-108">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="4c6c7-109">O backup será difuso, pois o backup será consistente para um único ponto no histórico de transações, mas não é possível controlar o ponto exato no tempo.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-109">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4c6c7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c6c7-110">Parameters</span></span>

<span data-ttu-id="4c6c7-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4c6c7-111">*grbit*</span></span>

<span data-ttu-id="4c6c7-112">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-112">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c6c7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4c6c7-113">Value</span></span></p></th>
<th><p><span data-ttu-id="4c6c7-114">Significado</span><span class="sxs-lookup"><span data-stu-id="4c6c7-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-115">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="4c6c7-115">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-116">Esse sinalizador foi preterido.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-116">This flag is deprecated.</span></span> <span data-ttu-id="4c6c7-117">O uso desse bit resultará na JET_errInvalidgrbit retornando.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-117">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-118">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="4c6c7-118">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-119">Cria um backup incremental em oposição a um backup completo.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-119">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="4c6c7-120">Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-120">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-121">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="4c6c7-121">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-122">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-122">Reserved for future use.</span></span> <span data-ttu-id="4c6c7-123">Definido para o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-123">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4c6c7-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4c6c7-124">Return Value</span></span>

<span data-ttu-id="4c6c7-125">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4c6c7-126">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4c6c7-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c6c7-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4c6c7-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="4c6c7-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c6c7-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4c6c7-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-130">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="4c6c7-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-132">Se um backup externo ou backup de instantâneo já estiver em andamento, esse erro será retornado, até que <strong>JetBeginExternalBackup</strong> (ou uma das variantes de ti) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-132">If an external backup or snapshot backup is already in process, this error will be returned, until <strong>JetBeginExternalBackup</strong> (or one of the variants of it) is called.</span></span> <span data-ttu-id="4c6c7-133">O ESE permite apenas um backup online de cada vez.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-133">ESE allows only one online backup at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-134">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="4c6c7-134">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-135">A instância ou o mecanismo de banco de dados está em recuperação ou em uma fase de desligamento ou término.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-135">The instance or database engine is either in recovery or in a shutdown or termination phase.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-136">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="4c6c7-136">JET_errCheckpointCorrupt</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-137">Em um backup completo, o arquivo de ponto de verificação não pôde ser lido ou o arquivo não pôde ser verificado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-137">On a full backup, the checkpoint file could not be read, or the file could not be verified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-138">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="4c6c7-138">JET_errCheckpointFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-139">Em um backup completo, o arquivo de ponto de verificação não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-139">On a full backup, the checkpoint file could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4c6c7-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-141">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-141">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4c6c7-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-143">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-143">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="4c6c7-144"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-144"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-145">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="4c6c7-145">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-146">O log circular está habilitado e o tipo de backup especificado é JET_bitBackupIncremental.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-146">Circular logging is enabled and the backup type specified is JET_bitBackupIncremental.</span></span> <span data-ttu-id="4c6c7-147">Consulte <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> nos <strong>erros do log de transações</strong> para obter informações sobre como controlar o registro em log circular ou não circular.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-147">See <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in the <strong>Transaction Log Errors</strong> for information about how to control circular or non-circular logging.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-148">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="4c6c7-148">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-149">Um ou mais dos membros do <em>grbit</em> eram inválidos.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-149">One or more of the <em>grbit</em> members was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-150">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="4c6c7-150">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-151">A recuperação ou o log está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-151">Recovery or logging is disabled.</span></span> <span data-ttu-id="4c6c7-152">Você não poderá fazer um backup online se o log estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-152">You cannot do an online backup if logging is disabled.</span></span> <span data-ttu-id="4c6c7-153">Para obter mais informações sobre log e recuperação, consulte <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-153">For more information about logging and recovery, see <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-154">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="4c6c7-154">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-155">O mecanismo parou de gravar na unidade de log devido ao log estar cheio ou erros de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-155">The engine has stopped writing to the log drive, due to log being full or disk IO errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-156">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="4c6c7-156">JET_errMissingFullBackup</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-157">O backup incremental foi especificado (com JET_bitBackupIncremental) e nunca foi feito um backup completo para um dos bancos de dados anexados para o conjunto de logs.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-157">The incremental backup was specified (with JET_bitBackupIncremental), and never was a full backup taken for one of the attached databases for the logging set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4c6c7-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-159">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="4c6c7-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-161">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4c6c7-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-163">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-164">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="4c6c7-164">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-165">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-165">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4c6c7-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4c6c7-167">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-167">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c6c7-168">Se a função for realizada com sucesso, um backup externo será iniciado e o mecanismo de estado de backup será inicializado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-168">If the function succeeds, an external backup is initiated and the backup state engine is initialized.</span></span> <span data-ttu-id="4c6c7-169">As APIs subsequentes agora podem ser chamadas para concluir a sequência de backup externo e transmitir ou ler o arquivo de banco de dados, o arquivo de patch de banco de dados (se houver suporte) e o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-169">Subsequent APIs can now be called to complete the external backup sequence and stream or read off the database file, the database patch file (if supported), and the log file.</span></span> <span data-ttu-id="4c6c7-170">Um evento pode ser registrado em log que um backup externo foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-170">An event can be logged that an external backup has begun.</span></span>

<span data-ttu-id="4c6c7-171">Se a função falhar, a sessão de backup não será iniciada.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-171">If the function fails, the backup session will not be initiated.</span></span> <span data-ttu-id="4c6c7-172">Se outra sessão de backup estiver em andamento, ela não será cancelada.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-172">If another backup session is in progress, it will not be cancelled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4c6c7-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c6c7-173">Remarks</span></span>

<span data-ttu-id="4c6c7-174">O processo de backup externo (como iniciado por **JetBeginExternalBackup**) foi projetado para permitir um backup online de transação difusa de toda a instância para um dispositivo de destino como um fluxo.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-174">The external backup process (as started by **JetBeginExternalBackup**) is designed to allow a fuzzy transaction online backup of the entire instance to a target device as a stream.</span></span> <span data-ttu-id="4c6c7-175">O backup conterá todos os arquivos de banco de dados anexados à instância usando [JetAttachDatabase](./jetattachdatabase-function.md) (para um backup completo), seguidos por seus arquivos de patch de banco de dados associados (se houver suporte) e, por fim, pelos arquivos de log de transações que foram gerados durante o processo de backup.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-175">The backup will contain all the database files that are attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) (for a full backup), followed by their associated database patch files (if supported), and finally by the transaction log files that were generated during the backup process.</span></span> <span data-ttu-id="4c6c7-176">O resultado final será um conjunto de arquivos que podem ser restaurados do fluxo, possivelmente combinados com os arquivos de banco de dados e de log existentes e, por fim, recuperados para um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-176">The end result will be a set of files that can be restored from the stream, possibly combined with existing database and log files, and finally recovered to a consistent state.</span></span>

<span data-ttu-id="4c6c7-177">A ordem geral de operações para um backup completo consiste nas chamadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-177">The general order of operations for a full backup consists of the following calls.</span></span> <span data-ttu-id="4c6c7-178">Primeiro, **JetBeginExternalBackup** é chamado para iniciar o processo de backup.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-178">First, **JetBeginExternalBackup** is called to start the backup process.</span></span> <span data-ttu-id="4c6c7-179">Em seguida, [JetGetAttachInfo](./jetgetattachinfo-function.md) é chamado para obter a lista de bancos de dados anexados à instância que precisa ser submetida a backup.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-179">Then, [JetGetAttachInfo](./jetgetattachinfo-function.md) is called to get the list of databases that are attached to the instance that needs to be backed up.</span></span> <span data-ttu-id="4c6c7-180">Para cada um desses bancos de dados, [JetOpenFile](./jetopenfile-function.md) é chamado, seguido por uma série de chamadas [JetReadFile](./jetreadfile-function.md) e, em seguida, por uma chamada para [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="4c6c7-180">For each of these databases, [JetOpenFile](./jetopenfile-function.md) is called, followed by a number of [JetReadFile](./jetreadfile-function.md) calls, and then by a call to [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="4c6c7-181">Em seguida, [JetGetLogInfo](./jetgetloginfo-function.md) é chamado para obter uma lista de arquivos de log e patch de banco de dados para backup.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-181">Then, [JetGetLogInfo](./jetgetloginfo-function.md) is called to get a list of database patch and log files to be backed up.</span></span> <span data-ttu-id="4c6c7-182">Para cada um desses arquivos, outra sequência de chamadas [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)e [JetCloseFile](./jetclosefile-function.md) são feitas.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-182">For each of these files, another sequence of [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md), and [JetCloseFile](./jetclosefile-function.md) calls are made.</span></span> <span data-ttu-id="4c6c7-183">Em seguida, todos os arquivos de log de transações indesejados são excluídos usando [JetTruncateLog](./jettruncatelog-function.md).</span><span class="sxs-lookup"><span data-stu-id="4c6c7-183">Then, any undesired transaction log files are deleted using [JetTruncateLog](./jettruncatelog-function.md).</span></span> <span data-ttu-id="4c6c7-184">Por fim, o backup é finalizado por uma chamada para [JetEndExternalBackup](./jetendexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="4c6c7-184">Finally, the backup is ended by a call to [JetEndExternalBackup](./jetendexternalbackup-function.md).</span></span>

<span data-ttu-id="4c6c7-185">Também é possível modificar esse conjunto de etapas para executar um backup incremental da instância.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-185">It is also possible to modify this set of steps to perform an incremental backup of the instance.</span></span> <span data-ttu-id="4c6c7-186">Um backup incremental enumera e faz backup dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-186">An incremental backup enumerates and backs up log files.</span></span> <span data-ttu-id="4c6c7-187">Os backups incrementais só serão possíveis se o log circular não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-187">Incremental backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="4c6c7-188">Também é possível modificar esse conjunto de etapas para permitir backups diferenciais subsequentes da instância a ser executada.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-188">It is also possible to modify this set of steps to allow subsequent differential backups of the instance to be performed.</span></span> <span data-ttu-id="4c6c7-189">Para executar um backup diferencial, não chame [JetTruncateLog](./jettruncatelog-function.md) no backup completo ou incremental anterior.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-189">To perform a differential backup, do not call [JetTruncateLog](./jettruncatelog-function.md) in the previous full or incremental backup.</span></span> <span data-ttu-id="4c6c7-190">Ao não chamar [JetTruncateLog](./jettruncatelog-function.md), você permite que os backups subsequentes sejam diferenciais em relação ao último backup completo ou incremental.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-190">By not calling [JetTruncateLog](./jettruncatelog-function.md), you enable subsequent backups to be differential with respect to the last full or incremental backup.</span></span> <span data-ttu-id="4c6c7-191">Os backups diferenciais só serão possíveis se o registro em log circular não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-191">Differential backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="4c6c7-192">O arquivo de patch de banco de dados é um arquivo auxiliar especial que é usado para armazenar imagens de página de banco de dados em determinadas circunstâncias durante o backup.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-192">The database patch file is a special auxiliary file that is used to store database page images under certain circumstances during the backup.</span></span> <span data-ttu-id="4c6c7-193">Esse arquivo deve estar presente no mesmo local que seu banco de dados associado durante uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-193">This file must be present in the same location as its associated database during a restore operation.</span></span> <span data-ttu-id="4c6c7-194">Esse arquivo só é usado no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-194">This file is only used in Windows 2000.</span></span> <span data-ttu-id="4c6c7-195">Como resultado, qualquer aplicativo escrito para funcionar no Windows 2000 e em outras versões deve dar suporte a arquivos de patch de banco de dados, se estiverem presentes, mas também não deverá falhar se não estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-195">As a result, any application that is written to work against Windows 2000 and other releases must support database patch files, if they are present, but also must not fail if they are not present.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4c6c7-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c6c7-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-197"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4c6c7-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4c6c7-198">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-199"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="4c6c7-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4c6c7-200">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-201"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="4c6c7-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4c6c7-202">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6c7-203"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="4c6c7-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4c6c7-204">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6c7-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4c6c7-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4c6c7-206">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4c6c7-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4c6c7-207">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4c6c7-207">See Also</span></span>

[<span data-ttu-id="4c6c7-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4c6c7-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4c6c7-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4c6c7-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4c6c7-210">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4c6c7-210">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4c6c7-211">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="4c6c7-211">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="4c6c7-212">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="4c6c7-212">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="4c6c7-213">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="4c6c7-213">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="4c6c7-214">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="4c6c7-214">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="4c6c7-215">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="4c6c7-215">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="4c6c7-216">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="4c6c7-216">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="4c6c7-217">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="4c6c7-217">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="4c6c7-218">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="4c6c7-218">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="4c6c7-219">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="4c6c7-219">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="4c6c7-220">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="4c6c7-220">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="4c6c7-221">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="4c6c7-221">JetTruncateLog</span></span>](./jettruncatelog-function.md)
