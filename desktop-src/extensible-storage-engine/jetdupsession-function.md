---
description: 'Saiba mais sobre: função JetDupSession'
title: Função JetDupSession
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829606"
---
# <a name="jetdupsession-function"></a><span data-ttu-id="ec20a-103">Função JetDupSession</span><span class="sxs-lookup"><span data-stu-id="ec20a-103">JetDupSession Function</span></span>


<span data-ttu-id="ec20a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ec20a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupsession-function"></a><span data-ttu-id="ec20a-105">Função JetDupSession</span><span class="sxs-lookup"><span data-stu-id="ec20a-105">JetDupSession Function</span></span>

<span data-ttu-id="ec20a-106">A função **JetDupSession** inicia uma sessão e inicializa e retorna um identificador de sessão do ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="ec20a-106">The **JetDupSession** function starts a session, and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="ec20a-107">As sessões controlam todo o acesso ao banco de dados e são usadas para controlar o escopo das transações.</span><span class="sxs-lookup"><span data-stu-id="ec20a-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="ec20a-108">A sessão pode ser usada para iniciar, confirmar ou anular transações.</span><span class="sxs-lookup"><span data-stu-id="ec20a-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="ec20a-109">A sessão também é usada para anexar, criar ou abrir um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ec20a-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="ec20a-110">A sessão é usada como contexto para todas as operações DDL e DML.</span><span class="sxs-lookup"><span data-stu-id="ec20a-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="ec20a-111">Para aumentar a simultaneidade e o acesso paralelo ao banco de dados, várias sessões podem ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="ec20a-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

<span data-ttu-id="ec20a-112">**Observação** Essa API funcionará de todas as maneiras como um [JetBeginSession](./jetbeginsession-function.md) chamado na instância da sessão passada.</span><span class="sxs-lookup"><span data-stu-id="ec20a-112">**Note** This API will act in all ways as a [JetBeginSession](./jetbeginsession-function.md) called on the instance of the session passed in.</span></span> <span data-ttu-id="ec20a-113">Essa função não é recomendada, [JetBeginSession](./jetbeginsession-function.md) é preferencial.</span><span class="sxs-lookup"><span data-stu-id="ec20a-113">This function is not recommended, [JetBeginSession](./jetbeginsession-function.md) is preferred.</span></span>

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a><span data-ttu-id="ec20a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec20a-114">Parameters</span></span>

<span data-ttu-id="ec20a-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ec20a-115">*sesid*</span></span>

<span data-ttu-id="ec20a-116">A sessão a ser usada como a origem para duplicar ou iniciar a sessão.</span><span class="sxs-lookup"><span data-stu-id="ec20a-116">The session to use as the source for duplicating or beginning the session.</span></span>

<span data-ttu-id="ec20a-117">*psesid*</span><span class="sxs-lookup"><span data-stu-id="ec20a-117">*psesid*</span></span>

<span data-ttu-id="ec20a-118">Um ponteiro para a variável que o identificador de sessão Inicializa no retorno bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ec20a-118">A pointer to the variable that the session handle initializes on successful return.</span></span>

### <a name="return-value"></a><span data-ttu-id="ec20a-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ec20a-119">Return Value</span></span>

<span data-ttu-id="ec20a-120">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec20a-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ec20a-121">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ec20a-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec20a-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ec20a-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="ec20a-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec20a-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ec20a-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ec20a-125">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ec20a-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec20a-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ec20a-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ec20a-127">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ec20a-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ec20a-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ec20a-129">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="ec20a-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="ec20a-130">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="ec20a-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec20a-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ec20a-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ec20a-132">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ec20a-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ec20a-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ec20a-134">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="ec20a-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec20a-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="ec20a-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="ec20a-136">A operação falhou porque não foi possível alocar memória.</span><span class="sxs-lookup"><span data-stu-id="ec20a-136">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-137">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="ec20a-137">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="ec20a-138">O número de sessões que o mecanismo permitirá que o cliente inicie é limitado.</span><span class="sxs-lookup"><span data-stu-id="ec20a-138">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="ec20a-139">Esse valor pode ser alterado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com a constante <em>JET_paramMaxSessions</em> .</span><span class="sxs-lookup"><span data-stu-id="ec20a-139">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the <em>JET_paramMaxSessions</em> constant.</span></span> <span data-ttu-id="ec20a-140">O número padrão de sessões é 16.</span><span class="sxs-lookup"><span data-stu-id="ec20a-140">The default number of sessions is 16.</span></span> <span data-ttu-id="ec20a-141">Consulte <a href="gg294139(v=exchg.10).md">parâmetros do sistema</a> para obter detalhes sobre <em>JET_paramMaxSessions</em>.</span><span class="sxs-lookup"><span data-stu-id="ec20a-141">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about <em>JET_paramMaxSessions</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec20a-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ec20a-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ec20a-143">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="ec20a-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ec20a-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ec20a-145">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="ec20a-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec20a-146">Em caso de sucesso, o identificador de sessão é inicializado e pode ser usado para operações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ec20a-146">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="ec20a-147">Em caso de falha, não há sessões disponíveis ou não foi possível inicializar uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="ec20a-147">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ec20a-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec20a-148">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-149"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ec20a-149"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec20a-150">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ec20a-150">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec20a-151"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ec20a-151"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec20a-152">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ec20a-152">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-153"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ec20a-153"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec20a-154">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ec20a-154">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec20a-155"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="ec20a-155"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ec20a-156">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ec20a-156">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec20a-157"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ec20a-157"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ec20a-158">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ec20a-158">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ec20a-159">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ec20a-159">See Also</span></span>

[<span data-ttu-id="ec20a-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ec20a-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ec20a-161">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="ec20a-161">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="ec20a-162">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="ec20a-162">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="ec20a-163">JetStopService</span><span class="sxs-lookup"><span data-stu-id="ec20a-163">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="ec20a-164">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="ec20a-164">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
