---
description: 'Saiba mais sobre: função JetOpenFileInstance'
title: Função JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781383"
---
# <a name="jetopenfileinstance-function"></a><span data-ttu-id="5caf1-103">Função JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-103">JetOpenFileInstance Function</span></span>


<span data-ttu-id="5caf1-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5caf1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfileinstance-function"></a><span data-ttu-id="5caf1-105">Função JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-105">JetOpenFileInstance Function</span></span>

<span data-ttu-id="5caf1-106">A função **JetOpenFileInstance** abre um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações de uma instância ativa com a finalidade de executar um backup difuso de streaming.</span><span class="sxs-lookup"><span data-stu-id="5caf1-106">The **JetOpenFileInstance** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="5caf1-107">Os dados desses arquivos podem, subsequentemente, ser lidos por meio do identificador retornado usando [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="5caf1-107">The data from these files can subsequently be read through the returned handle using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span> <span data-ttu-id="5caf1-108">O identificador retornado deve ser fechado usando [JetCloseFileInstance](./jetclosefileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="5caf1-108">The returned handle must be closed using [JetCloseFileInstance](./jetclosefileinstance-function.md).</span></span> <span data-ttu-id="5caf1-109">Um backup externo da instância deve ter sido iniciado anteriormente usando [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="5caf1-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span></span>

<span data-ttu-id="5caf1-110">**Windows XP:** o **JetOpenFileInstance** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="5caf1-110">**Windows XP:**  **JetOpenFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="5caf1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5caf1-111">Parameters</span></span>

<span data-ttu-id="5caf1-112">*cópia*</span><span class="sxs-lookup"><span data-stu-id="5caf1-112">*instance*</span></span>

<span data-ttu-id="5caf1-113">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="5caf1-113">The instance to use for this call.</span></span>

<span data-ttu-id="5caf1-114">Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="5caf1-114">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="5caf1-115">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="5caf1-115">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="5caf1-116">Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="5caf1-116">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="5caf1-117">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="5caf1-117">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="5caf1-118">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="5caf1-118">*szFileName*</span></span>

<span data-ttu-id="5caf1-119">O caminho relativo ou absoluto para um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações gerenciado pela instância do que é lido para backup.</span><span class="sxs-lookup"><span data-stu-id="5caf1-119">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that is read for backup.</span></span>

<span data-ttu-id="5caf1-120">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="5caf1-120">*phfFile*</span></span>

<span data-ttu-id="5caf1-121">Ponteiro para o buffer de saída que recebe um identificador para o arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="5caf1-121">Pointer to the output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="5caf1-122">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="5caf1-122">*pulFileSizeLow*</span></span>

<span data-ttu-id="5caf1-123">Ponteiro para o buffer de saída que recebe os 32 bits menos significativos do tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5caf1-123">Pointer to the output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="5caf1-124">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="5caf1-124">*pulFileSizeHigh*</span></span>

<span data-ttu-id="5caf1-125">Ponteiro para o buffer de saída que recebe os 32 bits mais significativos do tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5caf1-125">Pointer to the output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="5caf1-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5caf1-126">Return Value</span></span>

<span data-ttu-id="5caf1-127">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="5caf1-127">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5caf1-128">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5caf1-128">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5caf1-129">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5caf1-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="5caf1-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="5caf1-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5caf1-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5caf1-132">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5caf1-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-133">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="5caf1-133">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="5caf1-134">A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="5caf1-134">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="5caf1-135">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5caf1-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5caf1-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5caf1-137">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="5caf1-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-138">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="5caf1-138">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="5caf1-139">A operação falhou porque não pôde abrir o arquivo solicitado devido a uma violação de compartilhamento ou privilégios insuficientes.</span><span class="sxs-lookup"><span data-stu-id="5caf1-139">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-140">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="5caf1-140">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="5caf1-141">A operação falhou porque não pôde abrir o arquivo solicitado porque ele não foi encontrado no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="5caf1-141">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="5caf1-142">Esse erro só será retornado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5caf1-142">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-143">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="5caf1-143">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="5caf1-144">A operação de backup falhou porque ela foi chamada fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="5caf1-144">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-145">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="5caf1-145">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="5caf1-146">A operação falhou porque o caminho especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5caf1-146">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5caf1-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5caf1-148">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="5caf1-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="5caf1-149">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5caf1-149">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5caf1-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5caf1-151">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5caf1-151">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="5caf1-152">Isso pode ocorrer para <strong>JetOpenFileInstance</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="5caf1-152">This can happen for <strong>JetOpenFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="5caf1-153">O identificador de instância especificado é inválido (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="5caf1-153">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="5caf1-154">O parâmetro filename especificado é nulo ou uma cadeia de caracteres de comprimento zero (Windows XP e versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="5caf1-154">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-155">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="5caf1-155">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="5caf1-156">Não foi possível abrir o arquivo solicitado para backup porque ele não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5caf1-156">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="5caf1-157">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5caf1-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-158">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="5caf1-158">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="5caf1-159">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="5caf1-159">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5caf1-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5caf1-161">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="5caf1-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-162">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="5caf1-162">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="5caf1-163">A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</span><span class="sxs-lookup"><span data-stu-id="5caf1-163">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="5caf1-164"><strong>JetOpenFileInstance</strong> retornará JET_errOutOfMemory se for feita uma tentativa de abrir outro arquivo antes que o arquivo anterior aberto usando <strong>JetOpenFileInstance</strong> tenha sido fechado pelo <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="5caf1-164"><strong>JetOpenFileInstance</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFileInstance</strong> has been closed by <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span></span> <span data-ttu-id="5caf1-165">No momento, há suporte para apenas um identificador de arquivo pendente.</span><span class="sxs-lookup"><span data-stu-id="5caf1-165">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5caf1-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5caf1-167">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="5caf1-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-168">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="5caf1-168">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="5caf1-169">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="5caf1-169">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5caf1-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5caf1-171">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="5caf1-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5caf1-172">Em caso de sucesso, será retornado um identificador para o arquivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="5caf1-172">On success, a handle to the requested file is returned.</span></span> <span data-ttu-id="5caf1-173">Se o identificador for para um arquivo de banco de dados, esse arquivo de banco de dados será preparado para um backup de streaming que pode resultar na criação de um arquivo de patch de banco de dados no mesmo local que o arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5caf1-173">If the handle is for a database file, that database file will be prepared for a streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="5caf1-174">O arquivo de patch do banco de dados tem exatamente o mesmo caminho e nome de arquivo do banco de dados, mas com um. Extensão PAT.</span><span class="sxs-lookup"><span data-stu-id="5caf1-174">The database patch file has the exact same path and filename as the database file but with a .PAT extension.</span></span> <span data-ttu-id="5caf1-175">O tamanho do arquivo também será retornado.</span><span class="sxs-lookup"><span data-stu-id="5caf1-175">The size of the file will also be returned.</span></span>

<span data-ttu-id="5caf1-176">Em caso de falha, o estado dos buffers de saída será indefinido.</span><span class="sxs-lookup"><span data-stu-id="5caf1-176">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="5caf1-177">Um arquivo de patch de banco de dados pode ser criado temporariamente no disco e qualquer arquivo existente no local do arquivo de patch pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5caf1-177">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="5caf1-178">A falha resultará no cancelamento de todo o processo de backup da instância.</span><span class="sxs-lookup"><span data-stu-id="5caf1-178">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="5caf1-179">No Windows XP e versões posteriores, o backup não será cancelado se for feita uma tentativa de fazer backup de um banco de dados que não foi anexado à instância no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="5caf1-179">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="5caf1-180">**Aviso**  Por motivos de segurança, é importante observar que o **JetOpenFileInstance** não verifica se o caminho do arquivo solicitado está associado ao conjunto de arquivos cujo backup é feito para a instância.</span><span class="sxs-lookup"><span data-stu-id="5caf1-180">**Warning**  For security reasons, it is important to note that **JetOpenFileInstance** does not verify that the requested file path is associated with the set of files that are backed up for the instance.</span></span> <span data-ttu-id="5caf1-181">Como resultado, é possível usar essa função para acessar qualquer arquivo que possa ser aberto pelo contexto de segurança atual do thread.</span><span class="sxs-lookup"><span data-stu-id="5caf1-181">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="5caf1-182">É imperativo que o aplicativo restrinja os caminhos passados para essa função para um conjunto conhecido de bons caminhos de arquivo ou uma divulgação de ataque de informações poderia ser possível.</span><span class="sxs-lookup"><span data-stu-id="5caf1-182">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5caf1-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="5caf1-183">Remarks</span></span>

<span data-ttu-id="5caf1-184">Os buffers de saída de identificador e de tamanho de arquivo devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="5caf1-184">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="5caf1-185">Se eles não estiverem presentes, o mecanismo falhará porque os parâmetros do buffer de saída não são validados.</span><span class="sxs-lookup"><span data-stu-id="5caf1-185">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="5caf1-186">Neste momento, apenas um arquivo pode ser aberto para backup a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="5caf1-186">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="5caf1-187">**JetOpenFileInstance** não declara o privilégio de backup antes de abrir o arquivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="5caf1-187">**JetOpenFileInstance** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="5caf1-188">O tamanho do arquivo a ser lido como relatado por essa função pode não corresponder ao tamanho do arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="5caf1-188">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="5caf1-189">No Windows XP e versões posteriores, informações extras podem ser acrescentadas a um arquivo de banco de dados que é usado pelo mecanismo de banco de dados durante uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="5caf1-189">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="5caf1-190">Como tal, o aplicativo deve confiar apenas no tamanho do arquivo retornado por **JetOpenFileInstance** ou no número real de bytes de dados retornados por [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="5caf1-190">As such, the application should only rely on the file size returned by **JetOpenFileInstance** or on the actual number of bytes of data returned by [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5caf1-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5caf1-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5caf1-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5caf1-193">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5caf1-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-194"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5caf1-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5caf1-195">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5caf1-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-196"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5caf1-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5caf1-197">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5caf1-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-198"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="5caf1-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5caf1-199">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5caf1-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5caf1-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5caf1-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5caf1-201">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5caf1-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5caf1-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5caf1-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5caf1-203">Implementado como <strong>JetOpenFileInstanceW</strong> (Unicode) e <strong>JetOpenFileInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5caf1-203">Implemented as <strong>JetOpenFileInstanceW</strong> (Unicode) and <strong>JetOpenFileInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5caf1-204">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5caf1-204">See Also</span></span>

[<span data-ttu-id="5caf1-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5caf1-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5caf1-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="5caf1-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="5caf1-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5caf1-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5caf1-208">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="5caf1-208">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="5caf1-209">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-209">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="5caf1-210">JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-210">JetCloseFileInstance</span></span>](./jetclosefileinstance-function.md)  
[<span data-ttu-id="5caf1-211">JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-211">JetGetAttachInfoInstance</span></span>](./jetgetattachinfoinstance-function.md)  
[<span data-ttu-id="5caf1-212">JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-212">JetGetLogInfoInstance</span></span>](./jetgetloginfoinstance-function.md)  
[<span data-ttu-id="5caf1-213">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-213">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="5caf1-214">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-214">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="5caf1-215">JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="5caf1-215">JetTruncateLogInstance</span></span>](./jettruncateloginstance-function.md)
