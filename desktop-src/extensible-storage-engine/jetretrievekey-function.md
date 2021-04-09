---
description: 'Saiba mais sobre: função JetRetrieveKey'
title: Função JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011703"
---
# <a name="jetretrievekey-function"></a><span data-ttu-id="bdfc6-103">Função JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="bdfc6-103">JetRetrieveKey Function</span></span>


<span data-ttu-id="bdfc6-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bdfc6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievekey-function"></a><span data-ttu-id="bdfc6-105">Função JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="bdfc6-105">JetRetrieveKey Function</span></span>

<span data-ttu-id="bdfc6-106">A função **JetRetrieveKey** recupera a chave da entrada de índice na posição atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-106">The **JetRetrieveKey** function retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="bdfc6-107">Essas chaves são construídas por chamadas para [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="bdfc6-107">Such keys are constructed by calls to [JetMakeKey](./jetmakekey-function.md).</span></span> <span data-ttu-id="bdfc6-108">A chave recuperada pode então ser usada para retornar com eficiência esse cursor para a mesma entrada de índice por uma chamada para [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="bdfc6-108">The retrieved key can then be used to efficiently return that cursor to the same index entry by a call to [JetSeek](./jetseek-function.md).</span></span>

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="bdfc6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdfc6-109">Parameters</span></span>

<span data-ttu-id="bdfc6-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bdfc6-110">*sesid*</span></span>

<span data-ttu-id="bdfc6-111">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-111">The session to use for this call.</span></span>

<span data-ttu-id="bdfc6-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="bdfc6-112">*tableid*</span></span>

<span data-ttu-id="bdfc6-113">O cursor a ser usado para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-113">The cursor to use for this call.</span></span>

<span data-ttu-id="bdfc6-114">*pvData*</span><span class="sxs-lookup"><span data-stu-id="bdfc6-114">*pvData*</span></span>

<span data-ttu-id="bdfc6-115">O buffer de saída que receberá a chave.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-115">The output buffer that will receive the key.</span></span>

<span data-ttu-id="bdfc6-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="bdfc6-116">*cbMax*</span></span>

<span data-ttu-id="bdfc6-117">O tamanho máximo em bytes do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-117">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="bdfc6-118">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="bdfc6-118">*pcbActual*</span></span>

<span data-ttu-id="bdfc6-119">Recebe o tamanho real em bytes da chave.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-119">Receives the actual size in bytes of the key.</span></span>

<span data-ttu-id="bdfc6-120">Se esse parâmetro for nulo, o tamanho real da chave não será retornado.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-120">If this parameter is NULL then the actual size of the key will not be returned.</span></span>

<span data-ttu-id="bdfc6-121">Se o buffer de saída for muito pequeno, o tamanho real da chave ainda será retornado.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-121">If the output buffer is too small, then the actual size of the key will still be returned.</span></span> <span data-ttu-id="bdfc6-122">Isso significa que esse número será maior do que o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-122">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="bdfc6-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="bdfc6-123">*grbit*</span></span>

<span data-ttu-id="bdfc6-124">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-124">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdfc6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bdfc6-125">Value</span></span></p></th>
<th><p><span data-ttu-id="bdfc6-126">Significado</span><span class="sxs-lookup"><span data-stu-id="bdfc6-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-127">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="bdfc6-127">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-128">Quando especificado, o mecanismo retornará a chave de pesquisa para o cursor.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-128">When specified, the engine will return the search key for the cursor.</span></span> <span data-ttu-id="bdfc6-129">A chave de pesquisa é criada usando uma ou mais chamadas anteriores para <a href="gg269329(v=exchg.10).md">JetMakeKey</a> para fins de busca dessa chave usando <a href="gg294103(v=exchg.10).md">JetSeek</a> ou definindo um intervalo de índice usando <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-129">The search key is built up using one or more prior calls to <a href="gg269329(v=exchg.10).md">JetMakeKey</a> for the purposes of seeking to that key using <a href="gg294103(v=exchg.10).md">JetSeek</a> or setting an index range using <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="bdfc6-130">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bdfc6-130">Return Value</span></span>

<span data-ttu-id="bdfc6-131">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bdfc6-132">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bdfc6-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdfc6-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bdfc6-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="bdfc6-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdfc6-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bdfc6-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-136">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfc6-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bdfc6-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-138">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bdfc6-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-140">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bdfc6-141">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfc6-142">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="bdfc6-142">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-143">Não há uma chave de pesquisa atual para o cursor.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-143">There is no current search key for the cursor.</span></span> <span data-ttu-id="bdfc6-144">Isso ocorrerá para <strong>JetRetrieveKey</strong> se JET_bitRetrieveCopy for especificado e uma chave de pesquisa não tiver sido construída para este cursor usando uma chamada anterior para <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-144">This will happen for <strong>JetRetrieveKey</strong> if JET_bitRetrieveCopy is specified and a search key has not been constructed for this cursor using a prior call to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span> <span data-ttu-id="bdfc6-145">A chave de pesquisa será excluída por uma chamada anterior para qualquer API de navegação no cursor que não seja <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-145">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-146">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bdfc6-146">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-147">O cursor não está posicionado em um registro.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-147">The cursor is not positioned on a record.</span></span> <span data-ttu-id="bdfc6-148">Isso pode ocorrer por vários motivos diferentes.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-148">This can happen for many different reasons.</span></span> <span data-ttu-id="bdfc6-149">Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-149">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfc6-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bdfc6-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-151">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bdfc6-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-153">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfc6-154">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bdfc6-154">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-155">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-155">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="bdfc6-156">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bdfc6-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-158">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfc6-159">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="bdfc6-159">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="bdfc6-160">A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber a chave inteira.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-160">The operation completed successfully, but the output buffer was too small to receive the entire key.</span></span> <span data-ttu-id="bdfc6-161">O buffer de saída foi preenchido com o máximo de chave que se ajustaria.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-161">The output buffer has been filled with as much of the key as would fit.</span></span> <span data-ttu-id="bdfc6-162">O tamanho real da chave também foi retornado, se solicitado.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-162">The actual size of the key has also been returned, if requested.</span></span></p>
<p><span data-ttu-id="bdfc6-163"><strong>Observação</strong>   Esse erro não será retornado se JET_bitRetrieveCopy for especificado.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-163"><strong>Note</strong>   This error will not be returned if JET_bitRetrieveCopy is specified.</span></span> <span data-ttu-id="bdfc6-164">Consulte a seção comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-164">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bdfc6-165">Em caso de sucesso, a chave para a entrada de índice na posição atual de um cursor será retornada no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-165">On success, the key for the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="bdfc6-166">Se JET_wrnBufferTruncated for retornado, o buffer de saída conterá a maior parte da chave que se ajustará no espaço fornecido e o tamanho real da chave será preciso.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-166">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the key as will fit in the space provided and the actual size of the key will be accurate.</span></span> <span data-ttu-id="bdfc6-167">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-167">No change to the database state will occur.</span></span>

<span data-ttu-id="bdfc6-168">Em caso de falha, o estado do buffer de saída e o tamanho real da chave serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-168">On failure, the state of the output buffer and the actual size of the key will be undefined.</span></span> <span data-ttu-id="bdfc6-169">Nenhuma alteração no estado do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-169">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bdfc6-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdfc6-170">Remarks</span></span>

<span data-ttu-id="bdfc6-171">As chaves devem ser geralmente tratadas como partes opacas de dados.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-171">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="bdfc6-172">Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-172">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="bdfc6-173">No entanto, as seguintes propriedades podem ser conhecidas sobre todas as chaves ESENT:</span><span class="sxs-lookup"><span data-stu-id="bdfc6-173">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="bdfc6-174">As chaves podem ser comparadas entre si usando a função [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) para estabelecer sua ordenação relativa no índice de origem sobre a tabela das entradas de índice de origem.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-174">Keys may be compared against each other using [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) function to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="bdfc6-175">Não há sentido para comparar chaves de entradas de índice de índices diferentes entre si.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-175">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="bdfc6-176">Uma chave é sempre menor ou igual a JET_cbKeyMost (255) bytes de comprimento antes do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-176">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="bdfc6-177">No Windows Vista e versões posteriores, as chaves podem ser maiores.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-177">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="bdfc6-178">O tamanho máximo de uma chave é igual ao valor atual de JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-178">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="bdfc6-179">Além das propriedades acima das chaves ESENT em geral, é importante observar que uma chave de pesquisa é diferente da chave para uma entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-179">In addition to the above properties of ESENT keys in general, it is important to note that a search key is different from the key for an index entry.</span></span> <span data-ttu-id="bdfc6-180">Especificamente, uma chave de pesquisa pode ser maior que uma chave comum.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-180">Specifically, a search key may be longer than an ordinary key.</span></span> <span data-ttu-id="bdfc6-181">Esse comprimento extra ocorre quando uma opção curinga é usada ao construir a chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-181">This extra length occurs when a wildcard option is used while constructing the search key.</span></span> <span data-ttu-id="bdfc6-182">Consulte [JetMakeKey](./jetmakekey-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-182">See [JetMakeKey](./jetmakekey-function.md) for more information.</span></span>

<span data-ttu-id="bdfc6-183">Há um bug importante nessa API que está presente em todas as versões.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-183">There is an important bug in this API that is present in all releases.</span></span> <span data-ttu-id="bdfc6-184">Se a chave de pesquisa for solicitada usando o uso de JET_bitRetrieveCopy e o buffer de saída for muito pequeno para receber a chave inteira, JET_wrnBufferTruncated não será retornado.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-184">If the search key is requested using the use of JET_bitRetrieveCopy and the output buffer is too small to receive the entire key then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="bdfc6-185">JET_errSuccess será retornado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-185">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="bdfc6-186">É importante verificar se o tamanho real da chave, como retornado usando *pcbActual* , é menor ou igual ao tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-186">It is important to verify that the actual size of the key as returned using *pcbActual* is less than or equal to the size of the output buffer.</span></span> <span data-ttu-id="bdfc6-187">Se o tamanho real for maior do que o tamanho do buffer de saída, o chamador de **JetRetrieveKey** deverá reagir como se JET_wrnBufferTruncated retornassem em vez disso.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-187">If the actual size is larger than the size of the output buffer, then the caller of **JetRetrieveKey** should react as if JET_wrnBufferTruncated were returned instead.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bdfc6-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdfc6-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-189"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bdfc6-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bdfc6-190">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfc6-191"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="bdfc6-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bdfc6-192">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-193"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="bdfc6-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bdfc6-194">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfc6-195"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="bdfc6-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bdfc6-196">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfc6-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bdfc6-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bdfc6-198">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bdfc6-198">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bdfc6-199">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bdfc6-199">See Also</span></span>

[<span data-ttu-id="bdfc6-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bdfc6-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bdfc6-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bdfc6-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bdfc6-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bdfc6-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bdfc6-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bdfc6-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bdfc6-204">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="bdfc6-204">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="bdfc6-205">JetSeek</span><span class="sxs-lookup"><span data-stu-id="bdfc6-205">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="bdfc6-206">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="bdfc6-206">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
