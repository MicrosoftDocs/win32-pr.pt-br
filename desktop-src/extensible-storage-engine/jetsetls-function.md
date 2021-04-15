---
description: 'Saiba mais sobre: função JetSetLS'
title: Função JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501490"
---
# <a name="jetsetls-function"></a><span data-ttu-id="2ae72-103">Função JetSetLS</span><span class="sxs-lookup"><span data-stu-id="2ae72-103">JetSetLS Function</span></span>


<span data-ttu-id="2ae72-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2ae72-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetls-function"></a><span data-ttu-id="2ae72-105">Função JetSetLS</span><span class="sxs-lookup"><span data-stu-id="2ae72-105">JetSetLS Function</span></span>

<span data-ttu-id="2ae72-106">A função **JetSetLS** permite que o aplicativo associe um identificador de contexto conhecido como armazenamento local com um cursor ou a tabela associada a esse cursor.</span><span class="sxs-lookup"><span data-stu-id="2ae72-106">The **JetSetLS** function enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="2ae72-107">Esse identificador de contexto pode ser usado pelo aplicativo para armazenar dados auxiliares associados a um cursor ou tabela.</span><span class="sxs-lookup"><span data-stu-id="2ae72-107">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="2ae72-108">O aplicativo é notificado posteriormente usando um retorno de chamada de tempo de execução quando o identificador de contexto deve ser liberado.</span><span class="sxs-lookup"><span data-stu-id="2ae72-108">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="2ae72-109">Isso torna possível associar o estado alocado dinamicamente a um cursor ou tabela.</span><span class="sxs-lookup"><span data-stu-id="2ae72-109">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="2ae72-110">**Windows XP:** o **JetSetLS** é introduzido no Windows XP.  </span><span class="sxs-lookup"><span data-stu-id="2ae72-110">**Windows XP:**  **JetSetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2ae72-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ae72-111">Parameters</span></span>

<span data-ttu-id="2ae72-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2ae72-112">*sesid*</span></span>

<span data-ttu-id="2ae72-113">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="2ae72-113">The session to use for this call.</span></span>

<span data-ttu-id="2ae72-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2ae72-114">*tableid*</span></span>

<span data-ttu-id="2ae72-115">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="2ae72-115">The cursor to use for this call.</span></span>

<span data-ttu-id="2ae72-116">*ls*</span><span class="sxs-lookup"><span data-stu-id="2ae72-116">*ls*</span></span>

<span data-ttu-id="2ae72-117">O identificador de contexto a ser associado ao cursor ou à tabela.</span><span class="sxs-lookup"><span data-stu-id="2ae72-117">The context handle to be associated with the cursor or table.</span></span>

<span data-ttu-id="2ae72-118">Quando JET_bitLSReset for especificado, o valor real desse parâmetro será ignorado e JET_LSNil será usado.</span><span class="sxs-lookup"><span data-stu-id="2ae72-118">When JET_bitLSReset is specified then the actual value of this parameter is ignored and JET_LSNil is used.</span></span>

<span data-ttu-id="2ae72-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2ae72-119">*grbit*</span></span>

<span data-ttu-id="2ae72-120">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ae72-120">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ae72-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2ae72-121">Value</span></span></p></th>
<th><p><span data-ttu-id="2ae72-122">Significado</span><span class="sxs-lookup"><span data-stu-id="2ae72-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="2ae72-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="2ae72-124">Essa opção indica que o identificador de contexto deve ser associado ao cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="2ae72-124">This option indicates that the context handle should be associated with the given cursor.</span></span></p>
<p><span data-ttu-id="2ae72-125">Se nem JET_bitLSCursor nem JET_bitLSTable forem especificadas, JET_bitLSCursor será presumido.</span><span class="sxs-lookup"><span data-stu-id="2ae72-125">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="2ae72-126">É ilegal usar essa opção com JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="2ae72-126">It is illegal to use this option with JET_bitLSTable.</span></span> <span data-ttu-id="2ae72-127">A operação falhará com JET_errInvalidgrbit se for tentada.</span><span class="sxs-lookup"><span data-stu-id="2ae72-127">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ae72-128">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="2ae72-128">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="2ae72-129">Essa opção indica que o identificador de contexto especificado deve ser ignorado e que o identificador de contexto para o objeto escolhido deve ser redefinido para JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="2ae72-129">This option indicates that the specified context handle should be ignored and that the context handle for the chosen object should be reset to JET_LSNil.</span></span></p>
<p><span data-ttu-id="2ae72-130">É importante observar que essa ação não resultará em um retorno de chamada para limpar o valor anterior do identificador de contexto para o objeto escolhido.</span><span class="sxs-lookup"><span data-stu-id="2ae72-130">It is important to note that this action will not result in a callback to cleanup the previous value of the context handle for the chosen object.</span></span> <span data-ttu-id="2ae72-131">A limpeza adequada do identificador de contexto anterior pode ser obtida usando <a href="gg269234(v=exchg.10).md">JetGetLS</a> com JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="2ae72-131">Proper cleanup of the previous context handle can be achieved using <a href="gg269234(v=exchg.10).md">JetGetLS</a> with JET_bitLSReset.</span></span> <span data-ttu-id="2ae72-132">Consulte <a href="gg269234(v=exchg.10).md">JetGetLS</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2ae72-132">See <a href="gg269234(v=exchg.10).md">JetGetLS</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-133">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="2ae72-133">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="2ae72-134">Essa opção indica que o identificador de contexto deve ser associado à tabela associada ao cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="2ae72-134">This option indicates that the context handle should be associated with the table associated with the given cursor.</span></span></p>
<p><span data-ttu-id="2ae72-135">É ilegal usar essa opção com JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="2ae72-135">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="2ae72-136">A operação falhará com JET_errInvalidgrbit se for tentada.</span><span class="sxs-lookup"><span data-stu-id="2ae72-136">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2ae72-137">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2ae72-137">Return Value</span></span>

<span data-ttu-id="2ae72-138">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ae72-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2ae72-139">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2ae72-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ae72-140">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2ae72-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="2ae72-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ae72-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2ae72-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2ae72-143">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="2ae72-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ae72-144">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2ae72-144">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2ae72-145">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2ae72-145">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="2ae72-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="2ae72-147">Uma das opções solicitadas era inválida, foi usada incorretamente ou não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="2ae72-147">One of the options requested was invalid, used incorrectly, or not implemented.</span></span> <span data-ttu-id="2ae72-148">Isso pode ocorrer para <strong>JetSetLS</strong> quando JET_bitLSCursor e JET_bitLSTable são especificados.</span><span class="sxs-lookup"><span data-stu-id="2ae72-148">This can happen for <strong>JetSetLS</strong> when JET_bitLSCursor and JET_bitLSTable are both specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ae72-149">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2ae72-149">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2ae72-150">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="2ae72-150">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="2ae72-151">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="2ae72-151">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-152">JET_errLSAlreadySet</span><span class="sxs-lookup"><span data-stu-id="2ae72-152">JET_errLSAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="2ae72-153">O identificador de contexto fornecido não pôde ser associado ao objeto solicitado porque ele já tinha um identificador de contexto associado a ele.</span><span class="sxs-lookup"><span data-stu-id="2ae72-153">The given context handle could not be associated with the requested object because it already had a context handle associated with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ae72-154">JET_errLSCallbackNotSpecified</span><span class="sxs-lookup"><span data-stu-id="2ae72-154">JET_errLSCallbackNotSpecified</span></span></p></td>
<td><p><span data-ttu-id="2ae72-155">O identificador de contexto fornecido não pôde ser associado ao objeto solicitado porque o retorno de chamada de tempo de execução não foi configurado para a instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="2ae72-155">The given context handle could not be associated with the requested object because the runtime callback has not been configured for the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2ae72-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2ae72-157">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="2ae72-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ae72-158">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2ae72-158">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2ae72-159">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="2ae72-159">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2ae72-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2ae72-161">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="2ae72-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ae72-162">Em caso de sucesso, o identificador de contexto fornecido foi associado com êxito ao objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="2ae72-162">On success, the given context handle was successfully associated with the requested object.</span></span> <span data-ttu-id="2ae72-163">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="2ae72-163">No change to the database state will occur.</span></span>

<span data-ttu-id="2ae72-164">Em caso de falha, nenhuma alteração no estado do objeto solicitado ocorreu.</span><span class="sxs-lookup"><span data-stu-id="2ae72-164">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="2ae72-165">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="2ae72-165">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2ae72-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ae72-166">Remarks</span></span>

<span data-ttu-id="2ae72-167">O armazenamento local para um cursor ou uma tabela deve ser exibido como um cache volátil.</span><span class="sxs-lookup"><span data-stu-id="2ae72-167">The Local Storage for a cursor or table should be viewed as a volatile cache.</span></span> <span data-ttu-id="2ae72-168">O aplicativo deve primeiro tentar recuperar o identificador de contexto usando [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="2ae72-168">The application should first try to retrieve the context handle using [JetGetLS](./jetgetls-function.md).</span></span> <span data-ttu-id="2ae72-169">Se o valor não for definido (ou seja, JET_LSNil), o aplicativo deverá criar um novo contexto e carregá-lo no cache usando **JetSetLS**.</span><span class="sxs-lookup"><span data-stu-id="2ae72-169">If the value is not set (that is it is JET_LSNil) then the application should create a new context and load it into the cache using **JetSetLS**.</span></span> <span data-ttu-id="2ae72-170">O aplicativo pode limpar o cache usando uma chamada para [JetGetLS](./jetgetls-function.md) com JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="2ae72-170">The application can purge the cache using a call to [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="2ae72-171">Se o mecanismo de banco de dados limpar o cache, um retorno de chamada de tempo de execução será gerado para dar ao aplicativo a oportunidade de limpar esse contexto.</span><span class="sxs-lookup"><span data-stu-id="2ae72-171">If the database engine purges the cache then a runtime callback will be generated to give the application a chance to cleanup that context.</span></span> <span data-ttu-id="2ae72-172">O tipo de retorno de chamada será JET_cbtypFreeCursorLS para um identificador de contexto associado a um cursor e JET_cbtypFreeTableLS para um identificador de contexto associado a uma tabela.</span><span class="sxs-lookup"><span data-stu-id="2ae72-172">The callback type will be JET_cbtypFreeCursorLS for a context handle associated with a cursor and JET_cbtypFreeTableLS for a context handle associated with a table.</span></span> <span data-ttu-id="2ae72-173">Em ambos os casos, o identificador de contexto será passado como pvArg1.</span><span class="sxs-lookup"><span data-stu-id="2ae72-173">In either case, the context handle will be passed as pvArg1.</span></span> <span data-ttu-id="2ae72-174">Consulte [JET_CALLBACK](./jet-callback-callback-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2ae72-174">See [JET_CALLBACK](./jet-callback-callback-function.md) for more information.</span></span>

<span data-ttu-id="2ae72-175">O retorno de chamada de tempo de execução deve ser configurado corretamente para a instância associada à sessão especificada antes que o armazenamento local possa ser usado.</span><span class="sxs-lookup"><span data-stu-id="2ae72-175">The runtime callback must be properly configured for the instance associated with the given session before Local Storage can be used.</span></span> <span data-ttu-id="2ae72-176">Esse retorno de chamada pode ser definido usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramRuntimeCallback](./callback-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2ae72-176">This callback can be set using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramRuntimeCallback](./callback-parameters.md).</span></span> <span data-ttu-id="2ae72-177">Consulte [JetSetSystemParameter](./jetsetsystemparameter-function.md) e [JET_paramRuntimeCallback](./callback-parameters.md) em parâmetros do sistema para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2ae72-177">See [JetSetSystemParameter](./jetsetsystemparameter-function.md) and [JET_paramRuntimeCallback](./callback-parameters.md) in System Parameters for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2ae72-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae72-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-179"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2ae72-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2ae72-180">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ae72-180">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ae72-181"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="2ae72-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2ae72-182">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2ae72-182">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-183"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="2ae72-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2ae72-184">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2ae72-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ae72-185"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="2ae72-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2ae72-186">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2ae72-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ae72-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2ae72-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2ae72-188">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2ae72-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2ae72-189">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2ae72-189">See Also</span></span>

[<span data-ttu-id="2ae72-190">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="2ae72-190">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="2ae72-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2ae72-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2ae72-192">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2ae72-192">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2ae72-193">JET_LS</span><span class="sxs-lookup"><span data-stu-id="2ae72-193">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="2ae72-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2ae72-194">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2ae72-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2ae72-195">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2ae72-196">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="2ae72-196">JetGetLS</span></span>](./jetgetls-function.md)  
[<span data-ttu-id="2ae72-197">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="2ae72-197">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="2ae72-198">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="2ae72-198">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
