---
description: 'Saiba mais sobre: função JetSetSessionContext'
title: Função JetSetSessionContext
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815593"
---
# <a name="jetsetsessioncontext-function"></a><span data-ttu-id="0c580-103">Função JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="0c580-103">JetSetSessionContext Function</span></span>


<span data-ttu-id="0c580-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0c580-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsessioncontext-function"></a><span data-ttu-id="0c580-105">Função JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="0c580-105">JetSetSessionContext Function</span></span>

<span data-ttu-id="0c580-106">A função **JetSetSessionContext** associa uma sessão ao thread atual usando o identificador de contexto fornecido.</span><span class="sxs-lookup"><span data-stu-id="0c580-106">The **JetSetSessionContext** function associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="0c580-107">Essa associação substitui o requisito de mecanismo padrão que uma transação para uma determinada sessão deve ocorrer inteiramente no mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="0c580-107">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span>

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a><span data-ttu-id="0c580-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c580-108">Parameters</span></span>

<span data-ttu-id="0c580-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0c580-109">*sesid*</span></span>

<span data-ttu-id="0c580-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="0c580-110">The session to use for this call.</span></span>

<span data-ttu-id="0c580-111">*ulContext*</span><span class="sxs-lookup"><span data-stu-id="0c580-111">*ulContext*</span></span>

<span data-ttu-id="0c580-112">Um identificador exclusivo ao qual esta sessão será associada.</span><span class="sxs-lookup"><span data-stu-id="0c580-112">A unique identifier to which this session will be associated.</span></span>

### <a name="return-value"></a><span data-ttu-id="0c580-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0c580-113">Return Value</span></span>

<span data-ttu-id="0c580-114">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c580-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0c580-115">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0c580-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c580-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0c580-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="0c580-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c580-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c580-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0c580-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0c580-119">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="0c580-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c580-120">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="0c580-120">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="0c580-121">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="0c580-121">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c580-122">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="0c580-122">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="0c580-123">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="0c580-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="0c580-124"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c580-124"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c580-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0c580-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0c580-126">Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="0c580-126">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="0c580-127">Esse erro será retornado por <strong>JetSetSessionContext</strong> sob as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="0c580-127">This error will be returned by <strong>JetSetSessionContext</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="0c580-128"><em>ulContext</em> é nulo</span><span class="sxs-lookup"><span data-stu-id="0c580-128"><em>ulContext</em> is NULL</span></span></p></li>
<li><p><span data-ttu-id="0c580-129"><em>ulContext</em> é-1</span><span class="sxs-lookup"><span data-stu-id="0c580-129"><em>ulContext</em> is -1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c580-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="0c580-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="0c580-131">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="0c580-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c580-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="0c580-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="0c580-133">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="0c580-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c580-134">JET_errSessionContextAlreadySet</span><span class="sxs-lookup"><span data-stu-id="0c580-134">JET_errSessionContextAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="0c580-135">Não foi possível associar a sessão ao thread atual porque ela já foi associada a um thread.</span><span class="sxs-lookup"><span data-stu-id="0c580-135">The session could not be associated with the current thread because it has already been associated with a thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c580-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="0c580-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="0c580-137">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="0c580-137">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0c580-138">Se essa função for realizada com sucesso, a sessão será associada ao thread atual.</span><span class="sxs-lookup"><span data-stu-id="0c580-138">If this function succeeds, the session will be associated with the current thread.</span></span> <span data-ttu-id="0c580-139">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="0c580-139">No change to the database state will occur.</span></span>

<span data-ttu-id="0c580-140">Se essa função falhar, o estado da sessão permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="0c580-140">If this function fails, the session state will remain unchanged.</span></span> <span data-ttu-id="0c580-141">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="0c580-141">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0c580-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c580-142">Remarks</span></span>

<span data-ttu-id="0c580-143">Geralmente, uma sessão é associada a um thread específico durante uma transação.</span><span class="sxs-lookup"><span data-stu-id="0c580-143">A session is usually bound to a specific thread for the duration of a transaction.</span></span> <span data-ttu-id="0c580-144">Esse comportamento foi projetado para ajudar os aplicativos a detectar e impedir o compartilhamento de uma única sessão informada de forma conceitual entre vários threads.</span><span class="sxs-lookup"><span data-stu-id="0c580-144">This behavior is designed to help applications detect and prevent the conceptually ill-advised sharing of a single session amongst multiple threads.</span></span> <span data-ttu-id="0c580-145">Às vezes, essa verificação simples não funciona com a arquitetura do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c580-145">Sometimes, this simple check does not work with the application's architecture.</span></span> <span data-ttu-id="0c580-146">Por exemplo, se o aplicativo estiver hospedando objetos do lado do servidor usando um pool de threads e as transações abrangerem várias chamadas de servidor para um determinado objeto, essa proteção poderá fazer com que algumas dessas chamadas falhem com JET_errSessionSharingViolation embora o padrão de uso esteja correto.</span><span class="sxs-lookup"><span data-stu-id="0c580-146">For example, if the application is hosting server-side objects using a thread pool and transactions span multiple server calls to a given object then this protection may cause some of those calls to fail with JET_errSessionSharingViolation even though the usage pattern is correct.</span></span> <span data-ttu-id="0c580-147">Essa situação é comum para servidores de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="0c580-147">This situation is common for COM object servers.</span></span>

<span data-ttu-id="0c580-148">**JetSetSessionContext** e [JetResetSessionContext](./jetresetsessioncontext-function.md) resolvem esse problema tornando a verificação de compartilhamento de sessão um pouco mais flexível.</span><span class="sxs-lookup"><span data-stu-id="0c580-148">**JetSetSessionContext** and [JetResetSessionContext](./jetresetsessioncontext-function.md) solve this problem by making this session sharing check a little more flexible.</span></span> <span data-ttu-id="0c580-149">Quando o aplicativo começa a fazer uma série de chamadas de API do ESE usando uma sessão específica, ele primeiro define o contexto da sessão para um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="0c580-149">When the application starts to make a series of ESE API calls using a particular session, it first sets the session context to a given value.</span></span> <span data-ttu-id="0c580-150">Essa ação associa a sessão ao thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="0c580-150">This action associates the session to the calling thread.</span></span> <span data-ttu-id="0c580-151">No exemplo fornecido, esse contexto pode ser o endereço do objeto que contém o identificador de sessão do JET.</span><span class="sxs-lookup"><span data-stu-id="0c580-151">In the given example, this context could be the address of the object that contains the JET session handle.</span></span> <span data-ttu-id="0c580-152">Depois que as chamadas à API do ESE tiverem sido feitas, o aplicativo redefinirá o contexto da sessão.</span><span class="sxs-lookup"><span data-stu-id="0c580-152">Once the ESE API calls have been made, the application resets the session context.</span></span> <span data-ttu-id="0c580-153">Essa ação desassocia a sessão do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="0c580-153">This action disassociates the session from the calling thread.</span></span> <span data-ttu-id="0c580-154">O objeto e sua sessão podem ser usados por outro thread, mesmo que a sessão tenha uma transação ativa.</span><span class="sxs-lookup"><span data-stu-id="0c580-154">The object and its session can then be used by another thread even if the session has an active transaction.</span></span>

<span data-ttu-id="0c580-155">É importante observar que **JetSetSessionContext** deve ser chamado antes da abertura de uma transação nessa sessão, ou a associação não funcionará.</span><span class="sxs-lookup"><span data-stu-id="0c580-155">It is important to note that **JetSetSessionContext** must be called prior to opening a transaction on that session or the association will not work.</span></span>

<span data-ttu-id="0c580-156">**JetSetSessionContext** é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0c580-156">**JetSetSessionContext** is thread safe.</span></span> <span data-ttu-id="0c580-157">Vários threads podem tentar definir um contexto de thread na mesma sessão ao mesmo tempo e apenas um ganhará.</span><span class="sxs-lookup"><span data-stu-id="0c580-157">Multiple threads can try to set a thread context on the same session at the same time and only one will win.</span></span> <span data-ttu-id="0c580-158">Esse fato pode ser usado pelo aplicativo como um meio de alocar uma sessão de um pool sem armazenar o estado externo sobre sua alocação.</span><span class="sxs-lookup"><span data-stu-id="0c580-158">This fact can be used by the application as a means to allocate a session from a pool without storing external state about its allocation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0c580-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c580-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c580-160"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0c580-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0c580-161">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0c580-161">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c580-162"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="0c580-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0c580-163">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0c580-163">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c580-164"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="0c580-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0c580-165">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0c580-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c580-166"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="0c580-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0c580-167">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0c580-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c580-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0c580-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0c580-169">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0c580-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0c580-170">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0c580-170">See Also</span></span>

[<span data-ttu-id="0c580-171">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="0c580-171">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="0c580-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0c580-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0c580-173">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="0c580-173">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="0c580-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0c580-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0c580-175">JetStopService</span><span class="sxs-lookup"><span data-stu-id="0c580-175">JetStopService</span></span>](./jetstopservice-function.md)
