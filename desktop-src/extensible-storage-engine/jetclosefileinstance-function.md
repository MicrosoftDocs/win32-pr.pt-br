---
description: 'Saiba mais sobre: função JetCloseFileInstance'
title: Função JetCloseFileInstance
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501294"
---
# <a name="jetclosefileinstance-function"></a><span data-ttu-id="92e67-103">Função JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="92e67-103">JetCloseFileInstance Function</span></span>


<span data-ttu-id="92e67-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="92e67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefileinstance-function"></a><span data-ttu-id="92e67-105">Função JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="92e67-105">JetCloseFileInstance Function</span></span>

<span data-ttu-id="92e67-106">A função **JetCloseFileInstance** fecha um arquivo que foi aberto com [JetOpenFileInstance](./jetopenfileinstance-function.md) depois que os dados desse arquivo foram extraídos usando [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="92e67-106">The **JetCloseFileInstance** function closes a file that was opened with [JetOpenFileInstance](./jetopenfileinstance-function.md) after the data from that file has been extracted using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="92e67-107">**Windows XP: o JetCloseFileInstance** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="92e67-107">**Windows XP:  JetCloseFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="92e67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92e67-108">Parameters</span></span>

<span data-ttu-id="92e67-109">*cópia*</span><span class="sxs-lookup"><span data-stu-id="92e67-109">*instance*</span></span>

<span data-ttu-id="92e67-110">A instância a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="92e67-110">The instance to use for this call.</span></span>

<span data-ttu-id="92e67-111">Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="92e67-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="92e67-112">O uso dessa instância global é implícito nesse caso.</span><span class="sxs-lookup"><span data-stu-id="92e67-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="92e67-113">Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte.</span><span class="sxs-lookup"><span data-stu-id="92e67-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="92e67-114">Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="92e67-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="92e67-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="92e67-115">*hfFile*</span></span>

<span data-ttu-id="92e67-116">O identificador do arquivo a ser lido.</span><span class="sxs-lookup"><span data-stu-id="92e67-116">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="92e67-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="92e67-117">Return Value</span></span>

<span data-ttu-id="92e67-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="92e67-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="92e67-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="92e67-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92e67-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="92e67-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="92e67-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="92e67-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92e67-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="92e67-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="92e67-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="92e67-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e67-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="92e67-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="92e67-125">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="92e67-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e67-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="92e67-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="92e67-127">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="92e67-127">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="92e67-128">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="92e67-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e67-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="92e67-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="92e67-130">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="92e67-130">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="92e67-131">Isso pode ocorrer para <strong>JetCloseFileInstance</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="92e67-131">This can happen for <strong>JetCloseFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="92e67-132">O identificador de instância especificado é inválido (Windows XP e versões posteriores)</span><span class="sxs-lookup"><span data-stu-id="92e67-132">The specified instance handle is invalid (Windows XP and later releases)</span></span></p></li>
<li><p><span data-ttu-id="92e67-133">O identificador de arquivo especificado é inválido</span><span class="sxs-lookup"><span data-stu-id="92e67-133">The specified file handle is invalid</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e67-134">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="92e67-134">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="92e67-135">A operação falhou porque nenhum backup externo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="92e67-135">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e67-136">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="92e67-136">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="92e67-137">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="92e67-137">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e67-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="92e67-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="92e67-139">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="92e67-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e67-140">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="92e67-140">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="92e67-141">A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</span><span class="sxs-lookup"><span data-stu-id="92e67-141">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e67-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="92e67-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="92e67-143">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="92e67-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92e67-144">Em caso de sucesso, o identificador do arquivo é fechado.</span><span class="sxs-lookup"><span data-stu-id="92e67-144">On success, the file handle is closed.</span></span> <span data-ttu-id="92e67-145">Se um arquivo de banco de dados foi fechado, o arquivo de patch do banco de dados associado (se houver) será destruído.</span><span class="sxs-lookup"><span data-stu-id="92e67-145">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="92e67-146">Em caso de falha, nenhuma alteração ocorre.</span><span class="sxs-lookup"><span data-stu-id="92e67-146">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="92e67-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="92e67-147">Remarks</span></span>

<span data-ttu-id="92e67-148">O mecanismo de banco de dados atualmente dá suporte apenas a um arquivo aberto por meio de [JetOpenFileInstance](./jetopenfileinstance-function.md) por vez.</span><span class="sxs-lookup"><span data-stu-id="92e67-148">The database engine currently only supports one open file through [JetOpenFileInstance](./jetopenfileinstance-function.md) at a time.</span></span> <span data-ttu-id="92e67-149">Se um identificador de arquivo for aberto usando [JetOpenFileInstance](./jetopenfileinstance-function.md) , ele deverá ser fechado usando **JetCloseFileInstance** antes que outro arquivo possa ser aberto.</span><span class="sxs-lookup"><span data-stu-id="92e67-149">If a file handle is opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) then it must be closed using **JetCloseFileInstance** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="92e67-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e67-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92e67-151"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="92e67-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="92e67-152">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="92e67-152">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e67-153"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="92e67-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="92e67-154">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="92e67-154">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e67-155"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="92e67-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="92e67-156">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="92e67-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92e67-157"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="92e67-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="92e67-158">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="92e67-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92e67-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="92e67-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="92e67-160">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="92e67-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="92e67-161">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="92e67-161">See Also</span></span>

[<span data-ttu-id="92e67-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="92e67-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="92e67-163">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="92e67-163">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="92e67-164">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="92e67-164">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="92e67-165">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="92e67-165">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="92e67-166">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="92e67-166">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="92e67-167">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="92e67-167">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
