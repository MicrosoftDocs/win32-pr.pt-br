---
description: 'Saiba mais sobre: função JetStopBackup'
title: Função JetStopBackup
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105790385"
---
# <a name="jetstopbackup-function"></a><span data-ttu-id="9e89b-103">Função JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="9e89b-103">JetStopBackup Function</span></span>


<span data-ttu-id="9e89b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9e89b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackup-function"></a><span data-ttu-id="9e89b-105">Função JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="9e89b-105">JetStopBackup Function</span></span>

<span data-ttu-id="9e89b-106">A função **JetStopBackup** impede que qualquer atividade relacionada ao backup de streaming continue em uma instância em execução específica, encerrando assim o backup de streaming de forma previsível.</span><span class="sxs-lookup"><span data-stu-id="9e89b-106">The **JetStopBackup** function prevents any streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="9e89b-107">**Windows XP:**  Essa função é introduzida no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9e89b-107">**Windows XP:**  This function is introduced in Windows XP.</span></span>

<span data-ttu-id="9e89b-108">[JetStopService](./jetstopservice-function.md) é a chamada herdada quando apenas uma instância é permitida.</span><span class="sxs-lookup"><span data-stu-id="9e89b-108">[JetStopService](./jetstopservice-function.md) is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="9e89b-109">Nesse caso, a única instância ativa é aquela que está sendo preparada para encerramento.</span><span class="sxs-lookup"><span data-stu-id="9e89b-109">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="9e89b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e89b-110">Parameters</span></span>

<span data-ttu-id="9e89b-111">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9e89b-111">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="9e89b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9e89b-112">Return Value</span></span>

<span data-ttu-id="9e89b-113">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e89b-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9e89b-114">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9e89b-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e89b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9e89b-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="9e89b-116">Description</span><span class="sxs-lookup"><span data-stu-id="9e89b-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e89b-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9e89b-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9e89b-118">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="9e89b-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e89b-119">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="9e89b-119">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="9e89b-120">Não está claro qual instância deve ser preparada para encerramento ao usar <a href="gg269240(v=exchg.10).md">JetStopService</a> com o modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="9e89b-120">It is not clear which instance to prepare for termination when using <a href="gg269240(v=exchg.10).md">JetStopService</a> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="9e89b-121"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9e89b-121"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e89b-122">Se essa função for realizada com êxito, a instância começará a falhar quaisquer novas APIs de backup de streaming.</span><span class="sxs-lookup"><span data-stu-id="9e89b-122">If this function succeeds, the instance will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="9e89b-123">Se essa função falhar, nenhuma etapa a ser preparada para o término do backup na instância será executada e nenhuma alteração no estado da instância ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="9e89b-123">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9e89b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e89b-124">Remarks</span></span>

<span data-ttu-id="9e89b-125">O backup é geralmente disparado por um evento fora do mecanismo de processo e usando essa API, o aplicativo ESENT em si fará outras chamadas para que as APIs de backup de streaming falhem.</span><span class="sxs-lookup"><span data-stu-id="9e89b-125">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="9e89b-126">A maioria das APIs de backup de streaming começará a falhar com JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="9e89b-126">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="9e89b-127">Assim, qualquer progresso de backup de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9e89b-127">As such, any streaming backup progress (like [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="9e89b-128">Operações de backup que fazem parte do encerramento de backup (como [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ainda serão permitidas.</span><span class="sxs-lookup"><span data-stu-id="9e89b-128">Backup operations which are part of the backup termination (such as [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9e89b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e89b-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e89b-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9e89b-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9e89b-131">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9e89b-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e89b-132"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9e89b-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9e89b-133">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9e89b-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e89b-134"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9e89b-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9e89b-135">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9e89b-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e89b-136"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="9e89b-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9e89b-137">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9e89b-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e89b-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9e89b-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9e89b-139">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9e89b-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9e89b-140">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9e89b-140">See Also</span></span>

[<span data-ttu-id="9e89b-141">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="9e89b-141">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="9e89b-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9e89b-142">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9e89b-143">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="9e89b-143">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="9e89b-144">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="9e89b-144">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="9e89b-145">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9e89b-145">JetStopService</span></span>](./jetstopservice-function.md)
