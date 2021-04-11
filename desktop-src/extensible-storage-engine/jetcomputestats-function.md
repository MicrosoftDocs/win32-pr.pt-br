---
description: 'Saiba mais sobre: função JetComputeStats'
title: Função JetComputeStats
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172078"
---
# <a name="jetcomputestats-function"></a><span data-ttu-id="5d41d-103">Função JetComputeStats</span><span class="sxs-lookup"><span data-stu-id="5d41d-103">JetComputeStats Function</span></span>


<span data-ttu-id="5d41d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5d41d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcomputestats-function"></a><span data-ttu-id="5d41d-105">Função JetComputeStats</span><span class="sxs-lookup"><span data-stu-id="5d41d-105">JetComputeStats Function</span></span>

<span data-ttu-id="5d41d-106">A função **JetComputeStats** percorre cada índice de uma tabela para calcular exatamente o número de entradas em um índice e o número de chaves distintas em um índice.</span><span class="sxs-lookup"><span data-stu-id="5d41d-106">The **JetComputeStats** function walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="5d41d-107">Essas informações, junto com o número de páginas de banco de dados alocadas para um índice e a hora atual da computação, são armazenadas em metadados de índice no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5d41d-107">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="5d41d-108">Esses dados podem ser recuperados posteriormente com operações de informações.</span><span class="sxs-lookup"><span data-stu-id="5d41d-108">This data can be subsequently retrieved with information operations.</span></span>

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="5d41d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d41d-109">Parameters</span></span>

<span data-ttu-id="5d41d-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5d41d-110">*sesid*</span></span>

<span data-ttu-id="5d41d-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="5d41d-111">The session to use for this call.</span></span>

<span data-ttu-id="5d41d-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5d41d-112">*tableid*</span></span>

<span data-ttu-id="5d41d-113">O cursor que será usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="5d41d-113">The cursor that will be used for this call.</span></span> <span data-ttu-id="5d41d-114">Descreve a tabela na qual as estatísticas são computadas.</span><span class="sxs-lookup"><span data-stu-id="5d41d-114">Describes the table to compute statistics on.</span></span>

### <a name="return-value"></a><span data-ttu-id="5d41d-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5d41d-115">Return Value</span></span>

<span data-ttu-id="5d41d-116">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d41d-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5d41d-117">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5d41d-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d41d-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5d41d-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="5d41d-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d41d-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d41d-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5d41d-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5d41d-121">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5d41d-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d41d-122">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5d41d-122">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5d41d-123">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5d41d-123">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d41d-124">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5d41d-124">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5d41d-125">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="5d41d-125">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5d41d-126">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5d41d-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d41d-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5d41d-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5d41d-128">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="5d41d-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d41d-129">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5d41d-129">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d41d-130">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="5d41d-130">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d41d-131">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="5d41d-131">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="5d41d-132">Erro ao exigir que esta operação reverta todas as alterações, mas a reversão da transação falhou.</span><span class="sxs-lookup"><span data-stu-id="5d41d-132">An error occurred requiring this operation to rollback all changes, but the transaction rollback itself failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d41d-133">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5d41d-133">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5d41d-134">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="5d41d-134">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5d41d-135">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="5d41d-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d41d-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5d41d-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d41d-137">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="5d41d-137">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d41d-138">Em caso de êxito, as estatísticas atualizadas são armazenadas nos catálogos de banco de dados para a tabela descrita com o cursor fornecido.</span><span class="sxs-lookup"><span data-stu-id="5d41d-138">On success, up-to-date statistics are stored in the database catalogs for the table described with the given cursor.</span></span>

<span data-ttu-id="5d41d-139">Em caso de falha, nenhuma atualização de nenhum tipo é feita no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5d41d-139">On failure, no updates of any kind are made to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5d41d-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d41d-140">Remarks</span></span>

<span data-ttu-id="5d41d-141">Essa operação pode ser consumindo recursos, pois cada índice em uma tabela deve ser percorrido em sua totalidade.</span><span class="sxs-lookup"><span data-stu-id="5d41d-141">This operation can be resource consuming since each index in a table must be walked in its entirety.</span></span> <span data-ttu-id="5d41d-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) pode ser usado para obter uma estimativa aproximada do número de entradas em um índice, mas não pode, por si só, estimar o número de valores distintos em um índice.</span><span class="sxs-lookup"><span data-stu-id="5d41d-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) can be used to get a rough estimate of the number of entries in an index, but it cannot by itself estimate the number of distinct values in an index.</span></span>

<span data-ttu-id="5d41d-143">Os dados computados por essa operação começam a ficar desatualizados e a tabela é atualizada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="5d41d-143">The data computed by this operation begins to become out of date and the table is subsequently updated.</span></span>

<span data-ttu-id="5d41d-144">As atualizações no banco de dados feita pelo **JetComputeStats** são feitas de maneira lenta.</span><span class="sxs-lookup"><span data-stu-id="5d41d-144">Updates to the database made by **JetComputeStats** are made in a lazy fashion.</span></span> <span data-ttu-id="5d41d-145">Isso significa que nenhuma liberação de log será acompanhada por essa operação e uma falha do sistema subsequente para um retorno de JET_errSuccess pelo **JetComputeStats** ainda poderá fazer com que essas atualizações sejam perdidas.</span><span class="sxs-lookup"><span data-stu-id="5d41d-145">This means that no log flush will be accompanied by this operation and a system crash subsequent to a return of JET_errSuccess by **JetComputeStats** can still cause these updates to be lost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5d41d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d41d-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d41d-147"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5d41d-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5d41d-148">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5d41d-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d41d-149"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5d41d-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5d41d-150">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5d41d-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d41d-151"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5d41d-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5d41d-152">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5d41d-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d41d-153"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="5d41d-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5d41d-154">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5d41d-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d41d-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5d41d-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5d41d-156">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5d41d-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5d41d-157">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5d41d-157">See Also</span></span>

[<span data-ttu-id="5d41d-158">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5d41d-158">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5d41d-159">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5d41d-159">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5d41d-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5d41d-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5d41d-161">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="5d41d-161">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="5d41d-162">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="5d41d-162">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="5d41d-163">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="5d41d-163">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="5d41d-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5d41d-164">JetStopService</span></span>](./jetstopservice-function.md)
