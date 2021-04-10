---
description: 'Saiba mais sobre: função JetResetSessionContext'
title: Função JetResetSessionContext
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ee02050a9583aa67f50fbe53d710c352c196048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169782"
---
# <a name="jetresetsessioncontext-function"></a><span data-ttu-id="3459c-103">Função JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="3459c-103">JetResetSessionContext Function</span></span>


<span data-ttu-id="3459c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3459c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresetsessioncontext-function"></a><span data-ttu-id="3459c-105">Função JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="3459c-105">JetResetSessionContext Function</span></span>

<span data-ttu-id="3459c-106">A função **JetResetSessionContext** desassocia uma sessão do thread atual.</span><span class="sxs-lookup"><span data-stu-id="3459c-106">The **JetResetSessionContext** function disassociates a session from the current thread.</span></span>

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="3459c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3459c-107">Parameters</span></span>

<span data-ttu-id="3459c-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3459c-108">*sesid*</span></span>

<span data-ttu-id="3459c-109">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3459c-109">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="3459c-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3459c-110">Return Value</span></span>

<span data-ttu-id="3459c-111">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="3459c-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3459c-112">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3459c-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3459c-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3459c-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="3459c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3459c-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3459c-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3459c-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3459c-116">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3459c-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3459c-117">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3459c-117">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3459c-118">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="3459c-118">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3459c-119">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3459c-119">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3459c-120">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3459c-120">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3459c-121">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="3459c-121">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3459c-122">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3459c-122">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3459c-123">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="3459c-123">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3459c-124">JET_errSessionContextNotSetByThisThread</span><span class="sxs-lookup"><span data-stu-id="3459c-124">JET_errSessionContextNotSetByThisThread</span></span></p></td>
<td><p><span data-ttu-id="3459c-125">Não foi possível desassociar a sessão do thread atual porque ela está associada a um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="3459c-125">The session could not be disassociated from the current thread because it is associated with a different thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3459c-126">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3459c-126">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3459c-127">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="3459c-127">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3459c-128">Em caso de sucesso, a sessão será desassociada do thread atual.</span><span class="sxs-lookup"><span data-stu-id="3459c-128">On success, the session will be disassociated from the current thread.</span></span> <span data-ttu-id="3459c-129">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="3459c-129">No change to the database state will occur.</span></span>

<span data-ttu-id="3459c-130">Se houver falha, o estado da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="3459c-130">On failure, the session state will remain unchanged.</span></span> <span data-ttu-id="3459c-131">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="3459c-131">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3459c-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="3459c-132">Remarks</span></span>

<span data-ttu-id="3459c-133">**JetResetSessionContext** deve ser chamado no mesmo thread que chamou [JetSetSessionContext](./jetsetsessioncontext-function.md) para uma determinada sessão.</span><span class="sxs-lookup"><span data-stu-id="3459c-133">**JetResetSessionContext** must be called on the same thread that called [JetSetSessionContext](./jetsetsessioncontext-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3459c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3459c-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3459c-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3459c-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3459c-136">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3459c-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3459c-137"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3459c-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3459c-138">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3459c-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3459c-139"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3459c-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3459c-140">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3459c-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3459c-141"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3459c-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3459c-142">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3459c-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3459c-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3459c-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3459c-144">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3459c-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3459c-145">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3459c-145">See Also</span></span>

[<span data-ttu-id="3459c-146">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="3459c-146">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="3459c-147">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3459c-147">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3459c-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3459c-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3459c-149">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="3459c-149">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)
