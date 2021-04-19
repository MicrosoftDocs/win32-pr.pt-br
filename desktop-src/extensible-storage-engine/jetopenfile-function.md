---
description: 'Saiba mais sobre: função JetOpenFile'
title: Função JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783757"
---
# <a name="jetopenfile-function"></a><span data-ttu-id="71495-103">Função JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="71495-103">JetOpenFile Function</span></span>


<span data-ttu-id="71495-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="71495-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfile-function"></a><span data-ttu-id="71495-105">Função JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="71495-105">JetOpenFile Function</span></span>

<span data-ttu-id="71495-106">A função **JetOpenFile** abre um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações de uma instância ativa com a finalidade de executar um backup difuso de streaming.</span><span class="sxs-lookup"><span data-stu-id="71495-106">The **JetOpenFile** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="71495-107">Os dados desses arquivos podem, subsequentemente, ser lidos por meio do identificador retornado usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="71495-107">The data from these files can subsequently be read through the returned handle using [JetReadFile](./jetreadfile-function.md).</span></span> <span data-ttu-id="71495-108">O identificador retornado deve ser fechado usando [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="71495-108">The returned handle must be closed using [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="71495-109">Um backup externo da instância deve ter sido iniciado anteriormente usando [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="71495-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="71495-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71495-110">Parameters</span></span>

<span data-ttu-id="71495-111">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="71495-111">*szFileName*</span></span>

<span data-ttu-id="71495-112">O caminho relativo ou absoluto para um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações gerenciado pela instância do que será lida para backup.</span><span class="sxs-lookup"><span data-stu-id="71495-112">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that will be read for backup.</span></span>

<span data-ttu-id="71495-113">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="71495-113">*phfFile*</span></span>

<span data-ttu-id="71495-114">O buffer de saída que recebe um identificador para o arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="71495-114">The output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="71495-115">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="71495-115">*pulFileSizeLow*</span></span>

<span data-ttu-id="71495-116">O buffer de saída que recebe os 32 bits menos significativos do tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="71495-116">The output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="71495-117">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="71495-117">*pulFileSizeHigh*</span></span>

<span data-ttu-id="71495-118">O buffer de saída que recebe os 32 bits mais significativos do tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="71495-118">The output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="71495-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="71495-119">Return Value</span></span>

<span data-ttu-id="71495-120">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="71495-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="71495-121">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="71495-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71495-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="71495-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="71495-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="71495-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71495-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="71495-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="71495-125">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="71495-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-126">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="71495-126">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="71495-127">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="71495-127">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="71495-128">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="71495-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="71495-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="71495-130">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="71495-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-131">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="71495-131">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="71495-132">A operação falhou porque não pôde abrir o arquivo solicitado devido a uma violação de compartilhamento ou privilégios insuficientes.</span><span class="sxs-lookup"><span data-stu-id="71495-132">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-133">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="71495-133">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="71495-134">A operação falhou porque não pôde abrir o arquivo solicitado porque ele não foi encontrado no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="71495-134">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="71495-135">Esse erro só será retornado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="71495-135">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="71495-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="71495-137">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="71495-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="71495-138">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="71495-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="71495-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="71495-140">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="71495-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="71495-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="71495-142">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="71495-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="71495-143">Isso pode ocorrer para <strong>JetOpenFile</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="71495-143">This can happen for <strong>JetOpenFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="71495-144">O identificador de instância especificado é inválido (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="71495-144">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="71495-145">O parâmetro filename especificado é nulo ou uma cadeia de caracteres de comprimento zero (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="71495-145">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-146">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="71495-146">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="71495-147">A operação falhou porque o caminho especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="71495-147">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-148">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="71495-148">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="71495-149">Não foi possível abrir o arquivo solicitado para backup porque ele não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="71495-149">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="71495-150">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="71495-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-151">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="71495-151">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="71495-152">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="71495-152">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="71495-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="71495-154">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="71495-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-155">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="71495-155">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="71495-156">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="71495-156">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="71495-157"><strong>JetOpenFile</strong> retornará JET_errOutOfMemory se for feita uma tentativa de abrir outro arquivo antes que o arquivo anterior aberto usando <strong>JetOpenFile</strong> tenha sido fechado pelo <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span><span class="sxs-lookup"><span data-stu-id="71495-157"><strong>JetOpenFile</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFile</strong> has been closed by <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span></span> <span data-ttu-id="71495-158">No momento, há suporte para apenas um identificador de arquivo pendente.</span><span class="sxs-lookup"><span data-stu-id="71495-158">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-159">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="71495-159">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="71495-160">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="71495-160">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="71495-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="71495-162">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="71495-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span> <span data-ttu-id="71495-163">JET_errRestoreInProgress não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="71495-163">JET_errRestoreInProgress It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71495-164">Em caso de sucesso, será retornado um identificador para o arquivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="71495-164">On success, a handle to the requested file will be returned.</span></span> <span data-ttu-id="71495-165">Se o identificador for para um arquivo de banco de dados, esse arquivo de banco de dados será preparado para o backup de streaming, o que pode resultar na criação de um arquivo de patch de banco de dados no mesmo local que o arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71495-165">If the handle is for a database file, that database file will be prepared for streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="71495-166">O arquivo de patch do banco de dados tem exatamente o mesmo caminho e nome de arquivo do banco de dados, mas tem um. Extensão PAT.</span><span class="sxs-lookup"><span data-stu-id="71495-166">The database patch file has the exact same path and filename as the database file, but has a .PAT extension.</span></span> <span data-ttu-id="71495-167">O tamanho do arquivo também será retornado.</span><span class="sxs-lookup"><span data-stu-id="71495-167">The size of the file will also be returned.</span></span>

<span data-ttu-id="71495-168">Em caso de falha, o estado dos buffers de saída será indefinido.</span><span class="sxs-lookup"><span data-stu-id="71495-168">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="71495-169">Um arquivo de patch de banco de dados pode ser criado temporariamente no disco e qualquer arquivo existente no local do arquivo de patch pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="71495-169">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="71495-170">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="71495-170">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="71495-171">No Windows XP e versões posteriores, o backup não será cancelado se for feita uma tentativa de fazer backup de um banco de dados que não foi anexado à instância no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="71495-171">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="71495-172">**Aviso**  Por motivos de segurança, é importante observar que o **JetOpenFile** não verifica se o caminho do arquivo solicitado está associado ao conjunto de arquivos cujo backup deve ser feito para a instância.</span><span class="sxs-lookup"><span data-stu-id="71495-172">**Warning**  For security reasons, it is important to note that **JetOpenFile** does not verify that the requested file path is associated with the set of files that should be backed up for the instance.</span></span> <span data-ttu-id="71495-173">Como resultado, é possível usar essa função para acessar qualquer arquivo que possa ser aberto pelo contexto de segurança atual do thread.</span><span class="sxs-lookup"><span data-stu-id="71495-173">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="71495-174">É imperativo que o aplicativo restrinja os caminhos passados para essa função para um conjunto conhecido de bons caminhos de arquivo ou uma divulgação de ataque de informações poderia ser possível.</span><span class="sxs-lookup"><span data-stu-id="71495-174">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="71495-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="71495-175">Remarks</span></span>

<span data-ttu-id="71495-176">Os buffers de saída de identificador e de tamanho de arquivo devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="71495-176">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="71495-177">Se eles não estiverem presentes, o mecanismo falhará porque os parâmetros do buffer de saída não são validados.</span><span class="sxs-lookup"><span data-stu-id="71495-177">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="71495-178">Neste momento, apenas um arquivo pode ser aberto para backup a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="71495-178">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="71495-179">**JetOpenFile** não declara o privilégio de backup antes de abrir o arquivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="71495-179">**JetOpenFile** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="71495-180">O tamanho do arquivo a ser lido como relatado por essa função pode não corresponder ao tamanho do arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="71495-180">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="71495-181">No Windows XP e versões posteriores, informações extras podem ser acrescentadas a um arquivo de banco de dados que é usado pelo mecanismo de banco de dados durante uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="71495-181">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="71495-182">Como tal, o aplicativo deve confiar apenas no tamanho do arquivo retornado por **JetOpenFile** ou no número real de bytes de dados retornados por [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="71495-182">As such, the application should only rely on the file size returned by **JetOpenFile** or on the actual number of bytes of data returned by [JetReadFile](./jetreadfile-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="71495-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71495-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71495-184"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="71495-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="71495-185">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="71495-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-186"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="71495-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="71495-187">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="71495-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-188"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="71495-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="71495-189">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="71495-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-190"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="71495-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="71495-191">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="71495-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71495-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="71495-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="71495-193">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="71495-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71495-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="71495-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="71495-195">Implementado como <strong>JetOpenFileW</strong> (Unicode) e <strong>JetOpenFileA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="71495-195">Implemented as <strong>JetOpenFileW</strong> (Unicode) and <strong>JetOpenFileA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="71495-196">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="71495-196">See Also</span></span>

[<span data-ttu-id="71495-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="71495-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="71495-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="71495-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="71495-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="71495-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="71495-200">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="71495-200">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="71495-201">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="71495-201">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="71495-202">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="71495-202">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="71495-203">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="71495-203">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="71495-204">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="71495-204">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="71495-205">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="71495-205">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="71495-206">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="71495-206">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="71495-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="71495-207">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="71495-208">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="71495-208">JetTruncateLog</span></span>](./jettruncatelog-function.md)
