---
description: 'Saiba mais sobre: função JetGetRecordPosition'
title: Função JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011116"
---
# <a name="jetgetrecordposition-function"></a><span data-ttu-id="e66df-103">Função JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="e66df-103">JetGetRecordPosition Function</span></span>


<span data-ttu-id="e66df-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e66df-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordposition-function"></a><span data-ttu-id="e66df-105">Função JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="e66df-105">JetGetRecordPosition Function</span></span>

<span data-ttu-id="e66df-106">A função **JetGetRecordPosition** retorna a posição fracionária do registro atual no índice atual na forma de uma estrutura de [JET_RECPOS](./jet-recpos-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e66df-106">The **JetGetRecordPosition** function returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-structure.md) structure.</span></span> <span data-ttu-id="e66df-107">Essa estrutura descreve as posições fracionárias em termos de um número aproximado de entradas de índice antes do registro atual e um número total aproximado de entradas no índice.</span><span class="sxs-lookup"><span data-stu-id="e66df-107">This structure describes fractional positions in terms of an approximate number of index entries before the current record and an approximate total number of entries in the index.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a><span data-ttu-id="e66df-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e66df-108">Parameters</span></span>

<span data-ttu-id="e66df-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e66df-109">*sesid*</span></span>

<span data-ttu-id="e66df-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="e66df-110">The session to use for this call.</span></span>

<span data-ttu-id="e66df-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e66df-111">*tableid*</span></span>

<span data-ttu-id="e66df-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="e66df-112">The cursor to use for this call.</span></span>

<span data-ttu-id="e66df-113">*precpos*</span><span class="sxs-lookup"><span data-stu-id="e66df-113">*precpos*</span></span>

<span data-ttu-id="e66df-114">A descrição da fração a ser usada para obter a posição do registro atual no índice atual.</span><span class="sxs-lookup"><span data-stu-id="e66df-114">The description of the fraction to use in getting the position of the current record in the current index.</span></span>

<span data-ttu-id="e66df-115">*cbRecpos*</span><span class="sxs-lookup"><span data-stu-id="e66df-115">*cbRecpos*</span></span>

<span data-ttu-id="e66df-116">O tamanho da memória alocada em *precpos*.</span><span class="sxs-lookup"><span data-stu-id="e66df-116">The size of memory allocated at *precpos*.</span></span>

### <a name="return-value"></a><span data-ttu-id="e66df-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e66df-117">Return Value</span></span>

<span data-ttu-id="e66df-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e66df-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e66df-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e66df-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e66df-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e66df-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="e66df-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e66df-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e66df-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e66df-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e66df-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e66df-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e66df-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e66df-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e66df-125">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="e66df-125">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e66df-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e66df-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e66df-127">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e66df-127">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e66df-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e66df-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e66df-129">Esta operação não pode ser concluída porque a instância, associada à sessão, encontrou um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="e66df-129">This operation cannot complete because the instance, associated with the session, encountered a fatal error.</span></span> <span data-ttu-id="e66df-130">É necessário que o acesso a todos os dados seja revogado a fim de proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="e66df-130">It is required that access to all data be revoked in order to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e66df-131"><strong>Windows 2000:</strong>  Esse erro não será retornado pelo sistema operacional Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e66df-131"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e66df-132">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e66df-132">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e66df-133">O tamanho da memória alocada em <em>precpos</em> não é um tamanho suficiente.</span><span class="sxs-lookup"><span data-stu-id="e66df-133">The size of the allocated memory at <em>precpos</em> is not a sufficient size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e66df-134">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="e66df-134">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="e66df-135">O cursor não está em um registro no momento e não pode retornar uma posição.</span><span class="sxs-lookup"><span data-stu-id="e66df-135">The cursor is not currently on a record and cannot return a position.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e66df-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e66df-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e66df-137">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="e66df-137">It is not possible to complete the operation because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e66df-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e66df-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e66df-139">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e66df-139">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e66df-140"><strong>Windows 2000:</strong>  Esse erro não será retornado pelo sistema operacional Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e66df-140"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e66df-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e66df-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e66df-142">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="e66df-142">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e66df-143">Em caso de sucesso, o número aproximado de entradas de índice que antecedem o registro atual no índice são retornados em precpos- \> centriesLT.</span><span class="sxs-lookup"><span data-stu-id="e66df-143">On success, the approximate number of index entries preceding the current record in the index are returned in precpos-\>centriesLT.</span></span> <span data-ttu-id="e66df-144">1 é retornado em precpos- \> centriesInRange.</span><span class="sxs-lookup"><span data-stu-id="e66df-144">1 is returned in precpos-\>centriesInRange.</span></span> <span data-ttu-id="e66df-145">O número aproximado de entradas no índice é retornado em precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="e66df-145">The approximate number of entries in the index is returned in precpos-\>centriesTotal.</span></span>

<span data-ttu-id="e66df-146">Em caso de falha, nenhuma alteração é feita na memória alocada em *precpos*.</span><span class="sxs-lookup"><span data-stu-id="e66df-146">On failure, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e66df-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="e66df-147">Remarks</span></span>

<span data-ttu-id="e66df-148">Essa operação retorna dados variados quando as atualizações ocorrem continuamente na tabela.</span><span class="sxs-lookup"><span data-stu-id="e66df-148">This operation returns varying data when updates occur continuously on the table.</span></span> <span data-ttu-id="e66df-149">As alterações nos valores nem sempre corresponderão às expectativas com base no conhecimento das atualizações, já que os valores são aproximações com base nas propriedades físicas do índice.</span><span class="sxs-lookup"><span data-stu-id="e66df-149">The changes in the values will not always match expectations based on knowledge of the updates, since the values are approximations based on physical properties of the index.</span></span> <span data-ttu-id="e66df-150">O isolamento transacional não se aplica a posições de **JetGetRecordPosition** , pois os valores dependem das propriedades físicas do índice que não são isoladas da transação.</span><span class="sxs-lookup"><span data-stu-id="e66df-150">Transactional isolation does not apply to positions from **JetGetRecordPosition** since the values depend on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="e66df-151">[JET_RECPOS](./jet-recpos-structure.md) não deve ser usado para descrever um registro em uma tabela ou para reposicionar um registro próximo a um registro existente.</span><span class="sxs-lookup"><span data-stu-id="e66df-151">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="e66df-152">Em vez disso, os indicadores para um registro existente devem ser recuperados e, em seguida, usados para reposicionar o mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="e66df-152">Instead, bookmarks for an existing record should be retrieved and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e66df-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e66df-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e66df-154"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e66df-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e66df-155">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e66df-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e66df-156"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="e66df-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e66df-157">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e66df-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e66df-158"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="e66df-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e66df-159">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e66df-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e66df-160"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="e66df-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e66df-161">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e66df-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e66df-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e66df-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e66df-163">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e66df-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e66df-164">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e66df-164">See Also</span></span>

[<span data-ttu-id="e66df-165">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e66df-165">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e66df-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e66df-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e66df-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e66df-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e66df-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e66df-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e66df-169">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="e66df-169">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="e66df-170">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="e66df-170">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="e66df-171">JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="e66df-171">JetGotoPosition</span></span>](./jetgotoposition-function.md)  
[<span data-ttu-id="e66df-172">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e66df-172">JetStopService</span></span>](./jetstopservice-function.md)
