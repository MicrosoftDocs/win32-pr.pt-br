---
description: 'Saiba mais sobre: função JetIndexRecordCount'
title: Função JetIndexRecordCount
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501293"
---
# <a name="jetindexrecordcount-function"></a><span data-ttu-id="8b279-103">Função JetIndexRecordCount</span><span class="sxs-lookup"><span data-stu-id="8b279-103">JetIndexRecordCount Function</span></span>


<span data-ttu-id="8b279-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8b279-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetindexrecordcount-function"></a><span data-ttu-id="8b279-105">Função JetIndexRecordCount</span><span class="sxs-lookup"><span data-stu-id="8b279-105">JetIndexRecordCount Function</span></span>

<span data-ttu-id="8b279-106">A função **JetIndexRecordCount** conta o número de entradas no índice atual a partir da posição atual para frente.</span><span class="sxs-lookup"><span data-stu-id="8b279-106">The **JetIndexRecordCount** function counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="8b279-107">A posição atual é incluída na contagem.</span><span class="sxs-lookup"><span data-stu-id="8b279-107">The current position is included in the count.</span></span> <span data-ttu-id="8b279-108">A contagem pode ser maior que o número total de registros na tabela se o índice atual estiver sobre uma coluna de valores múltiplos e as instâncias da coluna tiverem vários valores.</span><span class="sxs-lookup"><span data-stu-id="8b279-108">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="8b279-109">Se a tabela estiver vazia, 0 será retornado para a contagem.</span><span class="sxs-lookup"><span data-stu-id="8b279-109">If the table is empty, then 0 will be returned for the count.</span></span>

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a><span data-ttu-id="8b279-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b279-110">Parameters</span></span>

<span data-ttu-id="8b279-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8b279-111">*sesid*</span></span>

<span data-ttu-id="8b279-112">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="8b279-112">The session to use for this call.</span></span>

<span data-ttu-id="8b279-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8b279-113">*tableid*</span></span>

<span data-ttu-id="8b279-114">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="8b279-114">The cursor to use for this call.</span></span>

<span data-ttu-id="8b279-115">*pcrec*</span><span class="sxs-lookup"><span data-stu-id="8b279-115">*pcrec*</span></span>

<span data-ttu-id="8b279-116">O ponteiro para um valor longo não atribuído para receber a contagem.</span><span class="sxs-lookup"><span data-stu-id="8b279-116">The pointer to an unsigned long value to receive the count.</span></span>

<span data-ttu-id="8b279-117">*crecMax*</span><span class="sxs-lookup"><span data-stu-id="8b279-117">*crecMax*</span></span>

<span data-ttu-id="8b279-118">O número máximo de registros a serem contados.</span><span class="sxs-lookup"><span data-stu-id="8b279-118">The maximum number of records to count.</span></span> <span data-ttu-id="8b279-119">Um valor de *crecMax* de 0 indica que a contagem é ilimitada.</span><span class="sxs-lookup"><span data-stu-id="8b279-119">A *crecMax* value of 0 indicates that the count is unlimited.</span></span>

### <a name="return-value"></a><span data-ttu-id="8b279-120">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8b279-120">Return Value</span></span>

<span data-ttu-id="8b279-121">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b279-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8b279-122">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8b279-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b279-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8b279-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="8b279-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b279-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b279-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8b279-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8b279-126">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8b279-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b279-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8b279-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8b279-128">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8b279-128">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b279-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8b279-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8b279-130">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="8b279-130">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8b279-131"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8b279-131"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b279-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="8b279-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="8b279-133">O cursor não está em um registro no momento e a tabela não está vazia.</span><span class="sxs-lookup"><span data-stu-id="8b279-133">The cursor is not currently on a record and the table is not empty.</span></span></p>
<p><span data-ttu-id="8b279-134"><strong>Windows XP, Windows Server 2003, windows 2000 Server e windows 2000 Professional:</strong>  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, <strong>JetIndexRecordCount</strong> retornará erroneamente JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="8b279-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:</strong>  If the cursor is positioned on an empty index or index range then <strong>JetIndexRecordCount</strong> erroneously returns JET_errNoCurrentRecord.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b279-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8b279-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8b279-136">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="8b279-136">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b279-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8b279-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8b279-138">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="8b279-138">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b279-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8b279-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8b279-140">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8b279-140">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="8b279-141"><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8b279-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b279-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8b279-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8b279-143">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="8b279-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8b279-144">Se essa função for bem sucedido, o número exato de entradas de índice, incluindo a posição atual e até *crecMax* (se não for 0), será retornado no longo não atribuído, apontado por *pcrec*.</span><span class="sxs-lookup"><span data-stu-id="8b279-144">If this function succeeds, the exact number of index entries including the current position and up to *crecMax* (if it is not 0), is returned in the unsigned long pointed to by *pcrec*.</span></span>

<span data-ttu-id="8b279-145">Se essa função falhar, nenhuma alteração será feita na memória alocada em *precpos*.</span><span class="sxs-lookup"><span data-stu-id="8b279-145">If this function fails, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8b279-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b279-146">Remarks</span></span>

<span data-ttu-id="8b279-147">Se a tabela não estiver vazia, o cursor deverá ser posicionado no registro do qual começar a contagem.</span><span class="sxs-lookup"><span data-stu-id="8b279-147">If the table is not empty, then the cursor should be positioned onto the record from which to begin the count.</span></span> <span data-ttu-id="8b279-148">A contagem incluirá esse registro e a contagem será encaminhada até o limite determinado em *crecMax*.</span><span class="sxs-lookup"><span data-stu-id="8b279-148">The count will include this record, and count forward up to the given limit in *crecMax*.</span></span> <span data-ttu-id="8b279-149">Se *crecMax* for 0, a operação continuará contando até o final do índice.</span><span class="sxs-lookup"><span data-stu-id="8b279-149">If *crecMax* is 0 then the operation will continue counting until the end of the index.</span></span>

<span data-ttu-id="8b279-150">Os intervalos de índice podem ser usados para construir limitações de fim de índice artificial para a contagem.</span><span class="sxs-lookup"><span data-stu-id="8b279-150">Index ranges can be used to construct artificial end-of-index limitations for the count.</span></span> <span data-ttu-id="8b279-151">Dessa forma, os subintervalos de um índice podem ser contados exatamente.</span><span class="sxs-lookup"><span data-stu-id="8b279-151">In this way, subranges of an index can be counted exactly.</span></span> <span data-ttu-id="8b279-152">O cursor deve ser posicionado na primeira linha do intervalo.</span><span class="sxs-lookup"><span data-stu-id="8b279-152">The cursor should be positioned to the first row in the range.</span></span> <span data-ttu-id="8b279-153">O final da chave do intervalo deve ser feito e, em seguida, [JetSetIndexRange](./jetsetindexrange-function.md) deve ser usado para definir o intervalo superior, inclusivamente ou exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="8b279-153">The end of the range key should be made and then [JetSetIndexRange](./jetsetindexrange-function.md) should be used to set the upper range, either inclusively or exclusively.</span></span> <span data-ttu-id="8b279-154">Por fim, **JetIndexRecordCount** deve ser chamado para contar exatamente o intervalo.</span><span class="sxs-lookup"><span data-stu-id="8b279-154">Lastly, **JetIndexRecordCount** should be called to exactly count the range.</span></span>

<span data-ttu-id="8b279-155">**JetIndexRecordCount** obedece à semântica de transação e retorna uma contagem que é precisa para essa sessão em particular em seu estado transacional atual.</span><span class="sxs-lookup"><span data-stu-id="8b279-155">**JetIndexRecordCount** obeys transaction semantics and returns a count that is accurate for this particular session in its current transactional state.</span></span>

<span data-ttu-id="8b279-156">O **JetIndexRecordCount** acessa páginas de folha de índice para contar com exatidão as entradas.</span><span class="sxs-lookup"><span data-stu-id="8b279-156">**JetIndexRecordCount** accesses index leaf pages in order to exactly count entries.</span></span> <span data-ttu-id="8b279-157">Consequentemente, ele pode executar uma grande quantidade de e/s e pode ser lento.</span><span class="sxs-lookup"><span data-stu-id="8b279-157">Consequently, it can perform a great deal of I/O and can be slow.</span></span> <span data-ttu-id="8b279-158">A limitação *crecMax* deve ser usada para evitar carga excessiva.</span><span class="sxs-lookup"><span data-stu-id="8b279-158">The *crecMax* limitation should be used to prevent excessive load.</span></span> <span data-ttu-id="8b279-159">Se um intervalo for grande, talvez seja possível contar o intervalo de maneira aproximada usando [JetGetRecordPosition](./jetgetrecordposition-function.md).</span><span class="sxs-lookup"><span data-stu-id="8b279-159">If a range is large, then it might be possible to count the range in an approximated fashion using [JetGetRecordPosition](./jetgetrecordposition-function.md).</span></span>

<span data-ttu-id="8b279-160">**Windows XP, Windows Server 2003, windows 2000 Server e windows 2000 Professional:**  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, **JetIndexRecordCount** retornará erroneamente JET_errNoCurrentRecord em vez de retornar uma contagem de registros zero.</span><span class="sxs-lookup"><span data-stu-id="8b279-160">**Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:**  If the cursor is positioned on an empty index or index range then **JetIndexRecordCount** erroneously returns JET_errNoCurrentRecord rather than returning a record count of zero.</span></span> <span data-ttu-id="8b279-161">O aplicativo deve verificar se o índice ou intervalo de índice está vazio nesse caso.</span><span class="sxs-lookup"><span data-stu-id="8b279-161">The application should check to see if the index or index range is empty in this case.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8b279-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b279-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b279-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8b279-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8b279-164">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8b279-164">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b279-165"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="8b279-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8b279-166">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8b279-166">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b279-167"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="8b279-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8b279-168">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8b279-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b279-169"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="8b279-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8b279-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8b279-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b279-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8b279-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8b279-172">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8b279-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8b279-173">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8b279-173">See Also</span></span>

[<span data-ttu-id="8b279-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8b279-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8b279-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8b279-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8b279-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8b279-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8b279-177">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="8b279-177">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="8b279-178">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="8b279-178">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="8b279-179">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8b279-179">JetStopService</span></span>](./jetstopservice-function.md)
