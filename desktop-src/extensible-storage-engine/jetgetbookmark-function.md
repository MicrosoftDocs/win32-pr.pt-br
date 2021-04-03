---
description: 'Saiba mais sobre: função JetGetBookmark'
title: Função JetGetBookmark
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091777"
---
# <a name="jetgetbookmark-function"></a><span data-ttu-id="3e561-103">Função JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="3e561-103">JetGetBookmark Function</span></span>


<span data-ttu-id="3e561-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3e561-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetbookmark-function"></a><span data-ttu-id="3e561-105">Função JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="3e561-105">JetGetBookmark Function</span></span>

<span data-ttu-id="3e561-106">A função **JetGetBookmark** recupera o indicador para o registro que está associado à entrada de índice na posição atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="3e561-106">The **JetGetBookmark** function retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="3e561-107">Esse indicador pode então ser usado para reposicionar esse cursor de volta para o mesmo registro usando [JetGoToBookmark](./jetgotobookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="3e561-107">This bookmark can then be used to reposition that cursor back to the same record using [JetGoToBookmark](./jetgotobookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="3e561-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e561-108">Parameters</span></span>

<span data-ttu-id="3e561-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3e561-109">*sesid*</span></span>

<span data-ttu-id="3e561-110">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3e561-110">The session to use for this call.</span></span>

<span data-ttu-id="3e561-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="3e561-111">*tableid*</span></span>

<span data-ttu-id="3e561-112">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="3e561-112">The cursor to use for this call.</span></span>

<span data-ttu-id="3e561-113">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="3e561-113">*pvBookmark*</span></span>

<span data-ttu-id="3e561-114">O buffer de saída que recebe o indicador.</span><span class="sxs-lookup"><span data-stu-id="3e561-114">The output buffer that receives the bookmark.</span></span>

<span data-ttu-id="3e561-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="3e561-115">*cbMax*</span></span>

<span data-ttu-id="3e561-116">O tamanho máximo, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="3e561-116">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="3e561-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="3e561-117">*pcbActual*</span></span>

<span data-ttu-id="3e561-118">O tamanho real, em bytes, do indicador.</span><span class="sxs-lookup"><span data-stu-id="3e561-118">The actual size, in bytes, of the bookmark.</span></span>

<span data-ttu-id="3e561-119">Se esse parâmetro for **nulo** , o tamanho real do indicador não será retornado.</span><span class="sxs-lookup"><span data-stu-id="3e561-119">If this parameter is **NULL** then the actual size of the bookmark will not be returned.</span></span>

<span data-ttu-id="3e561-120">Se o buffer de saída for muito pequeno, o tamanho real do indicador ainda será retornado.</span><span class="sxs-lookup"><span data-stu-id="3e561-120">If the output buffer is too small, the actual size of the bookmark will still be returned.</span></span> <span data-ttu-id="3e561-121">Isso significa que esse número será maior do que o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="3e561-121">That means that this number will be larger than the size of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="3e561-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3e561-122">Return Value</span></span>

<span data-ttu-id="3e561-123">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e561-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3e561-124">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3e561-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e561-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3e561-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="3e561-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e561-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e561-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3e561-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3e561-128">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3e561-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e561-129">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="3e561-129">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="3e561-130">A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber o indicador inteiro.</span><span class="sxs-lookup"><span data-stu-id="3e561-130">The operation completed successfully, but the output buffer was too small to receive the entire bookmark.</span></span> <span data-ttu-id="3e561-131">O buffer de saída foi preenchido com a maior parte do indicador que couber.</span><span class="sxs-lookup"><span data-stu-id="3e561-131">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="3e561-132">O tamanho real do indicador também foi retornado, se solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e561-132">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e561-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3e561-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3e561-134">A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="3e561-134">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e561-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3e561-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3e561-136">A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="3e561-136">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3e561-137"><strong>Windows XP:  </strong> Esses valores de retorno são apresentados no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e561-137"><strong>Windows XP:  </strong>This return values is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e561-138">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="3e561-138">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="3e561-139">O cursor não está posicionado em um registro.</span><span class="sxs-lookup"><span data-stu-id="3e561-139">The cursor is not positioned on a record.</span></span> <span data-ttu-id="3e561-140">Isso pode ocorrer por vários motivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="3e561-140">This can happen for many different reasons.</span></span> <span data-ttu-id="3e561-141">Por exemplo, isso ocorrerá se o cursor estiver posicionado após o último registro no índice atual.</span><span class="sxs-lookup"><span data-stu-id="3e561-141">For example, this will happen if the cursor is positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e561-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3e561-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3e561-143">A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="3e561-143">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e561-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3e561-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3e561-145">A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="3e561-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e561-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3e561-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3e561-147">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="3e561-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="3e561-148"><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e561-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e561-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3e561-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3e561-150">A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="3e561-150">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e561-151">Se essa função for realizada com sucesso, o indicador do registro associado à entrada de índice na posição atual de um cursor será retornado no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="3e561-151">If this function succeeds, the bookmark for the record that is associated with the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="3e561-152">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="3e561-152">No change to the database state will occur.</span></span>

<span data-ttu-id="3e561-153">Se essa função falhar, o estado do buffer de saída e o tamanho real do indicador serão indefinidos, a menos que JET_errBufferTooSmall seja retornado.</span><span class="sxs-lookup"><span data-stu-id="3e561-153">If this function fails, the state of the output buffer and the actual size of the bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="3e561-154">No caso em que JET_errBufferTooSmall for retornado, o buffer de saída conterá a maior parte do indicador que se ajustará no espaço fornecido e o tamanho real do indicador será preciso.</span><span class="sxs-lookup"><span data-stu-id="3e561-154">In the event that JET_errBufferTooSmall is returned, the output buffer will contain as much of the bookmark as will fit in the space provided and the actual size of the bookmark will be accurate.</span></span> <span data-ttu-id="3e561-155">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="3e561-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3e561-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e561-156">Remarks</span></span>

<span data-ttu-id="3e561-157">Os indicadores geralmente devem ser tratados como partes opacas de dados.</span><span class="sxs-lookup"><span data-stu-id="3e561-157">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="3e561-158">Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados.</span><span class="sxs-lookup"><span data-stu-id="3e561-158">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="3e561-159">No entanto, as seguintes condições são verdadeiras de todos os indicadores de ESENT:</span><span class="sxs-lookup"><span data-stu-id="3e561-159">However, the following conditions are true of all ESENT bookmarks:</span></span>

  - <span data-ttu-id="3e561-160">Um indicador identifica exclusivamente um registro em uma determinada tabela.</span><span class="sxs-lookup"><span data-stu-id="3e561-160">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="3e561-161">O indicador de um registro não será alterado durante o tempo de vida desse registro.</span><span class="sxs-lookup"><span data-stu-id="3e561-161">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="3e561-162">O indicador de um registro é o mesmo que a chave desse registro no índice primário na tabela que contém esse registro.</span><span class="sxs-lookup"><span data-stu-id="3e561-162">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="3e561-163">Se nenhum índice primário for definido nessa tabela, o mecanismo de banco de dados criará seu próprio indicador para o registro.</span><span class="sxs-lookup"><span data-stu-id="3e561-163">If no primary index is defined over that table the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="3e561-164">Os indicadores podem ser comparados entre si usando a função [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice primário na tabela dos registros de origem.</span><span class="sxs-lookup"><span data-stu-id="3e561-164">Bookmarks can be compared against each other using the [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) function to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="3e561-165">Se nenhum índice primário for definido nessa tabela, não será significativo usar a ordenação relativa de indicadores dessa tabela.</span><span class="sxs-lookup"><span data-stu-id="3e561-165">If no primary index is defined over that table, it is not meaningful to use the relative ordering of bookmarks from that table.</span></span>

  - <span data-ttu-id="3e561-166">Não há sentido comparar indicadores de registros de tabelas diferentes entre si.</span><span class="sxs-lookup"><span data-stu-id="3e561-166">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="3e561-167">Um indicador é sempre menor ou igual a JET_cbBookmarkMost (256) bytes de comprimento, antes do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3e561-167">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length, prior to Windows Vista.</span></span>
    
<span data-ttu-id="3e561-168">**Windows Vista:** No Windows Vista e versões posteriores, os indicadores podem ser maiores que JET_cbBookmarkMost (256) bytes.</span><span class="sxs-lookup"><span data-stu-id="3e561-168">**Windows Vista:** On Windows Vista and later releases, bookmarks can be larger than JET_cbBookmarkMost (256) bytes.</span></span> <span data-ttu-id="3e561-169">O tamanho máximo de um indicador é igual ao valor atual de JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="3e561-169">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3e561-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e561-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e561-171"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3e561-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3e561-172">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3e561-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e561-173"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3e561-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3e561-174">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3e561-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e561-175"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3e561-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3e561-176">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3e561-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e561-177"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="3e561-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3e561-178">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3e561-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e561-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3e561-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3e561-180">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3e561-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3e561-181">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3e561-181">See Also</span></span>

[<span data-ttu-id="3e561-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3e561-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3e561-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3e561-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3e561-184">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3e561-184">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3e561-185">JetGoToBookmark</span><span class="sxs-lookup"><span data-stu-id="3e561-185">JetGoToBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="3e561-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="3e561-186">JetStopService</span></span>](./jetstopservice-function.md)  
<span data-ttu-id="3e561-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="3e561-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
