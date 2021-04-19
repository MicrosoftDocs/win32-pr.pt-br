---
description: 'Saiba mais sobre: função JetGotoBookmark'
title: Função JetGotoBookmark
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814128"
---
# <a name="jetgotobookmark-function"></a><span data-ttu-id="24c39-103">Função JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="24c39-103">JetGotoBookmark Function</span></span>


<span data-ttu-id="24c39-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="24c39-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotobookmark-function"></a><span data-ttu-id="24c39-105">Função JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="24c39-105">JetGotoBookmark Function</span></span>

<span data-ttu-id="24c39-106">A função **JetGotoBookmark** posiciona um cursor para uma entrada de índice para o registro associado ao indicador especificado.</span><span class="sxs-lookup"><span data-stu-id="24c39-106">The **JetGotoBookmark** function positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="24c39-107">O indicador pode ser usado com qualquer índice definido em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="24c39-107">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="24c39-108">O indicador de um registro pode ser recuperado usando [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="24c39-108">The bookmark for a record can be retrieved using [JetGetBookmark](./jetgetbookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a><span data-ttu-id="24c39-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24c39-109">Parameters</span></span>

<span data-ttu-id="24c39-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="24c39-110">*sesid*</span></span>

<span data-ttu-id="24c39-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="24c39-111">The session to use for this call.</span></span>

<span data-ttu-id="24c39-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="24c39-112">*tableid*</span></span>

<span data-ttu-id="24c39-113">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="24c39-113">The cursor to use for this call.</span></span>

<span data-ttu-id="24c39-114">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="24c39-114">*pvBookmark*</span></span>

<span data-ttu-id="24c39-115">O buffer que contém o indicador a ser usado para posicionar o cursor.</span><span class="sxs-lookup"><span data-stu-id="24c39-115">The buffer that contains the bookmark to use to position the cursor.</span></span>

<span data-ttu-id="24c39-116">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="24c39-116">*cbBookmark*</span></span>

<span data-ttu-id="24c39-117">O tamanho do indicador no buffer.</span><span class="sxs-lookup"><span data-stu-id="24c39-117">The size of the bookmark in the buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="24c39-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="24c39-118">Return Value</span></span>

<span data-ttu-id="24c39-119">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="24c39-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="24c39-120">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="24c39-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24c39-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="24c39-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="24c39-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="24c39-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24c39-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="24c39-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="24c39-124">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="24c39-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c39-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="24c39-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="24c39-126">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="24c39-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c39-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="24c39-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="24c39-128">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="24c39-128">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="24c39-129"><strong>Windows XP:</strong>   Esse valor de retorno foi introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24c39-129"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c39-130">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="24c39-130">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="24c39-131">O indicador fornecido é inválido.</span><span class="sxs-lookup"><span data-stu-id="24c39-131">The bookmark that was provided is invalid.</span></span> <span data-ttu-id="24c39-132">Isso pode ter ocorrido porque o tamanho do indicador é zero ou o ponteiro do buffer do indicador é <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c39-132">This might have occurred because the size of the bookmark is zero or the bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c39-133">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="24c39-133">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="24c39-134">O cursor está em um índice secundário e nenhuma entrada de índice foi encontrada para o registro associado ao indicador.</span><span class="sxs-lookup"><span data-stu-id="24c39-134">The cursor is on a secondary index and no index entry could be found for the record that is associated with the bookmark.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c39-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="24c39-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="24c39-136">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="24c39-136">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c39-137">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="24c39-137">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="24c39-138">Não foi possível encontrar o registro associado ao indicador.</span><span class="sxs-lookup"><span data-stu-id="24c39-138">The record that is associated with the bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c39-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="24c39-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="24c39-140">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="24c39-140">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c39-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="24c39-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="24c39-142">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="24c39-142">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="24c39-143"><strong>Windows XP:</strong>   Esse valor de retorno foi introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24c39-143"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c39-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="24c39-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="24c39-145">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="24c39-145">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="24c39-146">Se essa função for bem sucedido, o cursor será posicionado em uma entrada de índice para o registro associado ao indicador especificado.</span><span class="sxs-lookup"><span data-stu-id="24c39-146">If this function succeeds, the cursor will be positioned at an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="24c39-147">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="24c39-147">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="24c39-148">Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="24c39-148">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="24c39-149">Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="24c39-149">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="24c39-150">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="24c39-150">No change to the database state will occur.</span></span>

<span data-ttu-id="24c39-151">Se essa função falhar, a posição do cursor permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="24c39-151">If this function fails, the position of the cursor will remain unchanged.</span></span> <span data-ttu-id="24c39-152">Se um registro tiver sido preparado para atualização, essa atualização será cancelada.</span><span class="sxs-lookup"><span data-stu-id="24c39-152">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="24c39-153">Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado.</span><span class="sxs-lookup"><span data-stu-id="24c39-153">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="24c39-154">Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída.</span><span class="sxs-lookup"><span data-stu-id="24c39-154">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="24c39-155">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="24c39-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="24c39-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="24c39-156">Remarks</span></span>

<span data-ttu-id="24c39-157">Há duas maneiras de usar um indicador para posicionar um cursor em um índice.</span><span class="sxs-lookup"><span data-stu-id="24c39-157">There are two ways to use a bookmark to position a cursor on an index.</span></span> <span data-ttu-id="24c39-158">A primeira é usar o indicador para posicioná-lo diretamente no registro.</span><span class="sxs-lookup"><span data-stu-id="24c39-158">The first is to use the bookmark to position on the record directly.</span></span> <span data-ttu-id="24c39-159">Isso ocorre quando o índice atual do cursor é o índice primário.</span><span class="sxs-lookup"><span data-stu-id="24c39-159">This occurs when the current index of the cursor is the primary index.</span></span> <span data-ttu-id="24c39-160">Essa técnica funciona porque um indicador de ESENT é o mesmo que a chave primária do registro associado.</span><span class="sxs-lookup"><span data-stu-id="24c39-160">This technique works because an ESENT bookmark is the same as the associated record's primary key.</span></span>

<span data-ttu-id="24c39-161">A segunda maneira de usar um indicador é posicioná-lo em uma entrada em um índice secundário que corresponda ao registro associado a esse indicador.</span><span class="sxs-lookup"><span data-stu-id="24c39-161">The second way to use a bookmark is to position it on an entry in a secondary index that corresponds to the record that is associated with that bookmark.</span></span> <span data-ttu-id="24c39-162">Durante esse processo, o mecanismo pesquisa o registro real usando o indicador no índice primário.</span><span class="sxs-lookup"><span data-stu-id="24c39-162">During this process, the engine looks up the actual record using the bookmark on the primary index.</span></span> <span data-ttu-id="24c39-163">Em seguida, ele usa os dados de registro e a definição de índice secundário para computar uma chave no índice secundário que aponta para o registro.</span><span class="sxs-lookup"><span data-stu-id="24c39-163">It then uses the record data and the secondary index definition to compute a key into the secondary index that points to the record.</span></span> <span data-ttu-id="24c39-164">Em seguida, ele posiciona o cursor na entrada de índice para essa chave.</span><span class="sxs-lookup"><span data-stu-id="24c39-164">It then positions the cursor on the index entry for that key.</span></span> <span data-ttu-id="24c39-165">Se o cursor estiver atualmente em um índice secundário em uma ou mais colunas de chave com valores múltiplos, o cursor será posicionado na entrada de índice correspondente ao primeiro valor múltiplo de cada uma dessas colunas de chave.</span><span class="sxs-lookup"><span data-stu-id="24c39-165">If the cursor is currently on a secondary index over one or more multi-valued key columns, the cursor will be positioned on the index entry corresponding to the first multi-value of each of those key columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="24c39-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24c39-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24c39-167"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="24c39-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="24c39-168">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="24c39-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c39-169"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="24c39-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="24c39-170">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="24c39-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c39-171"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="24c39-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="24c39-172">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="24c39-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24c39-173"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="24c39-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="24c39-174">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="24c39-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24c39-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="24c39-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="24c39-176">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="24c39-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="24c39-177">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="24c39-177">See Also</span></span>

[<span data-ttu-id="24c39-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="24c39-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="24c39-179">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="24c39-179">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="24c39-180">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="24c39-180">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="24c39-181">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="24c39-181">JetGetBookmark</span></span>](./jetgetbookmark-function.md)
