---
description: 'Saiba mais sobre: função JetCloseFile'
title: Função JetCloseFile
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370581"
---
# <a name="jetclosefile-function"></a><span data-ttu-id="180a9-103">Função JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="180a9-103">JetCloseFile Function</span></span>


<span data-ttu-id="180a9-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="180a9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefile-function"></a><span data-ttu-id="180a9-105">Função JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="180a9-105">JetCloseFile Function</span></span>

<span data-ttu-id="180a9-106">A função **JetCloseFile** fecha um arquivo que foi aberto com [JetOpenFile](./jetopenfile-function.md) depois que os dados desse arquivo foram extraídos usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="180a9-106">The **JetCloseFile** function closes a file that was opened with [JetOpenFile](./jetopenfile-function.md) after the data from that file has been extracted using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="180a9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="180a9-107">Parameters</span></span>

<span data-ttu-id="180a9-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="180a9-108">*hfFile*</span></span>

<span data-ttu-id="180a9-109">O identificador do arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="180a9-109">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="180a9-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="180a9-110">Return Value</span></span>

<span data-ttu-id="180a9-111">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="180a9-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="180a9-112">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="180a9-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="180a9-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="180a9-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="180a9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="180a9-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="180a9-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="180a9-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="180a9-116">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="180a9-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="180a9-117">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="180a9-117">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="180a9-118">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="180a9-118">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="180a9-119">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="180a9-119">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="180a9-120">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="180a9-120">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="180a9-121">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="180a9-121">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="180a9-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="180a9-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="180a9-123">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="180a9-123">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="180a9-124">Isso pode ocorrer para <strong>JetCloseFile</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="180a9-124">This can happen for <strong>JetCloseFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="180a9-125">O identificador de instância especificado é inválido (Windows XP e versões posteriores),</span><span class="sxs-lookup"><span data-stu-id="180a9-125">The specified instance handle is invalid (Windows XP and later releases),</span></span></p></li>
<li><p><span data-ttu-id="180a9-126">O identificador de arquivo especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="180a9-126">The specified file handle is invalid.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="180a9-127">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="180a9-127">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="180a9-128">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="180a9-128">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="180a9-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="180a9-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="180a9-130">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="180a9-130">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="180a9-131">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="180a9-131">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="180a9-132">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="180a9-132">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="180a9-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="180a9-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="180a9-134">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="180a9-134">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="180a9-135">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="180a9-135">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="180a9-136">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="180a9-136">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="180a9-137">Em caso de sucesso, o identificador do arquivo é fechado.</span><span class="sxs-lookup"><span data-stu-id="180a9-137">On success, the file handle is closed.</span></span> <span data-ttu-id="180a9-138">Se um arquivo de banco de dados foi fechado, o arquivo de patch do banco de dados associado (se houver) será destruído.</span><span class="sxs-lookup"><span data-stu-id="180a9-138">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="180a9-139">Em caso de falha, nenhuma alteração ocorre.</span><span class="sxs-lookup"><span data-stu-id="180a9-139">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="180a9-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="180a9-140">Remarks</span></span>

<span data-ttu-id="180a9-141">O mecanismo de banco de dados atualmente dá suporte apenas a um arquivo aberto por meio de [JetOpenFile](./jetopenfile-function.md) por vez.</span><span class="sxs-lookup"><span data-stu-id="180a9-141">The database engine currently only supports one open file through [JetOpenFile](./jetopenfile-function.md) at a time.</span></span> <span data-ttu-id="180a9-142">Se um identificador de arquivo for aberto usando [JetOpenFile](./jetopenfile-function.md) , ele deverá ser fechado usando **JetCloseFile** antes que outro arquivo possa ser aberto.</span><span class="sxs-lookup"><span data-stu-id="180a9-142">If a file handle is opened using [JetOpenFile](./jetopenfile-function.md) then it must be closed using **JetCloseFile** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="180a9-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="180a9-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="180a9-144"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="180a9-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="180a9-145">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="180a9-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="180a9-146"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="180a9-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="180a9-147">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="180a9-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="180a9-148"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="180a9-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="180a9-149">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="180a9-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="180a9-150"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="180a9-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="180a9-151">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="180a9-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="180a9-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="180a9-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="180a9-153">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="180a9-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="180a9-154">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="180a9-154">See Also</span></span>

[<span data-ttu-id="180a9-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="180a9-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="180a9-156">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="180a9-156">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="180a9-157">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="180a9-157">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="180a9-158">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="180a9-158">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="180a9-159">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="180a9-159">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="180a9-160">JetStopService</span><span class="sxs-lookup"><span data-stu-id="180a9-160">JetStopService</span></span>](./jetstopservice-function.md)
