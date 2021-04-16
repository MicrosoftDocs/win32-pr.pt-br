---
description: 'Saiba mais sobre: função JetRegisterCallback'
title: Função JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772606"
---
# <a name="jetregistercallback-function"></a><span data-ttu-id="795d2-103">Função JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="795d2-103">JetRegisterCallback Function</span></span>


<span data-ttu-id="795d2-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="795d2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetregistercallback-function"></a><span data-ttu-id="795d2-105">Função JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="795d2-105">JetRegisterCallback Function</span></span>

<span data-ttu-id="795d2-106">A função **JetRegisterCallback** permite que o aplicativo configure o mecanismo de banco de dados para emitir notificações para o aplicativo para eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="795d2-106">The **JetRegisterCallback** function allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="795d2-107">Essas notificações são associadas a uma tabela específica e permanecem em vigor somente até que a instância que contém a tabela seja desligada usando [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="795d2-107">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="795d2-108">**Windows XP: o JetRegisterCallback** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="795d2-108">**Windows XP:  JetRegisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="795d2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="795d2-109">Parameters</span></span>

<span data-ttu-id="795d2-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="795d2-110">*sesid*</span></span>

<span data-ttu-id="795d2-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="795d2-111">The session to use for this call.</span></span>

<span data-ttu-id="795d2-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="795d2-112">*tableid*</span></span>

<span data-ttu-id="795d2-113">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="795d2-113">The cursor to use for this call.</span></span>

<span data-ttu-id="795d2-114">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="795d2-114">*cbtyp*</span></span>

<span data-ttu-id="795d2-115">Uma máscara de bits composta pelos motivos de retorno de chamada para os quais o aplicativo deseja receber notificações.</span><span class="sxs-lookup"><span data-stu-id="795d2-115">A bit mask composed of the callback reasons for which the application wishes to receive notifications.</span></span>

<span data-ttu-id="795d2-116">Para criar essa máscara de bits, basta ou juntos motivos de retorno de chamada válidos da enumeração [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="795d2-116">To create this bit mask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="795d2-117">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="795d2-117">*pCallback*</span></span>

<span data-ttu-id="795d2-118">O ponteiro de função para a função de retorno de chamada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="795d2-118">The function pointer to the callback function for the application.</span></span>

<span data-ttu-id="795d2-119">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="795d2-119">*pvContext*</span></span>

<span data-ttu-id="795d2-120">Especifica um ponteiro de contexto que será dado à função de retorno de chamada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="795d2-120">Specifies a context pointer that will be given to the callback function for the application.</span></span>

<span data-ttu-id="795d2-121">*phCallbackId*</span><span class="sxs-lookup"><span data-stu-id="795d2-121">*phCallbackId*</span></span>

<span data-ttu-id="795d2-122">Retorna um identificador que posteriormente pode ser usado para cancelar o registro da função de retorno de chamada fornecida usando [JetUnregisterCallback](./jetunregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="795d2-122">Returns a handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback](./jetunregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="795d2-123">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="795d2-123">Return Value</span></span>

<span data-ttu-id="795d2-124">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="795d2-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="795d2-125">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="795d2-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="795d2-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="795d2-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="795d2-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="795d2-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="795d2-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="795d2-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="795d2-129">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="795d2-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="795d2-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="795d2-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="795d2-131">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="795d2-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="795d2-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="795d2-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="795d2-133">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="795d2-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="795d2-134">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="795d2-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="795d2-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="795d2-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="795d2-136">Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="795d2-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="795d2-137">Esse erro será retornado por <strong>JetRegisterCallback</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="795d2-137">This error will be returned by <strong>JetRegisterCallback</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="795d2-138"><em>cbtyp</em> é zero,</span><span class="sxs-lookup"><span data-stu-id="795d2-138"><em>cbtyp</em> is zero,</span></span></p></li>
<li><p><span data-ttu-id="795d2-139"><em>pCallback</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="795d2-139"><em>pCallback</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="795d2-140"><em>phCallbackId</em> é nulo.</span><span class="sxs-lookup"><span data-stu-id="795d2-140"><em>phCallbackId</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="795d2-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="795d2-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="795d2-142">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="795d2-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="795d2-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="795d2-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="795d2-144">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="795d2-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="795d2-145">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="795d2-145">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="795d2-146">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="795d2-146">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="795d2-147">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="795d2-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="795d2-148">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="795d2-148">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="795d2-149">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="795d2-149">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="795d2-150">Em caso de sucesso, o retorno de chamada especificado será registrado para os motivos de retorno de chamada fornecidos com a tabela associada ao cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="795d2-150">On success, the specified callback will be registered for the given callback reasons with the table associated with the given cursor.</span></span> <span data-ttu-id="795d2-151">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="795d2-151">No change to the database state will occur.</span></span>

<span data-ttu-id="795d2-152">Em caso de falha, o retorno de chamada não será registrado.</span><span class="sxs-lookup"><span data-stu-id="795d2-152">On failure, the callback will not be registered.</span></span> <span data-ttu-id="795d2-153">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="795d2-153">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="795d2-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="795d2-154">Remarks</span></span>

<span data-ttu-id="795d2-155">Esse método fornece um meio para que o aplicativo associe retornos de chamada voláteis a uma tabela em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="795d2-155">This method provides a means for the application to associate volatile callbacks with a table in a database.</span></span> <span data-ttu-id="795d2-156">Se o aplicativo quiser associar retornos de chamada persistentes a uma tabela no banco de dados, ele deverá passar o retorno de chamada para [JET_TABLECREATE](./jet-tablecreate-structure.md) usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="795d2-156">If the application wishes to associate persisted callbacks with a table in the database then it should pass the callback to [JET_TABLECREATE](./jet-tablecreate-structure.md) using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="795d2-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="795d2-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="795d2-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="795d2-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="795d2-159">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="795d2-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="795d2-160"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="795d2-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="795d2-161">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="795d2-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="795d2-162"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="795d2-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="795d2-163">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="795d2-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="795d2-164"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="795d2-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="795d2-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="795d2-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="795d2-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="795d2-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="795d2-167">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="795d2-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="795d2-168">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="795d2-168">See Also</span></span>

[<span data-ttu-id="795d2-169">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="795d2-169">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="795d2-170">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="795d2-170">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="795d2-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="795d2-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="795d2-172">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="795d2-172">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="795d2-173">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="795d2-173">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="795d2-174">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="795d2-174">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="795d2-175">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="795d2-175">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="795d2-176">JetTerm</span><span class="sxs-lookup"><span data-stu-id="795d2-176">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="795d2-177">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="795d2-177">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)
