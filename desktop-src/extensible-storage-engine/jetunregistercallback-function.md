---
description: 'Saiba mais sobre: função JetUnregisterCallback'
title: Função JetUnregisterCallback
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b342bab655e3cf1e3c1a5967410edb1c971af87b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370626"
---
# <a name="jetunregistercallback-function"></a><span data-ttu-id="a7fbd-103">Função JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="a7fbd-103">JetUnregisterCallback Function</span></span>


<span data-ttu-id="a7fbd-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a7fbd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetunregistercallback-function"></a><span data-ttu-id="a7fbd-105">Função JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="a7fbd-105">JetUnregisterCallback Function</span></span>

<span data-ttu-id="a7fbd-106">A função **JetUnregisterCallback** permite que o aplicativo configure o mecanismo de banco de dados para parar de emitir notificações para o aplicativo conforme solicitado anteriormente por meio de [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7fbd-106">The **JetUnregisterCallback** function enables the application to configure the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

<span data-ttu-id="a7fbd-107">**Windows XP:** o **JetUnregisterCallback** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="a7fbd-107">**Windows XP:**  **JetUnregisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="a7fbd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7fbd-108">Parameters</span></span>

<span data-ttu-id="a7fbd-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a7fbd-109">*sesid*</span></span>

<span data-ttu-id="a7fbd-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-110">The session to use for this call.</span></span>

<span data-ttu-id="a7fbd-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a7fbd-111">*tableid*</span></span>

<span data-ttu-id="a7fbd-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-112">The cursor to use for this call.</span></span>

<span data-ttu-id="a7fbd-113">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="a7fbd-113">*cbtyp*</span></span>

<span data-ttu-id="a7fbd-114">Um bitmask composto pelos motivos de retorno de chamada que o aplicativo não deseja mais receber notificações.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-114">A bitmask composed of the callback reasons that the application no longer wishes to receive notifications.</span></span>

<span data-ttu-id="a7fbd-115">Para criar essa bitmask, basta ou agrupar por motivos de retorno de chamada válidos da enumeração [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="a7fbd-115">To create this bitmask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="a7fbd-116">*hCallbackId*</span><span class="sxs-lookup"><span data-stu-id="a7fbd-116">*hCallbackId*</span></span>

<span data-ttu-id="a7fbd-117">O identificador do retorno de chamada registrado que foi retornado por [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="a7fbd-117">The handle of the registered callback that was returned by [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="a7fbd-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a7fbd-118">Return Value</span></span>

<span data-ttu-id="a7fbd-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a7fbd-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a7fbd-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7fbd-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a7fbd-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="a7fbd-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7fbd-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7fbd-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a7fbd-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a7fbd-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7fbd-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a7fbd-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a7fbd-126">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7fbd-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a7fbd-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a7fbd-128">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a7fbd-129"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-129"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7fbd-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a7fbd-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a7fbd-131">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7fbd-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a7fbd-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a7fbd-133">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7fbd-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a7fbd-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a7fbd-135">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-135">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a7fbd-136"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-136"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7fbd-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a7fbd-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a7fbd-138">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-138">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7fbd-139">Se essa função tiver sucesso, o retorno de chamada especificado terá seu registro cancelado para os motivos de retorno de chamada fornecidos com a tabela associada ao cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-139">If this function succeeds, the specified callback will be unregistered for the given callback reasons with the table that is associated with the given cursor.</span></span> <span data-ttu-id="a7fbd-140">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-140">No change to the database state will occur.</span></span>

<span data-ttu-id="a7fbd-141">Se essa função falhar, o retorno de chamada especificado não terá seu registro cancelado.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-141">If this function fails, the specified callback will not be unregistered.</span></span> <span data-ttu-id="a7fbd-142">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-142">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a7fbd-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7fbd-143">Remarks</span></span>

<span data-ttu-id="a7fbd-144">A bitmask fornecida deve corresponder exatamente ao bitmask especificado ao registrar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-144">The given bitmask should exactly match the bitmask that is specified when registering the callback.</span></span> <span data-ttu-id="a7fbd-145">No momento, o mecanismo de banco de dados não dá suporte à remoção de um subconjunto dessas notificações e não retorna um erro quando isso é tentado.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-145">The database engine does not currently support removing a subset of these notifications and it does not return an error when this is attempted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a7fbd-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7fbd-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7fbd-147"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a7fbd-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a7fbd-148">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-148">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7fbd-149"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a7fbd-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a7fbd-150">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-150">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7fbd-151"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a7fbd-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a7fbd-152">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7fbd-153"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="a7fbd-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a7fbd-154">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7fbd-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a7fbd-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a7fbd-156">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a7fbd-157">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a7fbd-157">See Also</span></span>

[<span data-ttu-id="a7fbd-158">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="a7fbd-158">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="a7fbd-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a7fbd-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a7fbd-160">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="a7fbd-160">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="a7fbd-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a7fbd-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a7fbd-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a7fbd-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a7fbd-163">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="a7fbd-163">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="a7fbd-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a7fbd-164">JetStopService</span></span>](./jetstopservice-function.md)
