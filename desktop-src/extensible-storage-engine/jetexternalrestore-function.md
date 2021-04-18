---
description: 'Saiba mais sobre: função JetExternalRestore'
title: Função JetExternalRestore
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105786273"
---
# <a name="jetexternalrestore-function"></a><span data-ttu-id="1baa2-103">Função JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="1baa2-103">JetExternalRestore Function</span></span>


<span data-ttu-id="1baa2-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1baa2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore-function"></a><span data-ttu-id="1baa2-105">Função JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="1baa2-105">JetExternalRestore Function</span></span>

<span data-ttu-id="1baa2-106">A função **JetExternalRestore** restaura um backup externo que foi feito com as APIs de backup externo e especifica um intervalo de números de arquivos de log a serem reproduzidos durante o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="1baa2-106">The **JetExternalRestore** function restores an external backup that was taken with the external backup APIs and specifies a range of log file numbers to replay during the restore process.</span></span> <span data-ttu-id="1baa2-107">Isso é conhecido como recuperação complexa, que é semelhante a, mas diferente da recuperação simples, conforme executado pela função [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1baa2-107">This is known as hard recovery, which is similar to but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="1baa2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1baa2-108">Parameters</span></span>

<span data-ttu-id="1baa2-109">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="1baa2-109">*szCheckpointFilePath*</span></span>

<span data-ttu-id="1baa2-110">O caminho para o arquivo de ponto de verificação a ser usado durante a recuperação se *szTargetInstanceCheckpointPath* não for especificado ou se já tiver uma instância ativa ou em execução.</span><span class="sxs-lookup"><span data-stu-id="1baa2-110">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or already has an active or running instance.</span></span>

<span data-ttu-id="1baa2-111">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="1baa2-111">*szLogPath*</span></span>

<span data-ttu-id="1baa2-112">O caminho ou diretório para os logs da fase final (desfazer) de recuperação e, possivelmente, para os logs de roll-forward.</span><span class="sxs-lookup"><span data-stu-id="1baa2-112">The path or directory for the logs for the final phase (undo) of recovery, and possibly for the roll forward logs.</span></span> <span data-ttu-id="1baa2-113">Esse caminho pode ser o mesmo que o *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="1baa2-113">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="1baa2-114">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="1baa2-114">*rgrstmap*</span></span>

<span data-ttu-id="1baa2-115">Esta é uma matriz de estruturas de [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="1baa2-115">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="1baa2-116">Este é um mapa de caminhos de banco de dados novos e antigos ou nomes de File.</span><span class="sxs-lookup"><span data-stu-id="1baa2-116">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="1baa2-117">Isso é usado porque os bancos de dados podem precisar ser recuperados para um local diferente do local do qual foram feitos backup.</span><span class="sxs-lookup"><span data-stu-id="1baa2-117">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="1baa2-118">No caso em que vários bancos de dados são anexados a um único conjunto de registros, o mapa de restauração pode especificar um subconjunto de bancos de dados a serem restaurados.</span><span class="sxs-lookup"><span data-stu-id="1baa2-118">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of databases to restore.</span></span>

<span data-ttu-id="1baa2-119">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="1baa2-119">*crstfilemap*</span></span>

<span data-ttu-id="1baa2-120">O número de entradas no parâmetro de matriz *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="1baa2-120">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="1baa2-121">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="1baa2-121">*szBackupLogPath*</span></span>

<span data-ttu-id="1baa2-122">O caminho para o diretório em que os arquivos de log são restaurados.</span><span class="sxs-lookup"><span data-stu-id="1baa2-122">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="1baa2-123">Esses são os logs que foram lidos durante a sequência de backup externo.</span><span class="sxs-lookup"><span data-stu-id="1baa2-123">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="1baa2-124">Esse caminho pode ser o mesmo que o szLogPath.</span><span class="sxs-lookup"><span data-stu-id="1baa2-124">This path may be the same as the szLogPath.</span></span>

<span data-ttu-id="1baa2-125">*genLow*</span><span class="sxs-lookup"><span data-stu-id="1baa2-125">*genLow*</span></span>

<span data-ttu-id="1baa2-126">O número de arquivo de log mais baixo a ser reproduzido de *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="1baa2-126">The lowest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="1baa2-127">A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1baa2-127">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="1baa2-128">Isso pode ser alterado em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="1baa2-128">This may change in future versions.</span></span>

<span data-ttu-id="1baa2-129">*genHigh*</span><span class="sxs-lookup"><span data-stu-id="1baa2-129">*genHigh*</span></span>

<span data-ttu-id="1baa2-130">O número do arquivo de log mais alto a ser reproduzido de *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="1baa2-130">The highest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="1baa2-131">A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1baa2-131">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="1baa2-132">Isso pode ser alterado em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="1baa2-132">This may change in future versions.</span></span>

<span data-ttu-id="1baa2-133">*PFN*</span><span class="sxs-lookup"><span data-stu-id="1baa2-133">*pfn*</span></span>

<span data-ttu-id="1baa2-134">O retorno de chamada de status para relatar o progresso da recuperação.</span><span class="sxs-lookup"><span data-stu-id="1baa2-134">The status callback, to report progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="1baa2-135">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1baa2-135">Return Value</span></span>

<span data-ttu-id="1baa2-136">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="1baa2-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1baa2-137">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1baa2-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1baa2-138">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1baa2-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="1baa2-139">Description</span><span class="sxs-lookup"><span data-stu-id="1baa2-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1baa2-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1baa2-141">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1baa2-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1baa2-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="1baa2-143">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="1baa2-143">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-144">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1baa2-144">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1baa2-145">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1baa2-145">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="1baa2-146">Isso pode ocorrer para <strong>JetExternalRestore</strong>, e assim por diante, quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> não forem especificados ou não forem ambos não especificados.</span><span class="sxs-lookup"><span data-stu-id="1baa2-146">This can happen for <strong>JetExternalRestore</strong>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="1baa2-147">Ou seja, eles devem corresponder e ser especificados ou ambos não especificados.</span><span class="sxs-lookup"><span data-stu-id="1baa2-147">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="1baa2-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="1baa2-149">Isso indica que o banco de dados foi corrompido ou um arquivo não reconhecido.</span><span class="sxs-lookup"><span data-stu-id="1baa2-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="1baa2-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="1baa2-151">A operação falhou porque não pôde abrir o arquivo solicitado porque ele não foi encontrado no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="1baa2-151">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1baa2-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="1baa2-153">A operação falhou porque o caminho especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="1baa2-153">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-154">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="1baa2-154">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="1baa2-155">Esse erro será retornado se o arquivo de banco de dados especificado durante a restauração não for um banco de dados cujo backup foi feito com backup externo.</span><span class="sxs-lookup"><span data-stu-id="1baa2-155">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-156">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="1baa2-156">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="1baa2-157">Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log abaixo especificada pelo <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="1baa2-157">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-158">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="1baa2-158">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="1baa2-159">Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log acima especificada em <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="1baa2-159">This error is returned if one fo the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-160">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="1baa2-160">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="1baa2-161">O <em>szTargetInstanceLogPath</em> especificado não pertence a uma instância inicializada.</span><span class="sxs-lookup"><span data-stu-id="1baa2-161">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="1baa2-162">Esse erro só será retornado no Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="1baa2-162">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-163">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="1baa2-163">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="1baa2-164">O mecanismo de banco de dados não pode executar restauração externa ou recuperação de hardware no modo de instância única.</span><span class="sxs-lookup"><span data-stu-id="1baa2-164">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="1baa2-165">Esse erro só será retornado no Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="1baa2-165">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1baa2-166">Em caso de sucesso, todos os bancos de dados do *rgrstmap* são completamente recuperados e em um estado limpo ou consistente.</span><span class="sxs-lookup"><span data-stu-id="1baa2-166">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="1baa2-167">Neste ponto, o banco de dados pode ser remontado em uma instância existente.</span><span class="sxs-lookup"><span data-stu-id="1baa2-167">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="1baa2-168">Em caso de falha, o mecanismo não pôde recuperar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1baa2-168">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="1baa2-169">O banco de dados está em um estado inválido e, para tentar a recuperação complexa, todo o banco de dados deve ser restaurado novamente.</span><span class="sxs-lookup"><span data-stu-id="1baa2-169">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="1baa2-170">Normalmente, a origem de tal situação é a corrupção de disco ou log, ou alguma outra forma de gerenciamento de ingestão de log ou um conjunto de logs não contínuo.</span><span class="sxs-lookup"><span data-stu-id="1baa2-170">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1baa2-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="1baa2-171">Remarks</span></span>

<span data-ttu-id="1baa2-172">Para entender como funciona uma recuperação "rígida", você deve entender que há três fases de recuperação, e a segunda fase pode ter duas partes.</span><span class="sxs-lookup"><span data-stu-id="1baa2-172">To understand how a "hard" recovery works, you must understand that there are three phases of recovery, and the second phase can have two parts.</span></span> <span data-ttu-id="1baa2-173">Na fase I, os logs são necessários para colocar um banco de dados de backup em consistência (ou um conjunto inicial de logs incrementais pode ser usado).</span><span class="sxs-lookup"><span data-stu-id="1baa2-173">In Phase I, logs are required to bring a backed up database to consistency (or an initial set of incremental logs can be used).</span></span> <span data-ttu-id="1baa2-174">Na fase II, todos os logs de roll-forward adicionais disponíveis são consumidos para tornar o banco de dados consistente.</span><span class="sxs-lookup"><span data-stu-id="1baa2-174">In Phase II, any additional roll forward logs that are available are consumed to make the database consistent.</span></span> <span data-ttu-id="1baa2-175">Também há uma repetição dos logs adicionais de roll-forward.</span><span class="sxs-lookup"><span data-stu-id="1baa2-175">There is also a replay of the additional roll forward logs.</span></span> <span data-ttu-id="1baa2-176">A fase III é a fase desfazer da recuperação.</span><span class="sxs-lookup"><span data-stu-id="1baa2-176">Phase III is the undo phase of recovery.</span></span>

<span data-ttu-id="1baa2-177">Fase I: a reprodução do conjunto de logs que devem ser restaurados para que o banco de dados seja trazido para um estado consistente (ou um conjunto inicial de arquivos de log) seja executado.</span><span class="sxs-lookup"><span data-stu-id="1baa2-177">Phase I: The replay of the set of logs that must be restored for the database to be brought to a consistent state (or an initial set of log files) is performed.</span></span> <span data-ttu-id="1baa2-178">Basicamente, essa é a repetição do conjunto de arquivos de log que não são opcionais para os bancos de dados que estão sendo restaurados.</span><span class="sxs-lookup"><span data-stu-id="1baa2-178">Basically, this is the replay of the set of log files that are not optional for the databases being restored.</span></span> <span data-ttu-id="1baa2-179">Se houver logs ausentes desse intervalo de logs, a restauração falhará.</span><span class="sxs-lookup"><span data-stu-id="1baa2-179">If there are missing logs from this range of logs then the restore will fail.</span></span> <span data-ttu-id="1baa2-180">Esses logs devem ser colocados no diretório especificado no parâmetro *szBackupLogPath* .</span><span class="sxs-lookup"><span data-stu-id="1baa2-180">These logs should be put in the directory specified in the *szBackupLogPath* parameter.</span></span>

<span data-ttu-id="1baa2-181">Fase II: opcionalmente, pode haver alguns conjuntos de arquivos de log que são arquivos de log de roll-forward que vêm de backups incrementais ou diferenciais e dos arquivos de log de uma instância ativa.</span><span class="sxs-lookup"><span data-stu-id="1baa2-181">Phase II: Optionally, there may be some sets of log files that are roll forward log files that come from incremental or differential backups and from the log files of an active instance.</span></span> <span data-ttu-id="1baa2-182">No caso de arquivos de log de backups incrementais ou diferenciais, os arquivos de log podem ser colocados nos diretórios especificados nos parâmetros *szBackupLogPath* ou *szTargetInstanceLogPath* , sendo que o primeiro é o diretório recomendado.</span><span class="sxs-lookup"><span data-stu-id="1baa2-182">In the case of log files from incremental or differential backups, the log files can be placed in the directories specified in either the *szBackupLogPath* or the *szTargetInstanceLogPath* parameters, with the former being the recommended directory.</span></span> <span data-ttu-id="1baa2-183">Os logs usados para a fase de roll-forward (fase II) devem vir da mesma série de logs reproduzidos durante a fase I e devem ter um incremento contínuo de números de log sem intervalos da fase I logs.</span><span class="sxs-lookup"><span data-stu-id="1baa2-183">The logs used for the roll forward phase (phase II) should come from the same series of logs played during Phase I and should have continuously incrementing log numbers with no gaps from the Phase I logs.</span></span> <span data-ttu-id="1baa2-184">Para reproduzir um banco de dados para ser totalmente atualizado com os arquivos de log que estão sendo usados atualmente por uma instância ativa, os parâmetros *szTargetInstanceLogPath* e *szTargetInstanceCheckpointPath* devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="1baa2-184">To play a database to be fully up to date with the log files currently being used by an active instance, the *szTargetInstanceLogPath* and *szTargetInstanceCheckpointPath* parameters must be specified.</span></span> <span data-ttu-id="1baa2-185">Isso pode ser feito mesmo enquanto outros bancos de dados são anexados a esse conjunto de logs.</span><span class="sxs-lookup"><span data-stu-id="1baa2-185">This can be done even while other databases are attached to that log set.</span></span>

<span data-ttu-id="1baa2-186">Fase III: na fase final de recuperação, todas as transações não confirmadas são revertidas, o que requer a geração de novos arquivos de log e a atualização do arquivo de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="1baa2-186">Phase III: In the final phase of recovery, any uncommitted transactions are rolled back, which requires generating new log files and updating the checkpoint file.</span></span> <span data-ttu-id="1baa2-187">Às vezes, essa fase é chamada de "desfazer".</span><span class="sxs-lookup"><span data-stu-id="1baa2-187">This phase is sometimes referred to as "undo".</span></span> <span data-ttu-id="1baa2-188">O caminho do arquivo de ponto de verificação a ser usado durante essa fase é o caminho análogo ao local do log da fase III, ou seja, se *szLogPath* for usado para a fase III, *szCheckpointFilePath* será usado se *szTargetInstanceLogPath* for usado para a fase III de recuperação *szTargetInstanceCheckpointPath* será usado.</span><span class="sxs-lookup"><span data-stu-id="1baa2-188">The checkpoint file path to use during this phase is the path analogous to the phase III log location, that is, if *szLogPath* is used for Phase III, *szCheckpointFilePath* will be used, if *szTargetInstanceLogPath* is used for phase III of recovery *szTargetInstanceCheckpointPath* will be used.</span></span>

<span data-ttu-id="1baa2-189">Para entender como os caminhos funcionam, use este gráfico de fluxo:</span><span class="sxs-lookup"><span data-stu-id="1baa2-189">To understand how the paths work, use this flow chart:</span></span>

<span data-ttu-id="1baa2-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span><span class="sxs-lookup"><span data-stu-id="1baa2-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span></span>

#### <a name="requirements"></a><span data-ttu-id="1baa2-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1baa2-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1baa2-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1baa2-193">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1baa2-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-194"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="1baa2-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1baa2-195">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1baa2-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-196"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="1baa2-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1baa2-197">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1baa2-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-198"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="1baa2-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1baa2-199">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1baa2-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1baa2-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1baa2-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1baa2-201">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1baa2-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1baa2-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1baa2-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1baa2-203">Implementado como <strong>JetExternalRestoreW</strong> (Unicode) e <strong>JetExternalRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1baa2-203">Implemented as <strong>JetExternalRestoreW</strong> (Unicode) and <strong>JetExternalRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1baa2-204">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1baa2-204">See Also</span></span>

[<span data-ttu-id="1baa2-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1baa2-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1baa2-206">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="1baa2-206">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="1baa2-207">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="1baa2-207">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="1baa2-208">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="1baa2-208">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="1baa2-209">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="1baa2-209">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="1baa2-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="1baa2-210">JetInit</span></span>](./jetinit-function.md)
