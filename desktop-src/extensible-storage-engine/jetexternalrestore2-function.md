---
description: 'Saiba mais sobre: função JetExternalRestore2'
title: Função JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922178"
---
# <a name="jetexternalrestore2-function"></a><span data-ttu-id="3b398-103">Função JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="3b398-103">JetExternalRestore2 Function</span></span>


<span data-ttu-id="3b398-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b398-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore2-function"></a><span data-ttu-id="3b398-105">Função JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="3b398-105">JetExternalRestore2 Function</span></span>

<span data-ttu-id="3b398-106">A função **JetExternalRestore2** restaura um backup externo que foi feito com as APIs de backup externo e fornece pontos de verificação a serem usados para operações de log circulares.</span><span class="sxs-lookup"><span data-stu-id="3b398-106">The **JetExternalRestore2** function restores an external backup that was taken with the external backup APIs and provides checkpoints to use for circular logging operations.</span></span> <span data-ttu-id="3b398-107">Isso é conhecido como recuperação complexa, que é semelhante, mas diferente da recuperação simples, conforme executado pela função [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3b398-107">This is known as hard recovery, which is similar but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

<span data-ttu-id="3b398-108">**Windows XP: o JetExternalRestore2** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b398-108">**Windows XP:  JetExternalRestore2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="3b398-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b398-109">Parameters</span></span>

<span data-ttu-id="3b398-110">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="3b398-110">*szCheckpointFilePath*</span></span>

<span data-ttu-id="3b398-111">O caminho para o arquivo de ponto de verificação a ser usado durante a recuperação se *szTargetInstanceCheckpointPath* não for especificado ou se o caminho tiver uma instância ativa ou em execução.</span><span class="sxs-lookup"><span data-stu-id="3b398-111">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or that path has an active or running instance.</span></span>

<span data-ttu-id="3b398-112">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="3b398-112">*szLogPath*</span></span>

<span data-ttu-id="3b398-113">O caminho ou diretório para os logs da fase final (desfazer) da recuperação e, possivelmente, para os logs de roll-forward.</span><span class="sxs-lookup"><span data-stu-id="3b398-113">The path or directory for the logs for the final phase (undo) of the recovery and possibly for the roll forward logs.</span></span> <span data-ttu-id="3b398-114">Esse caminho pode ser o mesmo que o *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="3b398-114">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="3b398-115">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="3b398-115">*rgrstmap*</span></span>

<span data-ttu-id="3b398-116">Esta é uma matriz de estruturas de [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="3b398-116">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="3b398-117">Este é um mapa de caminhos de banco de dados novos e antigos ou nomes de File.</span><span class="sxs-lookup"><span data-stu-id="3b398-117">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="3b398-118">Isso é usado porque os bancos de dados podem precisar ser recuperados para um local diferente do local do qual foram feitos backup.</span><span class="sxs-lookup"><span data-stu-id="3b398-118">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="3b398-119">No caso em que vários bancos de dados são anexados a um único conjunto de registros, o mapa de restauração pode especificar um subconjunto dos bancos de dados a serem restaurados.</span><span class="sxs-lookup"><span data-stu-id="3b398-119">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of the databases to restore.</span></span>

<span data-ttu-id="3b398-120">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="3b398-120">*crstfilemap*</span></span>

<span data-ttu-id="3b398-121">O número de entradas no parâmetro de matriz *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="3b398-121">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="3b398-122">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="3b398-122">*szBackupLogPath*</span></span>

<span data-ttu-id="3b398-123">O caminho para o diretório em que os arquivos de log são restaurados.</span><span class="sxs-lookup"><span data-stu-id="3b398-123">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="3b398-124">Esses são os logs que foram lidos durante a sequência de backup externo.</span><span class="sxs-lookup"><span data-stu-id="3b398-124">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="3b398-125">Esse caminho pode ser o mesmo que o *szLogPath*.</span><span class="sxs-lookup"><span data-stu-id="3b398-125">This path may be the same as the *szLogPath*.</span></span>

<span data-ttu-id="3b398-126">*pLogInfo*</span><span class="sxs-lookup"><span data-stu-id="3b398-126">*pLogInfo*</span></span>

<span data-ttu-id="3b398-127">O *pLogInfo* descreve vários aspectos dos logs de backup para recuperação, esse parâmetro permite que o **JetExternalRestore2** assuma os parâmetros explícitos de *GenLow* e *genHigh* que o **JetExternalRestore2** tem, bem como o nome do log base, em vez de um nome de base de log presumido de "edb".</span><span class="sxs-lookup"><span data-stu-id="3b398-127">The *pLogInfo* describes several aspects of the backup logs to recovery, this parameter allows **JetExternalRestore2** to take the explicit *genLow* and *genHigh* parameters that **JetExternalRestore2** has, as well as the base log name, instead of a presumed log base name of "edb".</span></span>

<span data-ttu-id="3b398-128">*szTargetInstanceName*</span><span class="sxs-lookup"><span data-stu-id="3b398-128">*szTargetInstanceName*</span></span>

<span data-ttu-id="3b398-129">Este parâmetro foi preterido e não pode ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b398-129">This parameter is deprecated and cannot be used in your application.</span></span>

<span data-ttu-id="3b398-130">*szTargetInstanceLogPath*</span><span class="sxs-lookup"><span data-stu-id="3b398-130">*szTargetInstanceLogPath*</span></span>

<span data-ttu-id="3b398-131">O caminho para os logs de roll-forward se o local dos logs que você deseja rolar para frente estiver em um conjunto de logs ou instância ativa.</span><span class="sxs-lookup"><span data-stu-id="3b398-131">The path for the roll forward logs if the location of the logs you would like to roll forward are in an active logging set or instance.</span></span> <span data-ttu-id="3b398-132">Isso não deve ser especificado se a instância de destino estiver usando log circular.</span><span class="sxs-lookup"><span data-stu-id="3b398-132">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="3b398-133">*szTargetInstanceCheckpointPath*</span><span class="sxs-lookup"><span data-stu-id="3b398-133">*szTargetInstanceCheckpointPath*</span></span>

<span data-ttu-id="3b398-134">O caminho para o ponto de verificação durante a recuperação se não houver nenhuma instância ativa em execução nesse destino.</span><span class="sxs-lookup"><span data-stu-id="3b398-134">The path for the checkpoint during recovery if there is no active instance running at this target.</span></span> <span data-ttu-id="3b398-135">Isso não deve ser especificado se a instância de destino estiver usando log circular.</span><span class="sxs-lookup"><span data-stu-id="3b398-135">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="3b398-136">*PFN*</span><span class="sxs-lookup"><span data-stu-id="3b398-136">*pfn*</span></span>

<span data-ttu-id="3b398-137">O retorno de chamada de status, que relata o progresso da recuperação.</span><span class="sxs-lookup"><span data-stu-id="3b398-137">The status callback, which reports the progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="3b398-138">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3b398-138">Return Value</span></span>

<span data-ttu-id="3b398-139">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b398-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3b398-140">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3b398-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b398-141">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b398-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b398-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b398-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b398-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b398-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b398-144">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3b398-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-145">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="3b398-145">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="3b398-146">O <em>szTargetInstanceLogPath</em> especificado não pertence a uma instância inicializada.</span><span class="sxs-lookup"><span data-stu-id="3b398-146">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="3b398-147">Esse erro só será retornado no Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3b398-147">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b398-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="3b398-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="3b398-149">Isso indica que o banco de dados foi corrompido ou um arquivo não reconhecido.</span><span class="sxs-lookup"><span data-stu-id="3b398-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-150">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="3b398-150">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="3b398-151">Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log acima especificada em <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="3b398-151">This error is returned if one for the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b398-152">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="3b398-152">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="3b398-153">A operação falhou porque não pôde abrir o arquivo solicitado porque ele não foi encontrado no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="3b398-153">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-154">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3b398-154">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3b398-155">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3b398-155">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="3b398-156">Isso pode ocorrer para <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, e assim por diante, quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> não forem especificados ou não forem ambos não especificados.</span><span class="sxs-lookup"><span data-stu-id="3b398-156">This can happen for <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="3b398-157">Ou seja, eles devem corresponder e ser especificados ou ambos não especificados.</span><span class="sxs-lookup"><span data-stu-id="3b398-157">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b398-158">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="3b398-158">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="3b398-159">A operação falhou porque o caminho especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="3b398-159">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="3b398-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="3b398-161">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="3b398-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b398-162">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="3b398-162">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="3b398-163">Esse erro será retornado se o arquivo de banco de dados especificado durante a restauração não for um banco de dados cujo backup foi feito com backup externo.</span><span class="sxs-lookup"><span data-stu-id="3b398-163">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-164">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="3b398-164">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="3b398-165">O mecanismo de banco de dados não pode executar restauração externa ou recuperação de hardware no modo de instância única.</span><span class="sxs-lookup"><span data-stu-id="3b398-165">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="3b398-166">Esse erro só será retornado no Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3b398-166">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b398-167">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="3b398-167">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="3b398-168">Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log abaixo especificada pelo <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="3b398-168">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b398-169">Em caso de sucesso, todos os bancos de dados do *rgrstmap* são completamente recuperados e em um estado limpo ou consistente.</span><span class="sxs-lookup"><span data-stu-id="3b398-169">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="3b398-170">Neste ponto, o banco de dados pode ser remontado em uma instância existente.</span><span class="sxs-lookup"><span data-stu-id="3b398-170">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="3b398-171">Em caso de falha, o mecanismo não pôde recuperar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b398-171">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="3b398-172">O banco de dados está em um estado inválido e, para tentar a recuperação complexa, todo o banco de dados deve ser restaurado novamente.</span><span class="sxs-lookup"><span data-stu-id="3b398-172">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="3b398-173">Normalmente, a origem de tal situação é a corrupção de disco ou log, ou alguma outra forma de gerenciamento de ingestão de log ou um conjunto de logs não contínuo.</span><span class="sxs-lookup"><span data-stu-id="3b398-173">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3b398-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b398-174">Remarks</span></span>

<span data-ttu-id="3b398-175">Consulte [JetExternalRestore](./jetexternalrestore-function.md).</span><span class="sxs-lookup"><span data-stu-id="3b398-175">See [JetExternalRestore](./jetexternalrestore-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b398-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b398-176">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b398-177"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3b398-177"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b398-178">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b398-178">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-179"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3b398-179"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b398-180">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b398-180">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b398-181"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3b398-181"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b398-182">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3b398-182">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-183"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3b398-183"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b398-184">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b398-184">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b398-185"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3b398-185"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b398-186">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b398-186">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b398-187"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3b398-187"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3b398-188">Implementado como <strong>JetExternalRestore2W</strong> (Unicode) e <strong>JetExternalRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3b398-188">Implemented as <strong>JetExternalRestore2W</strong> (Unicode) and <strong>JetExternalRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b398-189">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3b398-189">See Also</span></span>

[<span data-ttu-id="3b398-190">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b398-190">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b398-191">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="3b398-191">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="3b398-192">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="3b398-192">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="3b398-193">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="3b398-193">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="3b398-194">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="3b398-194">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="3b398-195">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="3b398-195">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="3b398-196">JetInit</span><span class="sxs-lookup"><span data-stu-id="3b398-196">JetInit</span></span>](./jetinit-function.md)
