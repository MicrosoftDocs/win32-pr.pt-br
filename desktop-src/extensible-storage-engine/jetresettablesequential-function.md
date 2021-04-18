---
description: 'Saiba mais sobre: função JetResetTableSequential'
title: Função JetResetTableSequential
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86de80ac935af81fd2b4e8fdfef8b20dbb8d27d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786136"
---
# <a name="jetresettablesequential-function"></a><span data-ttu-id="a10a8-103">Função JetResetTableSequential</span><span class="sxs-lookup"><span data-stu-id="a10a8-103">JetResetTableSequential Function</span></span>


<span data-ttu-id="a10a8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a10a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresettablesequential-function"></a><span data-ttu-id="a10a8-105">Função JetResetTableSequential</span><span class="sxs-lookup"><span data-stu-id="a10a8-105">JetResetTableSequential Function</span></span>

<span data-ttu-id="a10a8-106">A função **JetResetTableSequential** notifica o mecanismo de banco de dados de que o aplicativo não está mais verificando todo o índice atual que contém um determinado cursor.</span><span class="sxs-lookup"><span data-stu-id="a10a8-106">The **JetResetTableSequential** function notifies the database engine that the application is no longer scanning the entire current index containing a given cursor.</span></span> <span data-ttu-id="a10a8-107">Essa chamada reverte uma notificação enviada pelo [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="a10a8-107">This call reverses a notification sent by [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

<span data-ttu-id="a10a8-108">**Windows XP:** o **JetResetTableSequential** é introduzido no Windows XP.   </span><span class="sxs-lookup"><span data-stu-id="a10a8-108">**Windows XP:**   **JetResetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a10a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a10a8-109">Parameters</span></span>

<span data-ttu-id="a10a8-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a10a8-110">*sesid*</span></span>

<span data-ttu-id="a10a8-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a10a8-111">The session to use for this call.</span></span>

<span data-ttu-id="a10a8-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a10a8-112">*tableid*</span></span>

<span data-ttu-id="a10a8-113">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="a10a8-113">The cursor to use for this call.</span></span>

<span data-ttu-id="a10a8-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a10a8-114">*grbit*</span></span>

<span data-ttu-id="a10a8-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a10a8-115">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="a10a8-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a10a8-116">Return Value</span></span>

<span data-ttu-id="a10a8-117">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a10a8-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a10a8-118">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a10a8-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a10a8-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a10a8-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="a10a8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a10a8-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a10a8-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a10a8-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a10a8-122">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a10a8-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a10a8-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a10a8-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a10a8-124">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a10a8-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a10a8-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a10a8-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a10a8-126">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="a10a8-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a10a8-127">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a10a8-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a10a8-128">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a10a8-128">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a10a8-129">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="a10a8-129">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a10a8-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a10a8-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a10a8-131">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="a10a8-131">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a10a8-132">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a10a8-132">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a10a8-133">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="a10a8-133">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a10a8-134">Em caso de sucesso, o índice atual do cursor não é mais otimizado para uma verificação sequencial de todo o índice.</span><span class="sxs-lookup"><span data-stu-id="a10a8-134">On success, the current index of the cursor is no longer optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="a10a8-135">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a10a8-135">No change to the database state will occur.</span></span>

<span data-ttu-id="a10a8-136">Em caso de falha, nenhuma alteração na configuração do cursor ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a10a8-136">On failure, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="a10a8-137">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a10a8-137">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a10a8-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="a10a8-138">Remarks</span></span>

<span data-ttu-id="a10a8-139">É seguro fazer essa chamada em relação a um cursor que não tenha sido configurado anteriormente por uma chamada para [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="a10a8-139">It is safe to make this call against a cursor that has not been previously configured by a call to [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="a10a8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a10a8-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a10a8-141"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a10a8-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a10a8-142">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a10a8-142">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a10a8-143"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a10a8-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a10a8-144">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a10a8-144">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a10a8-145"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a10a8-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a10a8-146">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a10a8-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a10a8-147"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="a10a8-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a10a8-148">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a10a8-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a10a8-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a10a8-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a10a8-150">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a10a8-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a10a8-151">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a10a8-151">See Also</span></span>

[<span data-ttu-id="a10a8-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a10a8-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a10a8-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a10a8-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a10a8-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a10a8-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a10a8-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a10a8-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a10a8-156">JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="a10a8-156">JetSetTableSequential</span></span>](./jetsettablesequential-function.md)  
[<span data-ttu-id="a10a8-157">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a10a8-157">JetStopService</span></span>](./jetstopservice-function.md)
