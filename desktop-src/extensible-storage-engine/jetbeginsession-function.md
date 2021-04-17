---
description: 'Saiba mais sobre: função JetBeginSession'
title: Função JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785254"
---
# <a name="jetbeginsession-function"></a><span data-ttu-id="1fa58-103">Função JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="1fa58-103">JetBeginSession Function</span></span>


<span data-ttu-id="1fa58-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1fa58-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginsession-function"></a><span data-ttu-id="1fa58-105">Função JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="1fa58-105">JetBeginSession Function</span></span>

<span data-ttu-id="1fa58-106">A função **JetBeginSession** inicia uma sessão e inicializa e retorna um identificador de sessão do ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="1fa58-106">The **JetBeginSession** function starts a session and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="1fa58-107">As sessões controlam todo o acesso ao banco de dados e são usadas para controlar o escopo das transações.</span><span class="sxs-lookup"><span data-stu-id="1fa58-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="1fa58-108">A sessão pode ser usada para iniciar, confirmar ou anular transações.</span><span class="sxs-lookup"><span data-stu-id="1fa58-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="1fa58-109">A sessão também é usada para anexar, criar ou abrir um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1fa58-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="1fa58-110">A sessão é usada como contexto para todas as operações DDL e DML.</span><span class="sxs-lookup"><span data-stu-id="1fa58-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="1fa58-111">Para aumentar a simultaneidade e o acesso paralelo ao banco de dados, várias sessões podem ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="1fa58-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a><span data-ttu-id="1fa58-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fa58-112">Parameters</span></span>

<span data-ttu-id="1fa58-113">*cópia*</span><span class="sxs-lookup"><span data-stu-id="1fa58-113">*instance*</span></span>

<span data-ttu-id="1fa58-114">A instância do banco de dados a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="1fa58-114">The database instance to use for this call.</span></span>

<span data-ttu-id="1fa58-115">*psesid*</span><span class="sxs-lookup"><span data-stu-id="1fa58-115">*psesid*</span></span>

<span data-ttu-id="1fa58-116">Ponteiro para a variável que o identificador de sessão Inicializa no retorno bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1fa58-116">Pointer to the variable that the session handle initializes on successful return.</span></span>

<span data-ttu-id="1fa58-117">*szUserName*</span><span class="sxs-lookup"><span data-stu-id="1fa58-117">*szUserName*</span></span>

<span data-ttu-id="1fa58-118">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="1fa58-118">This parameter is reserved.</span></span>

<span data-ttu-id="1fa58-119">*szPassword*</span><span class="sxs-lookup"><span data-stu-id="1fa58-119">*szPassword*</span></span>

<span data-ttu-id="1fa58-120">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="1fa58-120">This parameter is reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="1fa58-121">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1fa58-121">Return Value</span></span>

<span data-ttu-id="1fa58-122">Essa função permite o retorno de qualquer [JET_ERR](./jet-err.md)s que são definidos nesta API.</span><span class="sxs-lookup"><span data-stu-id="1fa58-122">This function allows for the return of any [JET_ERR](./jet-err.md)s that are defined in this API.</span></span> <span data-ttu-id="1fa58-123">Para obter mais informações sobre erros do Jet, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1fa58-123">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fa58-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1fa58-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="1fa58-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fa58-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1fa58-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1fa58-127">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1fa58-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fa58-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1fa58-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1fa58-129">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="1fa58-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1fa58-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1fa58-131">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="1fa58-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1fa58-132">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="1fa58-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fa58-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1fa58-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1fa58-134">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1fa58-134">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1fa58-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1fa58-136">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="1fa58-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fa58-137">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1fa58-137">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="1fa58-138">A operação falhou porque não foi possível alocar memória.</span><span class="sxs-lookup"><span data-stu-id="1fa58-138">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-139">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="1fa58-139">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="1fa58-140">O número de sessões que o mecanismo permitirá que o cliente inicie é limitado.</span><span class="sxs-lookup"><span data-stu-id="1fa58-140">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="1fa58-141">Esse valor pode ser alterado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com a constante JET_paramMaxSessions.</span><span class="sxs-lookup"><span data-stu-id="1fa58-141">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the JET_paramMaxSessions constant.</span></span> <span data-ttu-id="1fa58-142">O número padrão de sessões é 16.</span><span class="sxs-lookup"><span data-stu-id="1fa58-142">The default number of sessions is 16.</span></span> <span data-ttu-id="1fa58-143">Consulte <a href="gg294139(v=exchg.10).md">parâmetros do sistema</a> para obter detalhes sobre JET_paramMaxSessions.</span><span class="sxs-lookup"><span data-stu-id="1fa58-143">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about JET_paramMaxSessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fa58-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1fa58-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1fa58-145">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="1fa58-145">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1fa58-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1fa58-147">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="1fa58-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1fa58-148">Em caso de sucesso, o identificador de sessão é inicializado e pode ser usado para operações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1fa58-148">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="1fa58-149">Em caso de falha, não há sessões disponíveis ou não foi possível inicializar uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="1fa58-149">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1fa58-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fa58-150">Remarks</span></span>

<span data-ttu-id="1fa58-151">É necessário usar atenção cuidadosa ao usar sessões em threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="1fa58-151">Careful attention must be used when using sessions across different threads.</span></span> <span data-ttu-id="1fa58-152">Uma sessão controla em qual thread ele foi usado durante [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md)ou [JetRollback](./jetrollback-function.md), e gerará um erro se usado em vários threads com uma transação aberta.</span><span class="sxs-lookup"><span data-stu-id="1fa58-152">A session tracks which thread it was used on during [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md), or [JetRollback](./jetrollback-function.md), and it will throw an error if used on multiple threads with an open transaction.</span></span> <span data-ttu-id="1fa58-153">O [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) pode alterar esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="1fa58-153">The [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) can change this behavior.</span></span> <span data-ttu-id="1fa58-154">Como a sessão ainda é um contexto serializado, e várias operações de banco de dados não podem ser executadas em uma única sessão simultaneamente, apenas em série.</span><span class="sxs-lookup"><span data-stu-id="1fa58-154">Since the session is still a serialized context, and multiple database operations cannot be performed on a single session concurrently, only serially.</span></span> <span data-ttu-id="1fa58-155">No entanto, você pode usar várias sessões para obter acesso simultâneo ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1fa58-155">However, you can use multiple sessions to achieve concurrent database access.</span></span> <span data-ttu-id="1fa58-156">As sessões podem ser usadas dentro de uma transação entre threads definindo e redefinindo os contextos de sessão.</span><span class="sxs-lookup"><span data-stu-id="1fa58-156">Sessions can be used inside a transaction across threads by setting and resetting the session contexts.</span></span>

<span data-ttu-id="1fa58-157">O identificador de sessão deve ser fechado com [JetEndSession](./jetendsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="1fa58-157">The session handle should be closed with [JetEndSession](./jetendsession-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="1fa58-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fa58-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-159"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1fa58-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1fa58-160">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1fa58-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fa58-161"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="1fa58-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1fa58-162">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1fa58-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-163"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="1fa58-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1fa58-164">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1fa58-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fa58-165"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="1fa58-165"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1fa58-166">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1fa58-166">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fa58-167"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1fa58-167"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1fa58-168">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1fa58-168">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fa58-169"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1fa58-169"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1fa58-170">Implementado como <strong>JetBeginSessionW</strong> (Unicode) e <strong>JetBeginSessionA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1fa58-170">Implemented as <strong>JetBeginSessionW</strong> (Unicode) and <strong>JetBeginSessionA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1fa58-171">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1fa58-171">See Also</span></span>

[<span data-ttu-id="1fa58-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1fa58-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1fa58-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1fa58-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="1fa58-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1fa58-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1fa58-175">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="1fa58-175">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="1fa58-176">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="1fa58-176">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="1fa58-177">JetDupSession</span><span class="sxs-lookup"><span data-stu-id="1fa58-177">JetDupSession</span></span>](./jetdupsession-function.md)  
[<span data-ttu-id="1fa58-178">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="1fa58-178">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="1fa58-179">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="1fa58-179">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="1fa58-180">JetRollback</span><span class="sxs-lookup"><span data-stu-id="1fa58-180">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="1fa58-181">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="1fa58-181">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="1fa58-182">JetStopService</span><span class="sxs-lookup"><span data-stu-id="1fa58-182">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="1fa58-183">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="1fa58-183">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
