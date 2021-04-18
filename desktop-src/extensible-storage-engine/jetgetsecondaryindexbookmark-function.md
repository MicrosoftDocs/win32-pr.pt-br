---
description: 'Saiba mais sobre: função JetGetSecondaryIndexBookmark'
title: Função JetGetSecondaryIndexBookmark
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787667"
---
# <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="280a8-103">Função JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="280a8-103">JetGetSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="280a8-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="280a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="280a8-105">Função JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="280a8-105">JetGetSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="280a8-106">A função **JetGetSecondaryIndexBookmark** recupera um indicador especial para a entrada de índice secundário na posição atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="280a8-106">The **JetGetSecondaryIndexBookmark** function retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="280a8-107">Esse indicador pode então ser usado para reposicionar com eficiência esse cursor de volta para a mesma entrada de índice usando [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="280a8-107">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span></span> <span data-ttu-id="280a8-108">Isso é mais útil ao reposicionar em um índice secundário que contém chaves duplicadas ou que contém várias entradas de índice para o mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="280a8-108">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="280a8-109">**Windows XP: o JetGetSecondaryIndexBookmark** é introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="280a8-109">**Windows XP:  JetGetSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="280a8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="280a8-110">Parameters</span></span>

<span data-ttu-id="280a8-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="280a8-111">*sesid*</span></span>

<span data-ttu-id="280a8-112">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="280a8-112">The session to use for this call.</span></span>

<span data-ttu-id="280a8-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="280a8-113">*tableid*</span></span>

<span data-ttu-id="280a8-114">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="280a8-114">The cursor to use for this call.</span></span>

<span data-ttu-id="280a8-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="280a8-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="280a8-116">O buffer de saída que recebe a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="280a8-116">The output buffer that receives the secondary key.</span></span>

<span data-ttu-id="280a8-117">*cbSecondaryKeyMax*</span><span class="sxs-lookup"><span data-stu-id="280a8-117">*cbSecondaryKeyMax*</span></span>

<span data-ttu-id="280a8-118">O tamanho máximo, em bytes, do buffer de saída para a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="280a8-118">The maximum size, in bytes, of the output buffer for the secondary key.</span></span>

<span data-ttu-id="280a8-119">*pcbSecondaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="280a8-119">*pcbSecondaryKeyActual*</span></span>

<span data-ttu-id="280a8-120">Recebe o tamanho real em bytes da chave secundária.</span><span class="sxs-lookup"><span data-stu-id="280a8-120">Receives the actual size in bytes of the secondary key.</span></span>

<span data-ttu-id="280a8-121">Se esse parâmetro for NULL, o tamanho real da chave secundária não será retornado.</span><span class="sxs-lookup"><span data-stu-id="280a8-121">If this parameter is NULL, the actual size of the secondary key will not be returned.</span></span>

<span data-ttu-id="280a8-122">Se o buffer de saída for muito pequeno, o tamanho real da chave secundária ainda será retornado.</span><span class="sxs-lookup"><span data-stu-id="280a8-122">If the output buffer is too small, the actual size of the secondary key will still be returned.</span></span> <span data-ttu-id="280a8-123">Isso significa que esse número será maior do que o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="280a8-123">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="280a8-124">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="280a8-124">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="280a8-125">O buffer de saída que recebe o indicador de chave primária.</span><span class="sxs-lookup"><span data-stu-id="280a8-125">The output buffer that receives the primary key bookmark.</span></span>

<span data-ttu-id="280a8-126">*cbPrimaryBookmarkMax*</span><span class="sxs-lookup"><span data-stu-id="280a8-126">*cbPrimaryBookmarkMax*</span></span>

<span data-ttu-id="280a8-127">O tamanho máximo, em bytes, do buffer de saída para o indicador de chave primária.</span><span class="sxs-lookup"><span data-stu-id="280a8-127">The maximum size, in bytes, of the output buffer for the primary key bookmark.</span></span>

<span data-ttu-id="280a8-128">*pcbPrimaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="280a8-128">*pcbPrimaryKeyActual*</span></span>

<span data-ttu-id="280a8-129">Recebe o tamanho real, em bytes, do indicador de chave primária.</span><span class="sxs-lookup"><span data-stu-id="280a8-129">Receives the actual size, in bytes, of the primary key bookmark.</span></span>

<span data-ttu-id="280a8-130">Se esse parâmetro for NULL, o tamanho real do indicador de chave primária não será retornado.</span><span class="sxs-lookup"><span data-stu-id="280a8-130">If this parameter is NULL then the actual size of the primary key bookmark will not be returned.</span></span>

<span data-ttu-id="280a8-131">Se o buffer de saída for muito pequeno, o tamanho real do indicador de chave primária ainda será retornado.</span><span class="sxs-lookup"><span data-stu-id="280a8-131">If the output buffer is too small, the actual size of the primary key bookmark will still be returned.</span></span> <span data-ttu-id="280a8-132">Isso significa que esse número será maior do que o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="280a8-132">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="280a8-133">*grbit*</span><span class="sxs-lookup"><span data-stu-id="280a8-133">*grbit*</span></span>

<span data-ttu-id="280a8-134">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="280a8-134">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="280a8-135">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="280a8-135">Return Value</span></span>

<span data-ttu-id="280a8-136">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="280a8-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="280a8-137">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="280a8-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="280a8-138">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="280a8-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="280a8-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="280a8-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="280a8-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="280a8-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="280a8-141">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="280a8-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280a8-142">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="280a8-142">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="280a8-143">A operação foi concluída com êxito, mas um dos buffers de saída era muito pequeno para receber os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="280a8-143">The operation completed successfully, but one of the output buffers was too small to receive the requested data.</span></span></p>
<p><span data-ttu-id="280a8-144">O buffer de saída foi preenchido com a maior parte do indicador que couber.</span><span class="sxs-lookup"><span data-stu-id="280a8-144">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="280a8-145">O tamanho real do indicador também foi retornado, se solicitado.</span><span class="sxs-lookup"><span data-stu-id="280a8-145">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280a8-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="280a8-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="280a8-147">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="280a8-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280a8-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="280a8-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="280a8-149">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="280a8-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="280a8-150">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="280a8-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280a8-151">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="280a8-151">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="280a8-152">O cursor não está em um índice secundário no momento.</span><span class="sxs-lookup"><span data-stu-id="280a8-152">The cursor is not currently on a secondary index.</span></span></p>
<p><span data-ttu-id="280a8-153">Não é significativo recuperar um indicador de índice secundário quando o cursor não está usando um índice secundário no momento.</span><span class="sxs-lookup"><span data-stu-id="280a8-153">It is not meaningful to retrieve a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="280a8-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> deve ser usado quando o cursor não estiver em um índice secundário.</span><span class="sxs-lookup"><span data-stu-id="280a8-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280a8-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="280a8-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="280a8-156">O cursor não está posicionado em um registro.</span><span class="sxs-lookup"><span data-stu-id="280a8-156">The cursor is not positioned on a record.</span></span></p>
<p><span data-ttu-id="280a8-157">Isso pode ocorrer por vários motivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="280a8-157">This can happen for many different reasons.</span></span> <span data-ttu-id="280a8-158">Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</span><span class="sxs-lookup"><span data-stu-id="280a8-158">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280a8-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="280a8-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="280a8-160">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="280a8-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280a8-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="280a8-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="280a8-162">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="280a8-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280a8-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="280a8-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="280a8-164">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="280a8-164">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="280a8-165">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="280a8-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280a8-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="280a8-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="280a8-167">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="280a8-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="280a8-168">Em caso de sucesso, o indicador de índice secundário para a entrada de índice na posição atual de um cursor será retornado nos buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="280a8-168">On success, the secondary index bookmark for the index entry at the current position of a cursor will be returned in the output buffers.</span></span> <span data-ttu-id="280a8-169">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="280a8-169">No change to the database state will occur.</span></span>

<span data-ttu-id="280a8-170">Em caso de falha, o estado dos buffers de saída e o tamanho real do indicador de índice secundário serão indefinidos, a menos que JET_errBufferTooSmall seja retornado.</span><span class="sxs-lookup"><span data-stu-id="280a8-170">On failure, the state of the output buffers and the actual size of the secondary index bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="280a8-171">No caso em que JET_errBufferTooSmall for retornado, os buffers de saída conterão a maior parte do indicador de índice secundário que se ajustará no espaço fornecido e o tamanho real do indicador de índice secundário será preciso.</span><span class="sxs-lookup"><span data-stu-id="280a8-171">In the event that JET_errBufferTooSmall is returned, the output buffers will contain as much of the secondary index bookmark as will fit in the space provided and the actual size of the secondary index bookmark will be accurate.</span></span> <span data-ttu-id="280a8-172">De qualquer forma, nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="280a8-172">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="280a8-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="280a8-173">Remarks</span></span>

<span data-ttu-id="280a8-174">Os indicadores geralmente devem ser tratados como partes opacas de dados.</span><span class="sxs-lookup"><span data-stu-id="280a8-174">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="280a8-175">Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados.</span><span class="sxs-lookup"><span data-stu-id="280a8-175">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="280a8-176">No entanto, as seguintes propriedades podem ser conhecidas sobre todos os indicadores de ESENT:</span><span class="sxs-lookup"><span data-stu-id="280a8-176">However, the following properties can be known about all ESENT bookmarks:</span></span>

  - <span data-ttu-id="280a8-177">Um indicador identifica exclusivamente um registro em uma determinada tabela.</span><span class="sxs-lookup"><span data-stu-id="280a8-177">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="280a8-178">O indicador de um registro não será alterado durante o tempo de vida desse registro.</span><span class="sxs-lookup"><span data-stu-id="280a8-178">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="280a8-179">O indicador de um registro é o mesmo que a chave desse registro no índice primário na tabela que contém esse registro.</span><span class="sxs-lookup"><span data-stu-id="280a8-179">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="280a8-180">Se nenhum índice primário for definido nessa tabela, o mecanismo de banco de dados criará seu próprio indicador para o registro.</span><span class="sxs-lookup"><span data-stu-id="280a8-180">If no primary index is defined over that table, the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="280a8-181">Os indicadores podem ser comparados entre si usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice primário na tabela dos registros de origem.</span><span class="sxs-lookup"><span data-stu-id="280a8-181">Bookmarks may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="280a8-182">Se nenhum índice primário for definido nessa tabela, a ordenação relativa de indicadores dessa tabela não será significativa.</span><span class="sxs-lookup"><span data-stu-id="280a8-182">If no primary index is defined over that table, the relative ordering of bookmarks from that table is not meaningful.</span></span>

  - <span data-ttu-id="280a8-183">Não há sentido comparar indicadores de registros de tabelas diferentes entre si.</span><span class="sxs-lookup"><span data-stu-id="280a8-183">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="280a8-184">Um indicador é sempre menor ou igual a JET_cbBookmarkMost (256) bytes de comprimento antes do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="280a8-184">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="280a8-185">No Windows Vista e versões posteriores, os indicadores podem ser maiores.</span><span class="sxs-lookup"><span data-stu-id="280a8-185">On Windows Vista and later releases, bookmarks can be larger.</span></span> <span data-ttu-id="280a8-186">O tamanho máximo de um indicador é igual ao valor atual de JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="280a8-186">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

<span data-ttu-id="280a8-187">As chaves devem ser geralmente tratadas como partes opacas de dados.</span><span class="sxs-lookup"><span data-stu-id="280a8-187">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="280a8-188">Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados.</span><span class="sxs-lookup"><span data-stu-id="280a8-188">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="280a8-189">No entanto, as seguintes propriedades podem ser conhecidas sobre todas as chaves ESENT:</span><span class="sxs-lookup"><span data-stu-id="280a8-189">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="280a8-190">As chaves podem ser comparadas entre si usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice de origem sobre a tabela das entradas de índice de origem.</span><span class="sxs-lookup"><span data-stu-id="280a8-190">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="280a8-191">Não há sentido para comparar chaves de entradas de índice de índices diferentes entre si.</span><span class="sxs-lookup"><span data-stu-id="280a8-191">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="280a8-192">Uma chave é sempre menor ou igual a JET_cbKeyMost (255) bytes de comprimento antes do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="280a8-192">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="280a8-193">No Windows Vista e versões posteriores, as chaves podem ser maiores.</span><span class="sxs-lookup"><span data-stu-id="280a8-193">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="280a8-194">O tamanho máximo de uma chave é igual ao valor atual de JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="280a8-194">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="280a8-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="280a8-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="280a8-196"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="280a8-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="280a8-197">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="280a8-197">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280a8-198"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="280a8-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="280a8-199">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="280a8-199">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280a8-200"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="280a8-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="280a8-201">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="280a8-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280a8-202"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="280a8-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="280a8-203">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="280a8-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280a8-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="280a8-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="280a8-205">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="280a8-205">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="280a8-206">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="280a8-206">See Also</span></span>

[<span data-ttu-id="280a8-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="280a8-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="280a8-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="280a8-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="280a8-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="280a8-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="280a8-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="280a8-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="280a8-211">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="280a8-211">JetGetBookmark</span></span>](./jetgetbookmark-function.md)  
[<span data-ttu-id="280a8-212">JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="280a8-212">JetGotoSecondaryIndexBookmark</span></span>](./jetgotosecondaryindexbookmark-function.md)  
[<span data-ttu-id="280a8-213">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="280a8-213">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
<span data-ttu-id="280a8-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="280a8-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
